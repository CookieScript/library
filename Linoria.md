no this is not my ui
I did not made this

this is js a example on how to use it

# booting the ui ilb

```
local repo = 'https://raw.githubusercontent.com/LionTheGreatRealFrFr/MobileLinoriaLib/main/'

local Library = loadstring(game:HttpGet(repo .. 'Library.lua'))()
local ThemeManager = loadstring(game:HttpGet(repo .. 'addons/ThemeManager.lua'))()
local SaveManager = loadstring(game:HttpGet(repo .. 'addons/SaveManager.lua'))()

--[[
Dont Change any here its important
you can delete ts msg also
]]
```

# Making the Window

```
local Window = Library:CreateWindow({
    Title = 'Example menu',
    Center = true,
    AutoShow = true,
    TabPadding = 8,
    MenuFadeTime = 0.2,
})

--[[
if you want to change the size add this to the table
Size = UDim2.new(0, 430, 0, 460),
]]
```

# Adding the Tabs

```
local Tabs = {
    Main = Window:AddTab('Main'),
    ['UI Settings'] = Window:AddTab('UI Settings'),
}

--[[
you can also change the names
]]
```

# Adding the Section

```
local Section = Tabs.Main:AddLeftGroupbox('Section')
--[[
You can also change the name
and also if you want to move it to the right rename Left to Right
]]
```

# Toggle

```
Section:AddToggle('MyToggle', {
    Text = 'Name',
    Default = true,
    Tooltip = 'Information',

    Callback = function(Value)

    end
})

--[[
you can also change the Name
Default value (true / false)
The Tooltip is the Information shown when you hover over the toggle
]]
```

```
Toggles.MyToggle:OnChanged(function()
    print('MyToggle changed to:', Toggles.MyToggle.Value)
end)

-- This should print to the console: "My toggle state changed! New value: false"
Toggles.MyToggle:SetValue(false)

--[[
here we get our toggle object & then get its value
]]
```

# Buttons

```
local MyButton = Section:AddButton('Button', function()
    print('You clicked a button!')
end)

local MyButton2 = MyButton:AddButton('Sub button', function()
    print('You clicked a sub button!')
end)
```

# Label

```
Section:AddLabel('This is a label')
Section:AddLabel('This is a label\n\nwhich wraps its text!', true)
```

# Divider

```
Section:AddDivider()
```

# Slider

```
Section:AddSlider('MySlider', {
    Text = 'Name',
    Default = 0,
    Min = 0,
    Max = 5,
    Rounding = 1,
    Compact = false,

    Callback = function(Value)
        
    end
})
```

```
local Number = Options.MySlider.Value
Options.MySlider:OnChanged(function()
    print('MySlider was changed! New value:', Options.MySlider.Value)
end)

-- This should print to the console: "MySlider was changed! New value: 3"
Options.MySlider:SetValue(3)
```

#

```
Section:AddInput('MyTextbox', {
    Default = 'Name',
    Numeric = false,
    Finished = false,
    
    Text = 'Name',
    Tooltip = 'Information',
    
    Placeholder = 'Placeholder text',
    
    Callback = function(Value)
        
    end
})

Options.MyTextbox:OnChanged(function()
    print('Text updated. New text:', Options.MyTextbox.Value)
end)

--[[
You can also Change the name
Numeric true / false, only allows numbers
Finished true / false, only calls callback when you press enter
Tooltip Information shown when you hover over the textbox
MaxLength is also an option which is the max length of the text
]]
```

#

```
Section:AddDropdown('MyDropdown', {
    Values = { 'This', 'is', 'a', 'dropdown' },
    Default = 1,
    Multi = false,
    
    Text = 'A dropdown',
    Tooltip = 'Information',
    
    Callback = function(Value)
        
    end
})

--[[
You can also change the name
Default number index of the value / string
Multi true / false, allows multiple choices to be selected
Tooltip Information shown when you hover over the dropdown
]]
```

