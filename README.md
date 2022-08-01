
wait(1)
do
   repeat until game:IsLoaded()
end
coroutine.wrap(function()
    if not game:IsLoaded() then
        repeat task.wait(1)
        until game:IsLoaded()
    end
   if identifyexecutor() == 'Arceus V2' or game:GetService("Stats").PerformanceStats.Memory:GetValueString{} and game:GetService("Stats").PerformanceStats.NetworkReceived:GetValueString{} and game:GetService("Stats").PerformanceStats.Ping:GetValueString{} then
      local function UserInputService()
          coroutine.wrap(function()
              pcall(function()
                 -- script
              end);
          end)();
         return UserInputService
      end
      if game.PlaceId == (game.PlaceId) then
         if game:IsLoaded() == true then
            coroutine.wrap(function()
               UserInputService()
               game.CoreGui.RobloxPromptGui.promptOverlay.ChildAdded:Connect(function(child)
                  if child.Name == "ErrorPrompt" then
                     local HttpService, DataService = game:GetService"HttpService", game:GetService"TeleportService";local OtherServers = HttpService:JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100"))
                     for Index, Server in next, OtherServers["data"] do
                        if Server ~= game.JobId then
                           DataService:TeleportToPlaceInstance(game.PlaceId, game.JobId, game:GetService("Players").LocalPlayer, Server["id"]);
                           game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId, game:GetService("Players").LocalPlayer);
                           game:Shutdown();
                        end
                     end
                  end
               end)
            end)();
            game:GetService("Players").LocalPlayer.Idled:connect(function()
                game:GetService("VirtualUser"):Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame);
                game:GetService("VirtualUser"):Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame);
            end)
        end
      elseif game.PlaceId == nil then
         return (game.PlaceId) or nil
      end
   elseif game:Shutdown() then
      return (game.PlaceId) or nil
   end
end)();
