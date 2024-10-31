# Russia-Car-Driving-Sochi-Script

Basic Auto Farm Script For RCDS

```lua
asd = game.Workspace.Pumpkins

for _, v in pairs(asd:GetChildren()) do
    wait(2)
    if v:GetChildren()[1] then
        v.CanCollide = false
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame
        v:GetChildren()[1].Label.ProximityPrompt.HoldDuration = 0
        wait(0.5)
        fireproximityprompt(v:GetChildren()[1].Label.ProximityPrompt)
    end
end
```

How To Use:
1. Join Game
2. Execute script
3. That's all

Script is Open Source, so You Can Modify Whatever You Want
