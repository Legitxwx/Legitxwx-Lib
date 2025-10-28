```local LegitxWX = require(game.ReplicatedStorage.LegitxWXLibTabs)```

```
local Window = LegitxWX:CreateWindow({
	Title = "LegitxWX Hub",
	Author = "Frietz Cyan Alag",
	RBXID = "127742093697776",
	UseToggles = true
})
```
```
local MainTab = Window:CreateTab("Main")
MainTab:CreateButton({
	Name = "Auto Farm",
	Description = "Automatically farms all drops.",
	Callback = function()
		print("Auto Farm Running!")
	end
})
```

MainTab:CreateButton({
	Name = "ESP Loader",
	Description = "Loads custom ESP script.",
	Script = [[
		print("ESP loaded via loadstring!")
	]]
})

MainTab:CreateToggle("God Mode", false, function(state)
	print("God Mode:", state)
end)

local MiscTab = Window:CreateTab("Misc")
MiscTab:CreateButton({
	Name = "Fly",
	Description = "Lets you fly around.",
	Callback = function()
		print("Fly toggled!")
	end
})
