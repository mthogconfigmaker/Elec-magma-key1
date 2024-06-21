script_key = "ixrddxLYtVjXNgplqdWmIuxIDvvdRwwg" -- cf by mrbear
getgenv().Team = "Pirates"
getgenv().WebhookSetting = {
    Enable = true, -- cf by mrbear
    Url = "",
    Embed = true,
    StoredFruit = true,
    ImageEmbed = true,
    CustomImage = true,
    CustomImageUrl = "https://i.imgur.com/StwILNy.png", --Your Url
    OnServerHop = true,
    BountyChanged = true,
}
getgenv().PlayerSetting = {
    SafeMode = true,
    SafeModeHealth = {4300,40},--Number And %, Start Safe Mode And Stop Safe Mode
    UseRaceV3 = true,
    SmartUseRaceV3= true,
    DashIfV4 = true,
    Dash= false,
    IgnoreInCombat = true, --Turn This Off When Reseting Or Hop You Lost Bounty (Rare, Happens On Some Accounts) cf by eric
    ChatKillEnable = true,
    Chat = {"Fixed By MrBear","MrBear is best"},
    IgnoreFriends = false, --true neu muon co ban be vao no hop sv
}
getgenv().AttackSetting = {
    ForceMelee = true,
    ForceMeleeTime = 3,
    StopAttack =true, --When Meet Below Condition
    StopAttackAtHealth = 69,--%
    FastAttack=true, -- Toggle Fast Attack
}
getgenv().UseSkillSetting = {
    -- Three Methods: "Normal", "Fast", "Spam", "SpamAll"
    MethodIfTargetOnV4 = "Fast",
    MethodIfPlayerOnV4 = "SpamAll",
    MethodIfTargetUseFruit = {Fruits={"Buddha","Portal"},Method="Fast"},
    NormalMethod = "Normal",
    LowHealthPlayerCondition = { --Player Can Attack Us, No Need For Slow Attack
        Enable = true,
        Health = 60,--%Health That Are Low
        Method = "Fast",
    },
    LowHealthTargetCondition = {
        Enable = true, -- cf by mrbear
        Health = 20,--%Health That Are Low
        DelayFirstTime = {true,2}, --1 Is Enable, 2 Is Second To Delay Before Attack Again
        Method = "Normal",
        WaitTime = 1,-- If Normal Method, Wait Every Skill If It Hits Target
    }
}
getgenv().WeaponsSetting = {
    ["Melee"] = {
        ["Enable"] = true, -- cf by mrbear
        ["Delay"] = 1, 
        ["SwitchNextWeaponIfCooldown"] = true,
        ["Skills"] = {
            ["Z"] = {
                ["Enable"] = true,
                ["NoPredict"] = true, -- For Dragon Tailon, Disable it 
                ["HoldTime"] = 0.75,
                ["TimeToNextSkill"] = 0.3, -- cf by mrbear
            },
        [ "X"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.2,
                ["TimeToNextSkill"] = 0.3, -- cf by mrbear
            },

            ["C"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.1,
                ["TimeToNextSkill"] = 0.3, -- cf by mrbear
            },
        },
    },
    ["Blox Fruit"] = {
        ["Enable"] = true, -- cf by mrbear
        ["Delay"] = 2,
        ["SwitchNextWeaponIfCooldown"] = true,
        ["Skills"] = {
            ["Z"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.2,
                ["TimeToNextSkill"] = 0.3, -- cf by mrbear
            },
            ["X"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.2,
                ["TimeToNextSkill"] = 0.3, -- cf by mrbear
            },

            ["C"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.2,
                ["TimeToNextSkill"] = 0.3, -- cf by mrbear
            },
            ["V"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.1,
                ["TimeToNextSkill"] = 0.3, -- cf by MrBear
            },
            ["F"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0,
                ["TimeToNextSkill"] = 0, -- cf by MrBear
            },
        },
    },
    ["Sword"] = {
        ["Enable"] = false, -- cf by mrbear
        ["Delay"] = 0.1,
        ["Skills"] = {
            ["Z"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.1,
                ["TimeToNextSkill"] = 0, -- cf by mrbear
            },
            ["X"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.1,
                ["TimeToNextSkill"] = 0, -- cf by mrbear
            },
        },
    },
    ["Gun"] = {
        ["Enable"] = false, -- cf by mrbear
        ["Delay"] = 0.1,
        ["Skills"] = {
            ["Z"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.1,
                ["TimeToNextSkill"] = 0, -- cf by mrbear
            },
            ["X"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.1,
                ["TimeToNextSkill"] = 0, -- cf by mrbear
            },
        },
    },
}
getgenv().Theme = { -- getgenv().Theme = false if you want to disable
    OldTheme = false, -- cf by mrbear
    Name="MrBear", --"Raiden","Ayaka","Hutao","Yelan","Miko","Nahida","Ganyu","Keqing","Nilou","Barbara","Zhongli","Layla"
    Custom={
            ["Enable"] = true, -- cf by mrbear
            ['char_size'] = UDim2.new(0.668, 0, 1.158, 0),
            ['char_pos'] = UDim2.new(0.463, 0, -0.105, 0),
            ['title_color'] = Color3.fromRGB(0, 0, 0, 1),
            ['titleback_color'] = Color3.fromRGB(0, 0, 0, 1), -- color black
            ['list_color'] = Color3.fromRGB(0, 0, 0, 1),
            ['liststroke_color'] = Color3.fromRGB(0, 0, 0, 1), -- color black
            ['button_color'] = Color3.fromRGB(0, 0, 0, 1)
       }
}
loadstring(game:HttpGet("https://api.luarmor.net/files/v3/loaders/b6d24ef1f7dab9c7b22f259a3db6c47e.lua"))()
