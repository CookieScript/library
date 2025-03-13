No This is not mine You can check the original here
https://pastebin.com/raw/Ajm4hBP7
# booting the Library

```
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/cat"))()
--you can go into the github link and copy all of it and modify it for yourself.
```
# Making the Window

```
local Window = Library:CreateWindow("cattoware UI", Vector2.new(492, 598), Enum.KeyCode.RightControl)
--you can change your UI keybind
```

# Making ur tab

```
local AimingTab = Window:CreateTab("Tab 1")
--[[
you can rename this tab to whatever you want
you can also change the tabs code, for example "AimingTab" can be changed to "FunnyCoolTab" etc.
]]
```

# Creating Your Section

```
local testSection = AimingTab:CreateSector("First Section", "left")
--you can  change the section code, for example "testsection" can be changed to "FunnyCoolSection" etc.
```

# Toggle

```
testSection:AddToggle("Toggle", false, function(Value)
    
end)
```

# Button

```
testSection:AddButton("Button", function(Value)
    
end)
```

# Slider

```
testSection:AddSlider("Slider", 0, 120, 2000, 1, function(Value)
    
end)
```

# Textbox

```
testSection:AddTextbox("textbox", nil, function(Value)

end)
```

# Dropdown

```
testSection:AddDropdown("Dropdown", {"1", "2"}, "1", true, function(Value)

end)
```

# Colorpicker With Toggle

```
local ColorToggle = testSection:AddToggle("ColorPicker w/Toggle", false, function(Value)

end)

ColorToggle:AddColorpicker(Color3.fromRGB(255,255,255), function(Value)
   
end)
```

# Toggle with keybind

```
local ToggleBind = testSection:AddToggle("Keybind w/Toggle", false, function(Value)

end)

ToggleBind:AddKeybind()
```

# Config

```
AimingTab:CreateConfigSystem("right")
--this is the config system
```
