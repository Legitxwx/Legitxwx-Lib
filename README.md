```
local lib = require(game.ReplicatedStorage.LegitxwxUILib)
```
```
local win = lib.CreateWindow({
	Title = "Legitxwx Hub",
	Author = "Frietz Cyan Alag",
	RBXID = tostring(game.Players.LocalPlayer.UserId),
	Size = UDim2.new(0, 720, 0, 480),
	AutoScale = true,
	SaveSettings = true,
	TabPosition = "Left",
	Animations = true,
	Theme = "Modern"
})
```
```
local main = win:CreateTab("Main")
```
```
main:CreateSection("Main Controls")
```
```
main:CreateLabel("Welcome to Legitxwx UI!")
```
```
main:CreateToggle({
	Name = "Auto Farm",
	Default = false,
	SaveKey = "autoFarm",
	Callback = function(s)
		print("AutoFarm:", s)
	end
})
```
```
main:CreateSlider({
	Name = "Speed",
	Min = 16,
	Max = 200,
	Default = 16,
	Step = 1,
	SaveKey = "speed",
	Callback = function(v)
		print("Speed:", v)
	end
})
```
```
main:CreateDropdown({
	Name = "Mode",
	Options = {"Easy", "Normal", "Hard"},
	Default = "Normal",
	SaveKey = "mode",
	Callback = function(v)
		print("Mode:", v)
	end
})
```
```
local progress = main:CreateProgress({
	Name = "Load",
	Value = 20
})
```
```
main:CreateColorPicker({
	Name = "Accent Color",
	Default = {R = 90, G = 160, B = 255},
	SaveKey = "accent",
	Callback = function(c)
		print("Color", c.R, c.G, c.B)
	end
})
```
```
main:CreateTextbox({
	Name = "Custom",
	Placeholder = "Type...",
	SaveKey = "custom",
	Callback = function(t)
		print("Text:", t)
	end
})
```
```
win:Notify("Loaded", "Legitxwx UI v3 ready", 3)
```
