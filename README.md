_G.Setting = {
    UI = {
        -- // [Setting UI Main] \\ --

        ["Logo"] = 000000, -- Use You Logo
        ["Rainbow"] = false, -- Coming Soon

        -- // [Size UI] \\ --

        ["Size UI"] = UDim2.fromOffset(500, 355), -- or UDim2.fromOffset(500, 545) 
        
        -- // [Color UI] \\ --

        ["Main"] = Color3.fromRGB(0, 255, 0),
        ["Background"] = Color3.fromRGB(40, 40, 40),
        ["OuterBorder"] = Color3.fromRGB(15, 15, 15),
        ["InnerBorder"] = Color3.fromRGB(73, 63, 73),
        ["TopGradient"] = Color3.fromRGB(35, 35, 35),
        ["BottomGradient"] = Color3.fromRGB(29, 29, 29),
        ["SectionBackground"] = Color3.fromRGB(35, 34, 34),
        ["Section"] = Color3.fromRGB(176, 175, 176),
        ["OtherElementText"] = Color3.fromRGB(129, 127, 129),
        ["ElementText"] = Color3.fromRGB(185, 185, 185),
        ["ElementBorder"] = Color3.fromRGB(20, 20, 20),
        ["SelectedOption"] = Color3.fromRGB(55, 55, 55),
        ["UnselectedOption"] = Color3.fromRGB(40, 40, 40),
        ["HoveredOptionTop"] = Color3.fromRGB(65, 65, 65),
        ["UnhoveredOptionTop"] = Color3.fromRGB(50, 50, 50),
        ["HoveredOptionBottom"] = Color3.fromRGB(45, 45, 45),
        ["UnhoveredOptionBottom"] = Color3.fromRGB(35, 35, 35),
        ["TabText"] = Color3.fromRGB(185, 185, 185)
    }
}

local library = loadstring(game:HttpGet("https://newpchx2.0xlii.repl.co/AllUI/NotProted_2554156454264842.lua"))()
local Wait = library.subs.Wait


local PepsisWorld = library:CreateWindow({
    Name = "Playback X Zee X ลุงตู่ | KL BF PetsimX",
    Image = "7483871523",
    Themeable = {
        Info = "Discord Server: VzYTJ7Y"
    }
})

local GeneralTab = PepsisWorld:CreateTab({
	Name = "General"
})

local FarmingSection = GeneralTab:CreateSection({
	Name = "Farming"
})

FarmingSection:AddSlider({
	Name = "Coin Distance",
	Flag = "FarmingSection_CoinDistance",
	Value = 175,
	Min = 0,
	Max = 200,
	Format = function(Value)
		if Value == 0 then
			return "Collection Distance: Infinite"
		else
			return "Collection Distance: " .. tostring(Value)
		end
	end
})

local BoardControlSection = GeneralTab:CreateSection({
Name = "Board Control"
})

local MiscSection = GeneralTab:CreateSection({
	Name = "Misc",
	Side = "Right"
})

MiscSection:AddButton({
	Name = "Repair Board",
	Callback = function()
		print("Fixed")
	end
})
MiscSection:AddKeybind({
	Name = "Test Key",
	Callback = print
})
MiscSection:AddToggle({
	Name = "Test Toggle/Key",
	Keybind = {
	Mode = "Dynamic" -- Dynamic means to use the 'hold' method, if the user keeps the button pressed for longer than 0.65 seconds; else use toggle method
	},
	Callback = function(v)
	
	end
})

local FunSection = GeneralTab:CreateSection({
	Name = "Fun Cosmetics"
})
FunSection:AddToggle({
	Name = "Ragdoll Assumes Flight",
	Flag = "FunSection_AssumesFlight"
})
FunSection:AddToggle({
	Name = "Ragdoll On Player Collision",
	Flag = "FunSection_RagdollOnPlayerCollision"
})
FunSection:AddToggle({
	Name = "Un-Ragdoll When Motionless",
	Flag = "FunSection_UnRagdollWhenMotionless"
})
FunSection:AddToggle({
	Name = "Extend Ragdoll Duration",
	Flag = "FunSection_ExtendRagdollDuration"
})
FunSection:AddSlider({
	Name = "Coin Distance",
	Flag = "FarmingSection_Coin Distance",
	Value = 4,
	Min = 0,
	Max = 60,
	Textbox = true,
	Format = function(Value)
		if Value == 0 then
			return "Ragdoll Extension: Indefinite"
		else
			return "Ragdoll Extension: " .. tostring(Value) .. "s"
		end
	end
})
