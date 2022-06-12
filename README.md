ModIDS = { 

12345,
15893719,
2843359276,
1573076392,
3587651675,

}

local Player = game.Players.LocalPlayer
local plr = game.Players.LocalPlayer
local Players = game.Players
local player = game.Players.LocalPlayer
local char = game.Players.LocalPlayer.Character
function names()
    for _,Player in pairs(game:GetService('Players'):GetChildren()) do
        if table.find(ModIDS, Player.UserId) then
            if Player.Character then
                if Player.Character.Parent.Name == 'Players' then
                    Player.Character:FindFirstChildWhichIsA('Humanoid').DisplayName = ('[🥊]' .. Player.DisplayName)
                end
            end
        else
            if Player.Character then
                if Player.Character.Parent.Name == 'Players' then
                    if not Player.Character.UpperTorso:FindFirstChild('OriginalSize') then
                        Player.Character:FindFirstChildWhichIsA('Humanoid').DisplayName = ('[🌟]' .. Player.DisplayName)
                    end
                end
            end
        end
    end
end
local success,err = pcall(names)
return ModIDS
