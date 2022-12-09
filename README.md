local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("TITLE", "Midnight")
local Tab = Window:NewTab("Luffy")
    local Section = Tab:NewSection("Skill")
        Section:NewKeybind("Heavy Slam", "KeybindInfo", Enum.KeyCode.Z, function()
            local args = {
                [1] = game:GetService("Players").LocalPlayer
            }
            
            game:GetService("ReplicatedStorage").Characters.MrFantastic.Remotes.StretchSlam:FireServer(unpack(args))                                   
    end)
    Section:NewKeybind("Counter", "KeybindInfo", Enum.KeyCode.X, function()
        local args = {
            [1] = game:GetService("Players").LocalPlayer
        }
        
        game:GetService("Players").LocalPlayer.Character.MrFantastic.CounterActivate:FireServer(unpack(args))                        
    end)
    Section:NewKeybind("Counter", "KeybindInfo", Enum.KeyCode.C, function()
        local args = {
            [1] = game:GetService("Players").LocalPlayer
        }
        
        game:GetService("Players").LocalPlayer.Character.MrFantastic.CounterActivate:FireServer(unpack(args))                       
    end)
    Section:NewKeybind("SmashGround", "KeybindInfo", Enum.KeyCode.V, function()
        local args = {
            [1] = game:GetService("Players").LocalPlayer
        }
        
        game:GetService("Players").LocalPlayer.Character.MrFantastic.GroundSmoke:FireServer(unpack(args))                
    end)
    Section:NewKeybind("Heal", "KeybindInfo", Enum.KeyCode.E, function()
        local args = {
            [1] = Vector3.new(-2.6949658393859863, 14.10774040222168, 390.3093566894531)
        }
        
        game:GetService("ReplicatedStorage").Characters.Moonknight.Remotes.Heal:FireServer(unpack(args))                
    end)
local Tab = Window:NewTab("Cradit")
    local Section = Tab:NewSection("UI")
    Section:NewKeybind("Hide UI", "KeybindInfo", Enum.KeyCode.P, function()
	Library:ToggleUI()
end)
