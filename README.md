# BasicLibrary
A lightweight library for basic needs

(this took me about 3 days lol.)

# Documentation


# UI Engine:
local BasicLibrary = loadstring(game:HttpGet('https://raw.githubusercontent.com/UserUnkown404/BasicLibrary/main/Library'))()


# Functions Returned
**Basic Library Variable**

variable BasicLibrary: BasicLibrary:New(Title), BasicLibrary:UserNotify(String, Duration)

**Example Usage:**

local BasicLibrary = loadstring(game:HttpGet('https://raw.githubusercontent.com/UserUnkown404/BasicLibrary/main/Library'))()

local MainUI = BasicLibrary:New("MainUI")

BasicLibrary:UserNotify("Successfully loaded!", 2)

**MainUI Variable**

variable MainUI: MainUI:NewTab(Name), MainUI:Exit()

**Example Usage:**

local BasicLibrary = loadstring(game:HttpGet('https://raw.githubusercontent.com/UserUnkown404/BasicLibrary/main/Library'))()

local MainUI = BasicLibrary:New("MainUI")

local Tab1 = MainUI:NewTab("1")

BasicLibrary:UserNotify("Successfully loaded!", 2)

task.wait(2)
MainUI:Exit()

**Tab1 Variable**

variable Tab1: Tab1:NewTitle(String), Tab1:NewButton(String,Call), Tab1:NewText(String), Tab1:NewSlider(String, Min, Max, SetValue), Tab1:NewToggle(String), Tab1:NewDropDown(TableList, SelectValue), Tab1:NewKeyBind(String, SetKeybind), Tab1:NewTextBox(String, SetText)

**returned functions:**

NewSlider:setSliderValue(Value)

NewToggle:setBoolValue(Bool), NewToggle:getBoolValue(): bool

NewDropDown:setNewValue(value), NewDropDown:removeValue(value), NewDropDown:selectValue(value), NewDropDown:getValue(): bool

NewKeyBind:NewCallBegan(Call_, gameProcessedChecker), NewKeyBind:NewCallEnded(Call_, gameProcessedChecker), NewKeyBind:getKeyBind(): Enum Keybind

NewTextBox:SetText(String), NewTextBox:GetText(): TextBox's Text

**Example Usage**

local BasicLibrary = loadstring(game:HttpGet('https://raw.githubusercontent.com/UserUnkown404/BasicLibrary/main/Library'))()

local MainUI = BasicLibrary:New("MainUI")

local Tab1 = MainUI:NewTab("1")

Tab1:NewTitle("1")

Tab1:NewText("Library UI")

Tab1:NewButton("Exit",function()
    MainUI:Exit()
end)

local Slider = Tab1:NewSlider("Wisdom of the Slider", -100, 100, 0)

local Toggle = Tab1:NewSlider("Toggle your mo-")

local ShoppingList = Tab1:NewDropDown({workspace, 123, "how about I go down your on mothe-", game:GetService("Players").LocalPlayer}, 123)

local Keybind = Tab1:NewKeyBind("+25 cents to charity", "E")

local YapYaYappityYapYappityYap = Tab1:NewTextBox("Holy yapping of the yappingtons", "Yapping")

Slider:setSliderValue(200)

NewToggle:setBoolValue(true)

print(NewToggle:getBoolValue())

NewDropDown:setNewValue(12873213498217391)

NewDropDown:removeValue(123)

NewDropDown:selectValue(workspace)

print(NewDropDown:getValue())

NewKeyBind:NewCallBegan(function()
    print("go donate if you have 25 cents 🤑")
end, true)

NewKeyBind:NewCallEnded(function()
    print("😏")
end, true)

print(NewKeyBind:getKeyBind())

NewTextBox:SetText("too much yapping")

print(NewTextBox:GetText())

BasicLibrary:UserNotify("Successfully loaded!", 2)

