game.Players.PlayerAdded:Connect(function(player)
    local playerGui = player:WaitForChild("PlayerGui")
    local backpack = player:WaitForChild("Backpack")

    for _, weapon in pairs(game.ServerStorage.Guns:GetDescendants()) do
        if weapon:IsA("Tool") then
            local newWeapon = weapon:Clone()
            newWeapon.Parent = backpack
        end
    end
end)
