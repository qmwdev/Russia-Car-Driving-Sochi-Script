# Russia-Car-Driving-Sochi-Script

Basic Auto Farm Script For RCDS

HALLOWEEN AutoFarm
```lua
asd = game.Workspace.Pumpkins

task.spawn(function()
	while task.wait() do
		for _,v in pairs(asd:GetChildren()) do
			wait(5) -- wait time between teleportation
			if v:GetChildren()[1] then -- p100 check and code
				v.CanCollide = false
				game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame
				wait(0.5)
				v:GetChildren()[1].Label.ProximityPrompt.HoldDuration = 0
				wait(0.5)
				fireproximityprompt(v:GetChildren()[1].Label.ProximityPrompt) -- йоу йоу картошка фри
			end
		end
	end
end)

```

Money AutoFarm
```lua
local start = game.Workspace.Jobs["Грузчик"].Base
local finish = game.workspace.Jobs['Грузчик'].Finish
local lpr = game.Players.LocalPlayer.Character.HumanoidRootPart

if lpr then
    task.spawn(function()
        while task.wait() do
            lpr.CFrame = start.CFrame
            task.wait(0.5)
            for _ = 1, 3 do
                fireproximityprompt(start.ProximityPrompt)
            end
            task.wait(0.5)
            lpr.CFrame = finish.CFrame
        end
    end)
else
    warn("HumanoidRootPart or ProximityPrompt not found.")
end
```

How To Use:
1. Join Game
2. Execute script
3. That's all

Script is Open Source, so You Can Modify Whatever You Want
