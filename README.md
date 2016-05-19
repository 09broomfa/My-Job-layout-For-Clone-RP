--[[---------------------------------------------------------------------------
DarkRP custom jobs
---------------------------------------------------------------------------
This file contains your custom jobs.
This file should also contain jobs from DarkRP that you edited.
Note: If you want to edit a default DarkRP job, first disable it in darkrp_config/disabled_defaults.lua
	Once you've done that, copy and paste the job to this file and edit it.
The default jobs can be found here:
https://github.com/FPtje/DarkRP/blob/master/gamemode/config/jobrelated.lua
For examples and explanation please visit this wiki page:
http://wiki.darkrp.com/index.php/DarkRP:CustomJobFields
Add jobs under the following line:
---------------------------------------------------------------------------]]
TEAM_CADET = DarkRP.createJob("Clone Cadet", {
   color = Color(182, 182, 182, 255),
   model = {"models/player/asgclonewars/clone_cadet/clone_cadet.mdl"},
   description = [[You need to be trained to become a higher rank.]],
   weapons = {"keys"},
   command = "cadet",
   max = 0,
   salary = 0,
   admin = 0,
   vote = false,
   hasLicense = true,
   candemote = false,
   category = "Cadet",
   sortOrder = 100,
})
--[[Clones]]--
TEAM_CT = DarkRP.createJob("Clone Trooper", {
   color = Color(0, 56, 255, 255),
   model = {"models/player/trooper/cctrooper.mdl"},
   description = [[Clone Trooper Private | Congrats on passing the training!]],
   weapons = {"weapon_752_dc15a"},
   command = "clonetrooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "clonetrooper" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Trooper") end,
   category = "Clone Trooper",
   sortOrder = 2,
   PlayerSpawn = function(ply)
   ply:SetHealth(500)
end	
})
TEAM_CT = DarkRP.createJob("Clone Trooper Sergant", {
   color = Color(0, 56, 255, 255),
   model = {"models/player/testp2c/cgi ctp2.mdl"},
   description = [[You are a clonetrooper sergant! Congrats on the promotion!]],
   weapons = {"weapon_752_dc15a"},
   command = "clonetrooper-sergant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "clonetrooper-sergant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Trooper Sergant") end,
   category = "Clone Trooper",
   sortOrder = 2,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_CTP = DarkRP.createJob("Clone Trooper Pilot", {
   color = Color(0, 56, 255, 255),
   model = {"models/player/bst/bst.mdl"},
   description = [[Clone Trooper Pilot]],
   weapons = {"weapon_752_dc15a","weapon_752_dc17"},
   command = "clonetrooper-pilot",
   max = 5,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "clonetrooper-pilot" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Trooper Pilot") end,
   category = "Clone Trooper",
   sortOrder = 7,
   PlayerSpawn = function(ply)
   ply:SetHealth(400)
   end	
})
TEAM_CT = DarkRP.createJob("Clone Trooper Lieutnant", {
   color = Color(0, 56, 255, 255),
   model = {"models/player/testp2c/cgi ctp2.mdl"},
   description = [[You are a clonetrooper lieutnant! Congrats on the promotion!]],
   weapons = {"weapon_752_dc15a"},
   command = "clonetrooper-lieutnant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "clonetrooper-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Trooper Lieutnant") end,
   category = "Clone Trooper",
   sortOrder = 2,
    PlayerSpawn = function(ply)
    ply:SetHealth(750)
	end
})
TEAM_CT = DarkRP.createJob("Clone Trooper Captain", {
   color = Color(0, 56, 255, 255),
   model = {"models/player/testp2c/cgi ctp2.mdl"},
   description = [[You are a clonetrooper captain! Congrats on the promotion!]],
   weapons = {"weapon_752_dc15a"},
   command = "clonetrooper-captain",
   max = 5,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "clonetrooper-captain" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Trooper Captain") end,
   category = "Clone Trooper",
   sortOrder = 2,
    PlayerSpawn = function(ply)
    ply:SetHealth(750)
	end
})
TEAM_CT = DarkRP.createJob("Clone Trooper XO", {
   color = Color(0, 56, 255, 255),
   model = {"models/player/testp2c/cgi ctp2.mdl"},
   description = [[You are a clonetrooper xo! Congrats on the promotion!]],
   weapons = {"weapon_752_dc15a"},
   command = "clonetrooper-xo",
   max = 5,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "clonetrooper-xo" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Trooper XO") end,
   category = "Clone Trooper",
   sortOrder = 2,
    PlayerSpawn = function(ply)
    ply:SetHealth(800)
	end
})
TEAM_CT = DarkRP.createJob("Clone Trooper Commander", {
   color = Color(0, 56, 255, 255),
   model = {"models/player/stew/stew.mdl"},
   description = [[You are the Clone Trooper Commander! Youorder your troopers!]],
   weapons = {"weapon_752_dc15a","weapon_752bf3_binoculars","weapon_752_dc17dual"},
   command = "clonetrooper-commander",
   max = 1,
   salary = 60,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "clonetrooper-commander" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Trooper Commander") end,
   category = "Clone Trooper",
   sortOrder = 2,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_CG = DarkRP.createJob("Clone Guard Trooper", {
   color = Color(200, 55, 76, 255),
   model = {"models/player/sgg/starwars/clonetrooper_thire.mdl"},
   description = [[You are a Clone Guard Trooper | Congrats on passing the tryouts!]],
   weapons = {"weapon_752_dc15a"},
   command = "cloneguard",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "cloneguard" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Guard Trooper") end,
   category = "Clone Guard",
   sortOrder = 2,
   PlayerSpawn = function(ply)
   ply:SetHealth(500)
end	
})
TEAM_CG = DarkRP.createJob("Clone Guard Sergant", {
   color = Color(200, 55, 76, 255),
   model = {"models/player/sgg/starwars/clonetrooper_thire.mdl"},
   description = [[You are a Clone Guard Sergant | Congrats on the promotion!]],
   weapons = {"weapon_752_dc15a"},
   command = "cloneguard-sergant",
   max = 10,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "cloneguard-sergant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Guard Sergant") end,
   category = "Clone Guard",
   sortOrder = 2,
   PlayerSpawn = function(ply)
   ply:SetHealth(500)
end	
})
TEAM_CG = DarkRP.createJob("Clone Guard Lieutnant", {
   color = Color(200, 55, 76, 255),
   model = {"models/player/sgg/starwars/clonetrooper_thire.mdl"},
   description = [[You are a Clone Guard Sergant | Congrats on the promotion!]],
   weapons = {"weapon_752_dc15a"},
   command = "cloneguard-lieutnant",
   max = 10,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "cloneguard-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Guard Lieutnant") end,
   category = "Clone Guard",
   sortOrder = 2,
   PlayerSpawn = function(ply)
   ply:SetHealth(500)
end	
})
TEAM_CG = DarkRP.createJob("Clone Guard Captain", {
   color = Color(200, 55, 76, 255),
   model = {"models/player/sgg/starwars/clonetrooper_thire.mdl"},
   description = [[You are a Clone Guard Captain | Congrats on the promotion!]],
   weapons = {"weapon_752_dc15a"},
   command = "cloneguard-captain",
   max = 10,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "cloneguard-captain" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Guard Captain") end,
   category = "Clone Guard",
   sortOrder = 2,
   PlayerSpawn = function(ply)
   ply:SetHealth(650)
end	
})
TEAM_CG = DarkRP.createJob("Clone Guard XO", {
   color = Color(200, 55, 76, 255),
   model = {"models/player/sgg/starwars/clonetrooper_thire.mdl"},
   description = [[You are a Clone Guard XO | Congrats on the promotion!]],
   weapons = {"weapon_752_dc15a"},
   command = "cloneguard-xo",
   max = 10,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "cloneguard-xo" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Guard XO") end,
   category = "Clone Guard",
   sortOrder = 2,
   PlayerSpawn = function(ply)
   ply:SetHealth(650)
end	
})
TEAM_CG = DarkRP.createJob("Clone Guard Commander", {
   color = Color(200, 55, 76, 255),
   model = {"models/player/stooge/stooge.mdl"},
   description = [[You are the Clone Guard Commander | You order the troopers!]],
   weapons = {"weapon_752_dc15a"},
   command = "cloneguard-commander",
   max = 2,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "cloneguard-commander" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Clone Guard Commander") end,
   category = "Clone Guard",
   sortOrder = 2,
   PlayerSpawn = function(ply)
   ply:SetHealth(1000)
end	
})
TEAM_101st = DarkRP.createJob("101st Medic Trooper", {
   color = Color(242, 177, 79, 255),
   model = {"models/player/dyna/dyna.mdl"},
   description = [[You are a 101st Advanced Medic Trooper | Welcome to the 101st!]],
   weapons = {"weapon_752_dc15a","health_injection"},
   command = "101st-trooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "101st-trooper" or ply:IsSuperAdmin()  end,
   category = "101st",
   sortOrder = 3,
   PlayerSpawn = function(ply)
   ply:SetHealth(300)
end	
})
TEAM_101st = DarkRP.createJob("101st Advanced Medic Trooper", {
   color = Color(242, 177, 79, 255),
   model = {"models/player/veco/veco.mdl"},
   description = [[You are a 101st Advanced Medic Trooper! | Congrats on the promotion!]],
   weapons = {"weapon_752_dc15a","health_injection"},
   command = "101st-advanced-trooper",
   max = 10,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "101st-advanced-trooper" or ply:IsSuperAdmin()  end,
   category = "101st",
   sortOrder = 3,
   PlayerSpawn = function(ply)
   ply:SetHealth(300)
end	
})
TEAM_101st = DarkRP.createJob("101st Elite Medic Trooper", {
   color = Color(242, 177, 79, 255),
   model = {"models/player/moose/moose.mdl"},
   description = [[You are a 101st Elite Medic Trooper | Congrats on the promotion!]],
   weapons = {"weapon_752_dc15a","macrobinoculars","health_injection"},
   command = "101st-elite-trooper",
   max = 2,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "101st-elite-trooper" or ply:IsSuperAdmin()  end,
   category = "101st",
   sortOrder = 3,
   PlayerSpawn = function(ply)
   ply:SetHealth(300)
end	
})
TEAM_187th = DarkRP.createJob("187th Trooper", {
   color = Color(139, 87, 191, 255),
   model = {"models/player/asgclonewars/clonetrooper_187th/clonetrooper_187th.mdl"},
   description = [[You are the 187th trooper! Congrats on passing the tryouts!]],
   weapons = {"weapon_752_dc15a"},
   command = "187th-trooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "187th-trooper" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"187th Trooper") end,
   category = "187th",
   sortOrder = 9,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_187th = DarkRP.createJob("187th Sergant", {
   color = Color(139, 87, 191, 255),
   model = {"models/player/asgclonewars/trooper_187th_para/clonetrooper_187th_para.mdl"},
   description = [[You are the 187th Sergant!]],
   weapons = {"weapon_752_dc15a"},
   command = "187th-sergant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "187th-sergant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"187th Sergant") end,
   category = "187th",
   sortOrder = 9,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_187th = DarkRP.createJob("187th Lieutnant", {
   color = Color(139, 87, 191, 255),
   model = {"models/player/asgclonewars/trooper_187th_para/clonetrooper_187th_para.mdl"},
   description = [[You are the 187th Lieutnant!]],
   weapons = {"weapon_752_dc15a"},
   command = "187th-lieutnant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "187th-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"187th Lieutnant") end,
   category = "187th",
   sortOrder = 9,
    PlayerSpawn = function(ply)
    ply:SetHealth(750)
	end
})
TEAM_187th = DarkRP.createJob("187th Captain", {
   color = Color(139, 87, 191, 255),
   model = {"models/player/asgclonewars/trooper_187th_para/clonetrooper_187th_para.mdl"},
   description = [[You are the 187th Captain!]],
   weapons = {"weapon_752_dc15a"},
   command = "187th-captain",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "187th-captain" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"187th Captain") end,
   category = "187th",
   sortOrder = 9,
    PlayerSpawn = function(ply)
    ply:SetHealth(750)
	end
})
TEAM_187th = DarkRP.createJob("187th XO", {
   color = Color(139, 87, 191, 255),
   model = {"models/player/asgclonewars/trooper_187th_para/clonetrooper_187th_para.mdl"},
   description = [[You are the 187th Captain!]],
   weapons = {"weapon_752_dc15a"},
   command = "187th-xo",
   max = 5,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "187th-xo" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"187th XO") end,
   category = "187th",
   sortOrder = 9,
    PlayerSpawn = function(ply)
    ply:SetHealth(800)
	end
})
TEAM_187th = DarkRP.createJob("187th Commander Deviss", {
   color = Color(139, 87, 191, 255),
   model = {"models/player/187commander/assassinv3.mdl"},
   description = [[You are the 187th Commander!]],
   weapons = {"weapon_752_dc15a","weapon_752_dc17dual","macrobinoculars"},
   command = "187th-commander",
   max = 1,
   salary = 60,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "187th-commander" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"187th Commander Deviss") end,
   category = "187th",
   sortOrder = 9,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_212th = DarkRP.createJob("212th Trooper", {
   color = Color(183, 132, 1, 255),
   model = {"models/player/212th/c212th trooper.mdl"},
   description = [[212th Trooper | Welcome to the 212th!]],
   weapons = {"weapon_752_dc15a"},
   command = "212th-trooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "212th-trooper" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"212th Trooper") end,
   category = "212th",
   sortOrder = 3,
   PlayerSpawn = function(ply)
   ply:SetHealth(500)
end	
})
TEAM_212th = DarkRP.createJob("212th Sergant", {
   color = Color(183, 132, 1, 255),
   model = {"models/player/goco/goco.mdl"},
   description = [[You are a 212th Sergant]],
   weapons = {"weapon_752_dc15a","weapon_752_e60r"},
   command = "212th-sergant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "212th-sergant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"212th Sergant") end,
   category = "212th",
   sortOrder = 3,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_212th = DarkRP.createJob("212th Lieutnant", {
   color = Color(183, 132, 1, 255),
   model = {"models/player/goco/goco.mdl"},
   description = [[You are a 212th Lieutnant]],
   weapons = {"weapon_752_dc15a","weapon_752_e60r"},
   command = "212th-lieutnant",
   max = 10,
   salary = 50,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "212th-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"212th Lieutnant") end,
   category = "212th",
   sortOrder = 3,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_212th = DarkRP.createJob("212th Captain", {
   color = Color(183, 132, 1, 255),
   model = {"models/player/sokol/sokol.mdl"},
   description = [[You are a 212th Captain]],
   weapons = {"weapon_752_dc15a","weapon_752_e60r"},
   command = "212th-captain",
   max = 10,
   salary = 55,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "212th-captain" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"212th Captain") end,
   category = "212th",
   sortOrder = 3,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_212th = DarkRP.createJob("212th XO", {
   color = Color(183, 132, 1, 255),
   model = {"models/player/sokol/sokol.mdl"},
   description = [[You are a 212th XO]],
   weapons = {"weapon_752_dc15a","weapon_752_e60r"},
   command = "212th-xo",
   max = 2,
   salary = 55,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "212th-xo" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"212th XO") end,
   category = "212th",
   sortOrder = 3,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_212th = DarkRP.createJob("212th Commander Cody", {
   color = Color(183, 132, 1, 255),
   model = {"models/player/testccc/ccody.mdl"},
   description = [[You are the 212th Commander! Youorder your troopers]],
   weapons = {"weapon_752_dc15a","weapon_752_dc17dual","macrobinoculars","weapon_752_e60r"},
   command = "212th-commander",
   max = 1,
   salary = 60,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "212th-commander" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"212th Commander Cody") end,
   category = "212th",
   sortOrder = 3,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})

TEAM_327th = DarkRP.createJob("327th Trooper", {
   color = Color(173, 175, 35, 255),
   model = {"models/player/327th/c327tht.mdl"},
   description = [[You are the 327th trooper! Congrats on passing the tryouts!]],
   weapons = {"weapon_752_dc15sa","weapon_752_dc15a"},
   command = "327th-trooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "327th-trooper" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"327th Trooper") end,
   category = "327th",
   sortOrder = 4,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_327th = DarkRP.createJob("327th Sergant", {
   color = Color(173, 175, 35, 255),
   model = {"models/player/327th/c327tht.mdl"},
   description = [[You are the 327th Sergant!]],
   weapons = {"weapon_752_dc15sa","weapon_752_dc17m_br"},
   command = "327th-sergant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "327th-sergant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"327th Sergant") end,
   category = "327th",
   sortOrder = 4,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_327th = DarkRP.createJob("327th Lieutnant", {
   color = Color(173, 175, 35, 255),
   model = {"models/player/327thlt/c327th lt.mdl"},
   description = [[You are the 327th Lieutnant!]],
   weapons = {"weapon_752_dc15sa","weapon_752_dc17m_br"},
   command = "327th-lieutnant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "327th-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"327th Lieutnant") end,
   category = "327th",
   sortOrder = 4,
    PlayerSpawn = function(ply)
    ply:SetHealth(700)
	end
})
TEAM_327th = DarkRP.createJob("327th Captain", {
   color = Color(173, 175, 35, 255),
   model = {"models/player/327thlt/c327th lt.mdl"},
   description = [[You are the 327th Captain!]],
   weapons = {"weapon_752_dc15sa","weapon_752_dc17m_br"},
   command = "327th-captain",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "327th-captain" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"327th Captain") end,
   category = "327th",
   sortOrder = 4,
    PlayerSpawn = function(ply)
    ply:SetHealth(750)
	end
})
TEAM_327th = DarkRP.createJob("327th XO", {
   color = Color(173, 175, 35, 255),
   model = {"models/player/327thlt/c327th lt.mdl"},
   description = [[You are the 327th XO!]],
   weapons = {"weapon_752_dc15sa","weapon_752_dc17m_br"},
   command = "327th-xo",
   max = 2,
   salary = 55,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "327th-xo" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"327th XO") end,
   category = "327th",
   sortOrder = 4,
    PlayerSpawn = function(ply)
    ply:SetHealth(800)
	end
})
TEAM_327th = DarkRP.createJob("327th Commander Bly", {
   color = Color(173, 175, 35, 255),
   model = {"models/player/bly/cbly.mdl"},
   description = [[You are the 327th Commander!]],
   weapons = {"weapon_752_dc17dual","weapon_752_dc17m_br","macrobinoculars"},
   command = "327th-commander",
   max = 1,
   salary = 60,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "327th-commander" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"327th Commander Bly") end,
   category = "327th",
   sortOrder = 4,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_501ST = DarkRP.createJob("501st Trooper", {
   color = Color(133, 229, 242, 255),
   model = {"models/player/501st/c501st.mdl"},
   description = [[You are a 501st trooper! Congrats on passing the tryouts!]],
   weapons = {"weapon_752_dc17","weapon_752_dc15a"},
   command = "501st-trooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "501st-trooper" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"501st Trooper") end,
   category = "501st",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_501ST = DarkRP.createJob("501st Sergant", {
   color = Color(133, 229, 242, 255),
   model = {"models/player/501stlt/c501stlt.mdl"},
   description = [[You are a 501st Sergant!]],
   weapons = {"weapon_752_dc17","weapon_752_dc15a"},
   command = "501st-sergant",
   max = 0,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "501st-sergant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"501st Sergant") end,
   category = "501st",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_501ST = DarkRP.createJob("501st Lieutnant", {
   color = Color(133, 229, 242, 255),
   model = {"models/player/kano/kano.mdl"},
   description = [[You are a 501st Lieutnant!]],
   weapons = {"weapon_752_dc17","weapon_752_dc15a"},
   command = "501st-lieutnant",
   max = 0,
   salary = 45,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "501st-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"501st Lieutnant") end,
   category = "501st",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_501ST = DarkRP.createJob("501st Captain", {
   color = Color(133, 229, 242, 255),
   model = {"models/player/test/rex.mdl"},
   description = [[You are the 501st Captain!]],
   weapons = {"weapon_752_dc17","weapon_752_dc15a","macrobinoculars"},
   command = "501st-captain",
   max = 10,
   salary = 60,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "501st-captain" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"501st Captain") end,
   category = "501st",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_501ST = DarkRP.createJob("501st XO", {
   color = Color(133, 229, 242, 255),
   model = {"models/player/test/rex.mdl"},
   description = [[You are the 501st XO!]],
   weapons = {"weapon_752_dc17","weapon_752_dc15a","macrobinoculars"},
   command = "501st-xo",
   max = 10,
   salary = 60,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "501st-xo" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"501st XO") end,
   category = "501st",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_501ST = DarkRP.createJob("501st Commander", {
   color = Color(133, 229, 242, 255),
   model = {"models/player/hunter2/hunter2.mdl"},
   description = [[You are the 501st Commander!]],
   weapons = {"weapon_752_dc17dual","weapon_752_dc15a","macrobinoculars"},
   command = "501st-commander",
   max = 2,
   salary = 60,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "501st-commander" or ply:GetNWString("usergroup") == "trial-moderator" or ply:GetNWString("usergroup") == "moderator" or ply:IsAdmin() or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"501st Commander") end,
   category = "501st",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_RSF = DarkRP.createJob("RSF Trooper",{
   color = Color(0, 94, 255, 255),
   model = {"models/player/tcg/starwars/shadow/shadowtrooper.mdl"},
   description = [[You are a RSF Trooper! Congrats on passing the tryouts!]],
   weapons = {"weapon_752_dc15a","weapon_752_de10","weapon_camo"},
   command = "rsf-trooper",
   max = 0,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "rsf-trooper" or ply:IsSuperAdmin()  end,
   category = "RSF",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(300)
	end
})
TEAM_RSF = DarkRP.createJob("RSF Sergeant",{
   color = Color(0, 94, 255, 255),
   model = {"models/player/tcg/starwars/shadow/shadowtrooper.mdl"},
   description = [[You are a RSF Sergeant!]],
   weapons = {"weapon_752_dc15a","weapon_752_de10","weapon_camo"},
   command = "rsf-sergeant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "rsf-sergeant" or ply:IsSuperAdmin()  end,
   category = "RSF",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(650)
	end
})
TEAM_RSF = DarkRP.createJob("RSF Commander",{
   color = Color(0, 94, 255, 255),
   model = {"models/player/tcg/starwars/shadow/captain/shadowcaptain.mdl"},
   description = [[You are a RSF Sergeant!]],
   weapons = {"weapon_752_dc15a","weapon_752_de10","weapon_camo"},
   command = "rsf-commander",
   max = 2,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "rsf-commander" or ply:IsSuperAdmin()  end,
   category = "RSF",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_WP = DarkRP.createJob("Wolf Pack Trooper", {
   color = Color(158, 156, 156, 255),
   model = {"models/wpclonetrooper.mdl"},
   description = [[You are a Wolf Pack Trooper | Congrats on passing the tryouts!]],
   weapons = {"weapon_752_dc15a","realistic_hook","riot_shield"},
   command = "wolf-pack-trooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "wolf-pack-trooper" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Wolf Pack Trooper") end,
   category = "Wolf Pack",
   sortOrder = 5,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_WP = DarkRP.createJob("Wolf Pack Sergant", {
   color = Color(158, 156, 156, 255),
   model = {"models/wpclonetrooper.mdl"},
   description = [[You are a Wolf Pack Sergant!]],
   weapons = {"weapon_752_dc15a","realistic_hook","riot_shield"},
   command = "wolf-pack-sergant",
   max = 0,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "wolf-pack-sergant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Wolf Pack Sergant") end,
   category = "Wolf Pack",
   sortOrder = 5,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_WP = DarkRP.createJob("Wolf Pack Lieutnant", {
   color = Color(158, 156, 156, 255),
   model = {"models/wpclonetrooper2.mdl"},
   description = [[You are a Wolf Pack Lieutnant!]],
   weapons = {"weapon_752_dc15a","realistic_hook","riot_shield"},
   command = "wolf-pack-lieutnant",
   max = 0,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "wolf-pack-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Wolf Pack Lieutnant") end,
   category = "Wolf Pack",
   sortOrder = 5,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_WP = DarkRP.createJob("Wolf Pack Captain", {
   color = Color(158, 156, 156, 255),
   model = {"models/wpclonetrooper2.mdl"},
   description = [[You are a Wolf Pack Captain!]],
   weapons = {"weapon_752_dc15a","realistic_hook","riot_shield"},
   command = "wolf-pack-captain",
   max = 0,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "wolf-pack-captain" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Wolf Pack Captain") end,
   category = "Wolf Pack",
   sortOrder = 5,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_WP = DarkRP.createJob("Wolf Pack XO", {
   color = Color(158, 156, 156, 255),
   model = {"models/wpclonetrooper2.mdl"},
   description = [[You are a Wolf Pack XO!]],
   weapons = {"weapon_752_dc15a","realistic_hook","riot_shield"},
   command = "wolf-pack-xo",
   max = 0,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "wolf-pack-xo" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Wolf Pack XO") end,
   category = "Wolf Pack",
   sortOrder = 5,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_WP = DarkRP.createJob("Wolf Pack Commander Wolffe", {
   color = Color(158, 156, 156, 255),
   model = {"models/player/wolffe/ccgi wolffe.mdl"},
   description = [[You are a Wolf Pack Commander Wolffe! Yourorder your troopers!]],
   weapons = {"weapon_752_dc15a","weapon_752_dc17dual","realistic_hook","riot_shield","macrobinoculars"},
   command = "wolf-pack-commander",
   max = 1,
   salary = 60,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "wolf-pack-commander" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Wolf Pack Commander Wolffe") end,
   category = "Wolf Pack",
   sortOrder = 5,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_GC = DarkRP.createJob("Green Company Trooper", {
   color = Color(5, 252, 0, 255),
   model = {"models/player/tcg/starwars/green/greentrooper.mdl"},
   description = [[Green Company Trooper]],
   weapons = {"weapon_752_dc15a","weapon_lasermgun"},
   command = "green-company-trooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "green-company-trooper" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Green Company Trooper") end,
   category = "Green Company",
   sortOrder = 6,
   PlayerSpawn = function(ply)
   ply:SetHealth(500)
   end	
})
TEAM_GC = DarkRP.createJob("Green Company Scout Unit", {
   color = Color(5, 252, 0, 255),
   model = {"models/player/41a/41a.mdl"},
   description = [[Green Company Trooper]],
   weapons = {"weapon_752_dc15sa","weapon_752_dc17m_sn",},
   command = "green-company-scout",
   max = 10,
   salary = 10,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "green-company-scout" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Green Company Trooper") end,
   category = "Green Company",
   sortOrder = 6,
   PlayerSpawn = function(ply)
   ply:SetHealth(500)
   end	
})
TEAM_GC = DarkRP.createJob("Green Company Sergant", {
   color = Color(5, 252, 0, 255),
   model = {"models/player/tcg/starwars/green/greentrooper.mdl"},
   description = [[Green Company SGT]],
   weapons = {"weapon_752_dc15a","weapon_lasermgun"},
   command = "green-company-sergant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "green-company-sergant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Green Company Sergant") end,
   category = "Green Company",
   sortOrder = 6,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_GC = DarkRP.createJob("Green Company Lieutnant", {
   color = Color(5, 252, 0, 255),
   model = {"models/player/tcg/starwars/green/greentrooper.mdl"},
   description = [[Green Company LT]],
   weapons = {"weapon_752_dc15a","weapon_lasermgun"},
   command = "green-company-lieutnant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "green-company-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Green Company Lieutnant") end,
   category = "Green Company",
   sortOrder = 6,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_GC = DarkRP.createJob("Green Company Captain", {
   color = Color(5, 252, 0, 255),
   model = {"models/player/tcg/starwars/green/captain/greencaptain.mdl"},
   description = [[Green Company CPT]],
   weapons = {"weapon_752_dc15a","weapon_lasermgun"},
   command = "green-company-captain",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "green-company-captain" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Green Company Captain") end,
   category = "Green Company",
   sortOrder = 6,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_GC = DarkRP.createJob("Green Company XO", {
   color = Color(5, 252, 0, 255),
   model = {"models/player/41stlt/c41stlt.mdl"},
   description = [[Green Company XO]],
   weapons = {"weapon_752_dc15a","weapon_lasermgun"},
   command = "green-company-xo",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "green-company-xo" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Green Company XO") end,
   category = "Green Company",
   sortOrder = 6,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_GC = DarkRP.createJob("Green Company Commander Gree", {
   color = Color(5, 252, 0, 255),
   model = {"models/player/imok/imok.mdl"},
   description = [[Green Company Commander]],
   weapons = {"weapon_752_dc15a","weapon_752_dc17dual","weapon_minigun","macrobinoculars"},
   command = "green-company-commander",
   max = 1,
   salary = 60,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "green-company-commander" or ply:GetNWString("usergroup") == "Moderator" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Green Company Commander Gree") end,
   category = "Green Company",
   sortOrder = 6,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_GM = DarkRP.createJob("Galatic Marine Trooper", {
   color = Color(138, 33, 242, 255),
   model = {"models/player/tcg/starwars/gm/galacticmarine.mdl"},
   description = [[Galatic Marine Trooper]],
   weapons = {"weapon_572_ihr","weapon_752_dc17","weapon_752_dc17m_br"},
   command = "gm-trooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "gm-trooper" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Galatic Marine Trooper") end,
   category = "Galatic Marine",
   sortOrder = 8,
   PlayerSpawn = function(ply)
   ply:SetHealth(500)
   end	
})
TEAM_GM = DarkRP.createJob("Galatic Marine Sergant", {
   color = Color(138, 33, 242, 255),
   model = {"models/player/tcg/starwars/gm/galacticmarine.mdl"},
   description = [[Galatic Marine SGT]],
   weapons = {"weapon_572_ihr","weapon_752_dc17","weapon_752_dc17m_br"},
   command = "gm-sergant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "gm-sergant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Galatic Marine Sergant") end,
   category = "Galatic Marine",
   sortOrder = 8,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_GM = DarkRP.createJob("Galatic Marine Lieutnant", {
   color = Color(138, 33, 242, 255),
   model = {"models/player/tcg/starwars/gm/galacticmarine.mdl"},
   description = [[Galatic Marine LT]],
   weapons = {"weapon_572_ihr","weapon_752_dc17","weapon_752_dc17m_br"},
   command = "gm-lieutnant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "gm-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Galatic Marine Lieutnant") end,
   category = "Galatic Marine",
   sortOrder = 8,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_GM = DarkRP.createJob("Galatic Marine Captain", {
   color = Color(138, 33, 242, 255),
   model = {"models/player/tcg/starwars/gm/captain/gmcaptain.mdl"},
   description = [[Galatic Marine CPT]],
   weapons = {"weapon_572_ihr","weapon_752_dc17","weapon_752_dc17m_br"},
   command = "gm-captain",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "gm-captain" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Galatic Marine Captain") end,
   category = "Galatic Marine",
   sortOrder = 8,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_GM = DarkRP.createJob("Galatic Marine XO", {
   color = Color(138, 33, 242, 255),
   model = {"models/player/tcg/starwars/gm/captain/gmcaptain.mdl"},
   description = [[Galatic Marine CPT]],
   weapons = {"weapon_572_ihr","weapon_752_dc17","weapon_752_dc17m_br"},
   command = "gm-xo",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "gm-xo" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Galatic Marine XO") end,
   category = "Galatic Marine",
   sortOrder = 8,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_GM = DarkRP.createJob("Galatic Marine Commander Bacara", {
   color = Color(138, 33, 242, 255),
   model = {"models/player/tcg/starwars/gm/bacara/bacara.mdl"},
   description = [[You are the Galatic Marine Commander | You order your troopers!]],
   weapons = {"weapon_572_ihr","weapon_752_dc17dual","weapon_752_dc17m_br"},
   command = "gm-commander",
   max = 1,
   salary = 60,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "gm-commander" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Galatic Marine Commander Bacara") end,
   category = "Galatic Marine",
   sortOrder = 8,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_EOD = DarkRP.createJob("EOD Trooper", {
   color = Color(247, 203, 46, 255),
   model = {"models/player/teste/cgi eod.mdl"},
   description = [[You are the EOD trooper! Congrats on passing the tryouts!]],
   weapons = {"weapon_752_dc17"},
   command = "eod-trooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "eod-trooper" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"EOD Trooper") end,
   category = "EOD",
   sortOrder = 11,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_EOD = DarkRP.createJob("EOD Sergant", {
   color = Color(247, 203, 46, 255),
   model = {"models/player/teste/cgi eod.mdl"},
   description = [[You are the EOD Sergant!]],
   weapons = {"weapon_752_dc17"},
   command = "eod-sergant",
   max = 0,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "eod-sergant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"EOD Sergant") end,
   category = "EOD",
   sortOrder = 11,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_EOD = DarkRP.createJob("EOD Lieutnant", {
   color = Color(247, 203, 46, 255),
   model = {"models/player/teste/cgi eod.mdl"},
   description = [[You are the EOD Lieutnant!]],
   weapons = {"weapon_752_dc17"},
   command = "eod-lieutnant",
   max = 0,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "eod-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"EOD Lieutnant") end,
   category = "EOD",
   sortOrder = 11,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_EOD = DarkRP.createJob("EOD Captain", {
   color = Color(247, 203, 46, 255),
   model = {"models/player/teste/cgi eod.mdl"},
   description = [[You are the EOD Captain!]],
   weapons = {"weapon_752_dc17"},
   command = "eod-captain",
   max = 0,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "eod-captain" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"EOD Captain") end,
   category = "EOD",
   sortOrder = 11,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_EOD = DarkRP.createJob("EOD XO", {
   color = Color(247, 203, 46, 255),
   model = {"models/player/teste/cgi eod.mdl"},
   description = [[You are the EOD XO!]],
   weapons = {"weapon_752_dc17"},
   command = "eod-xo",
   max = 0,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "eod-xo" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"EOD XO") end,
   category = "EOD",
   sortOrder = 11,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
--[[models/player/asgclonewars/eod_trooper/eod_trooper.mdl - maybe LT+]]
TEAM_EOD = DarkRP.createJob("EOD Commander", {
   color = Color(247, 203, 46, 255),
   model = {"models/player/steel/steel.mdl"},
   description = [[You are the EOD Commander!]],
   weapons = {"weapon_752_dc17dual","macrobinoculars"},
   command = "eod-commander",
   max = 0,
   salary = 60,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "eod-commander" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"EOD Commander") end,
   category = "EOD",
   sortOrder = 11,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_ARF = DarkRP.createJob("Advanced Recon Forces Trooper", {
   color = Color(255, 107, 0, 255),
   model = {"models/player/212a/cgi212a.mdl"},
   description = [[You are a Advanced Recon Forces trooper! Congrats on passing the tryouts!]],
   weapons = {"weapon_752_dc17m_sn","gauss_rifle"},
   command = "advanced-recon-forces-trooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "arf-trooper" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Advanced Recon Forces Trooper") end,
   category = "Advanced Recon Forces",
   sortOrder = 13,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_ARF = DarkRP.createJob("Advanced Recon Forces Lieutnant", {
   color = Color(255, 107, 0, 255),
   model = {"models/player/carf/ccarf.mdl"},
   description = [[You are a Advanced Recon Forces Lieutnant!]],
   weapons = {"weapon_752_dc17m_sn","gauss_rifle"},
   command = "advanced-recon-forces-lieutnant",
   max = 10,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "arf-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Advanced Recon Forces Lieutnant") end,
   category = "Advanced Recon Forces",
   sortOrder = 13,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_ARF = DarkRP.createJob("Advanced Recon Forces Captain", {
   color = Color(255, 107, 0, 255),
   model = {"models/player/pat/pat.mdl"},
   description = [[You are a Advanced Recon Forces Captain!]],
   weapons = {"weapon_752_dc17m_sn","gauss_rifle"},
   command = "advanced-recon-forces-captain",
   max = 10,
   salary = 55,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "arf-captain" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Advanced Recon Forces Captain") end,
   category = "Advanced Recon Forces",
   sortOrder = 13,
    PlayerSpawn = function(ply)
    ply:SetHealth(750)
	end
})
TEAM_ARF = DarkRP.createJob("Advanced Recon Forces XO", {
   color = Color(255, 107, 0, 255),
   model = {"models/player/dansea/danseacb.mdl"},
   description = [[You are a Advanced Recon Forces XO!]],
   weapons = {"weapon_752_dc17m_sn","gauss_rifle"},
   command = "advanced-recon-forces-xo",
   max = 5,
   salary = 60,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "arf-xo" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Advanced Recon Forces XO") end,
   category = "Advanced Recon Forces",
   sortOrder = 13,
    PlayerSpawn = function(ply)
    ply:SetHealth(850)
	end
})
TEAM_ARF = DarkRP.createJob("Advanced Recon Forces Commander Trauma", {
   color = Color(255, 107, 0, 255),
   model = {"models/player/trauma/cctrauma.mdl"},
   description = [[You are the Advanced Recon Forces Commander!]],
   weapons = {"weapon_752_dc17m_sn","weapon_752_dc17dual","gauss_rifle","macrobinoculars"},
   command = "trauma",
   max = 1,
   salary = 65,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "arf-trauma" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Advanced Recon Forces Commander Trauma") end,
   category = "Advanced Recon Forces",
   sortOrder = 13,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_ARC = DarkRP.createJob("ARC Trooper", {
   color = Color(0, 196, 239, 255),
   model = {"models/player/barc/cgicbarc.mdl"},
   description = [[You are a ARC Trooper! Congrats on passing the tryouts!]],
   weapons = {"weapon_752_dc17","weapon_752_dc15a"},
   command = "arc-trooper",
   max = 0,
   salary = 10,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "arc-trooper" or ply:GetNWString("usergroup") == "donator" or ply:GetNWString("usergroup") == "trial-moderator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"ARC Trooper") end,
   category = "ARC",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_ARC = DarkRP.createJob("ARC Sergant", {
   color = Color(0, 196, 239, 255),
   model = {"models/player/garc/garc.md"},
   description = [[You are a ARC Sergant! Congrats on the promotion!]],
   weapons = {"weapon_752_dc17","weapon_752_dc15a"},
   command = "arc-sergant",
   max = 10,
   salary = 10,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "arc-sergant" or ply:GetNWString("usergroup") == "donator" or ply:GetNWString("usergroup") == "trial-moderator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"ARC Sergant") end,
   category = "ARC",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_ARC = DarkRP.createJob("ARC Lieutnant", {
   color = Color(0, 196, 239, 255),
   model = {"models/player/rarc/cgirarc.mdl"},
   description = [[You are a ARC Lieutnant! Congrats on the promotion!]],
   weapons = {"weapon_752_dc17","weapon_752_dc15a"},
   command = "arc-lieutnant",
   max = 10,
   salary = 10,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "arc-lieutnant" or ply:GetNWString("usergroup") == "donator" or ply:GetNWString("usergroup") == "trial-moderator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"ARC Lieutnant") end,
   category = "ARC",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_ARC = DarkRP.createJob("ARC Captain", {
   color = Color(0, 196, 239, 255),
   model = {"models/player/echo/echo.mdl"},
   description = [[You are a ARC Captain! Congrats on the promotion!]],
   weapons = {"weapon_752_dc17","weapon_752_dc15a"},
   command = "arc-captain",
   max = 10,
   salary = 10,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "arc-captain" or ply:GetNWString("usergroup") == "donator" or ply:GetNWString("usergroup") == "trial-moderator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"ARC Captain") end,
   category = "ARC",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_ARC = DarkRP.createJob("ARC XO", {
   color = Color(0, 196, 239, 255),
   model = {"models/player/fives/fives.mdl"},
   description = [[You are a ARC XO! Congrats on the promotion!]],
   weapons = {"weapon_752_dc17","weapon_752_dc15a"},
   command = "arc-xo",
   max = 10,
   salary = 10,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "arc-xo" or ply:GetNWString("usergroup") == "donator" or ply:GetNWString("usergroup") == "trial-moderator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"ARC XO") end,
   category = "ARC",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_ARC = DarkRP.createJob("ARC Commander", {
   color = Color(0, 196, 239, 255),
   model = {"models/player/yarc/cgicyarc.mdl"},
   description = [[You are the ARC Commander! You order the troopers!]],
   weapons = {"weapon_752_dc17","weapon_752_dc15a"},
   command = "arc-commander",
   max = 1,
   salary = 10,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "arc-commander" or ply:GetNWString("usergroup") == "trial-moderator" or ply:GetNWString("usergroup") == "moderator" or ply:IsAdmin() or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"ARC Commander") end,
   category = "ARC",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_DS = DarkRP.createJob("Delta Squad Sev", {
   color = Color(0, 94, 255, 255),
   model = {"models/player/sgg/starwars/clone_commando_07.mdl"},
   description = [[You are Delta Squad Sev!]],
   weapons = {"weapon_752_dc17","weapon_752_dc17m_br"},
   command = "ds-sev",
   max = 1,
   salary = 15,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "ds-sev" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Delta Squad Sev") end,
   category = "Delta Squad",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(1500)
	end
})
TEAM_DS = DarkRP.createJob("Delta Squad Fixer", {
   color = Color(0, 94, 255, 255),
   model = {"models/player/sgg/starwars/clone_commando_40.mdl"},
   description = [[You are Delta Squad Fixer!]],
   weapons = {"weapon_752_dc17","weapon_752_dc17m_br"},
   command = "ds-fixer",
   max = 1,
   salary = 25,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "ds-fixer" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Delta Squad Fixer") end,
   category = "Delta Squad",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(1500)
	end
})
TEAM_DS = DarkRP.createJob("Delta Squad Scorch", {
   color = Color(0, 94, 255, 255),
   model = {"models/player/sgg/starwars/clone_commando_62.mdl"},
   description = [[You are Delta Squad Scorch!]],
   weapons = {"weapon_752_dc17","weapon_752_dc17m_br","weapon_avpflamer"},
   command = "ds-scorch",
   max = 1,
   salary = 35,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "ds-scorch" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Delta Squad Scorch") end,
   category = "Delta Squad",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(1500)
	end
})
TEAM_DS = DarkRP.createJob("Delta Squad Commander Boss", {
   color = Color(0, 94, 255, 255),
   model = {"models/player/sgg/starwars/clone_commando_38.mdl"},
   description = [[You are Delta Squad Commander Boss!]],
   weapons = {"weapon_752_dc17","weapon_752_dc17m_br","weapon_swrc_det"},
   command = "ds-boss",
   max = 1,
   salary = 45,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "ds-boss" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Delta Squad Commander Boss") end,
   category = "Delta Squad",
   sortOrder = 14,
    PlayerSpawn = function(ply)
    ply:SetHealth(2000)
	end
})
--[[Fleet]]--
TEAM_FLEET = DarkRP.createJob("Fleet Ensign", {
   color = Color(102, 102, 102, 255),
   model = {"models/player/donut/donut.mdl"},
   description = [[You are a fleet, you help in the control room]],
   weapons = {"weapon_752_dc17"},
   command = "fleet-ensign",
   max = 0,
   salary = 100,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "fleet-ensign" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Fleet Ensign") end,
   category = "Fleet",
   sortOrder = 68,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_FLEET = DarkRP.createJob("Fleet Captain", {
   color = Color(102, 102, 102, 255),
   model = {"models/player/donut/donut.mdl"},
   description = [[You are a fleet, you help in the control room]],
   weapons = {"weapon_752_dc17"},
   command = "fleet-cpt",
   max = 10,
   salary = 500,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "fleet-captain" or ply:GetNWString("usergroup") == "donator" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Fleet Captain") end,
   category = "Fleet",
   sortOrder = 68,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_FLEET = DarkRP.createJob("Fleet Commander", {
   color = Color(102, 102, 102, 255),
   model = {"models/player/donut/donut.mdl"},
   description = [[You are a fleet, you help in the control room]],
   weapons = {"weapon_752_dc17"},
   command = "fleet-commander",
   max = 10,
   salary = 500,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "fleet-commander" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Fleet Commander") end,
   category = "Fleet",
   sortOrder = 68,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_FLEET = DarkRP.createJob("Fleet Admiral", {
   color = Color(102, 102, 102, 255),
   model = {"models/player/donut/donut.mdl"},
   description = [[You are a fleet, you help in the control room]],
   weapons = {"weapon_752_dc17"},
   command = "fleet-admiral",
   max = 2,
   salary = 500,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "fleet-admiral" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Fleet Admiral") end,
   category = "Fleet",
   sortOrder = 68,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
TEAM_FLEET = DarkRP.createJob("Fleet Vice Admiral", {
   color = Color(102, 102, 102, 255),
   model = {"models/player/scifi_bill.mdl"},
   description = [[You are a fleet, you help in the control room]],
   weapons = {"weapon_752_dc17"},
   command = "fleet-vice-admiral",
   max = 2,
   salary = 500,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "fleet-vice-admiral" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Fleet Vice Admiral") end,
   category = "Fleet",
   sortOrder = 68,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
    ply:SetSkin(2)
	end
    
})
TEAM_FLEET = DarkRP.createJob("Grand Admiral", {
   color = Color(102, 102, 102, 255),
   model = {"models/player/scifi_bill.mdl"},
   description = [[You are a fleet, you help in the control room]],
   weapons = {"weapon_752_dc17"},
   command = "grand-admiral",
   max = 1,
   salary = 10000,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "grand-admiral" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Grand Admiral") end,
   category = "Fleet",
   sortOrder = 68,
    PlayerSpawn = function(ply)
    ply:SetHealth(1000)
	end
})
--[[Jedis]]--
TEAM_JEDI = DarkRP.createJob("Aayla Secura", {
color = Color(227, 169, 232, 255),
model = {"models/player/nav/aayla.mdl"},
description = [[You are Aayla Secura.]],
weapons = {"weapon_lightsaber"},
command = "aaylasecura",
max = 1,
salary = 100,
admin = 0,
vote = false,
candemote = false,
customCheck = function(ply) return ply:GetNWString("usergroup") == "aaylasecura" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Aayla Secura") end,
modelScale = 1,
category = "Hero Jobs",
sortOrder = 15,PlayerSpawn = function(ply)
ply:SetHealth(3500)
end
})
TEAM_JEDI = DarkRP.createJob("Ki Adi Mundi", {
color = Color(227, 169, 232, 255),
model = {"models/player/nav/mundi.mdl"},
description = [[You are the one and only Ki Adi Mundi]],
weapons = {"weapon_lightsaber"},
command = "kiadimundi",
max = 1,
salary = 100,
admin = 0,
vote = false,

candemote = false,
customCheck = function(ply) return ply:GetNWString("usergroup") == "kiadimundi" or  ply:IsSuperAdmin() or PlychangeAllowed(ply,"Ki Adi Mundi")  end,
modelScale = 1,
category = "Hero Jobs",
sortOrder = 15,
PlayerSpawn = function(ply)
ply:SetHealth(3500)
end
})
TEAM_JEDI = DarkRP.createJob("Kit Fisto", {
color = Color(227, 169, 232, 255),
model = {"models/player/nav/kitfisto.mdl"},
description = [[You are the one and only Kit Fisto]],
weapons = {"weapon_lightsaber"},
command = "kitfisto",
max = 1,
salary = 100,
admin = 0,
vote = false,

candemote = false,
customCheck = function(ply) return ply:GetNWString("usergroup") == "kitfisto" or  ply:IsSuperAdmin() or PlychangeAllowed(ply,"Kit Fisto") end,
modelScale = 1,
category = "Hero Jobs",
sortOrder = 15,
PlayerSpawn = function(ply)
ply:SetHealth(3500)
end
})
TEAM_JEDI = DarkRP.createJob("Plo Koon", {
color = Color(227, 169, 232, 255),
model = {"models/player/plokoon/plokoon.mdl"},
description = [[You are the one and only Plo Koon]],
weapons = {"weapon_lightsaber"},
command = "plokoon",
max = 1,
salary = 100,
admin = 0,
vote = false,

candemote = false,
customCheck = function(ply) return ply:GetNWString("usergroup") == "plokoon" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Plo Koon") end,
modelScale = 1,
category = "Hero Jobs",
sortOrder = 15,
PlayerSpawn = function(ply)
ply:SetHealth(3500)
end
})
TEAM_JEDI = DarkRP.createJob("Mace Windu", {
color = Color(227, 169, 232, 255),
model = {"models/player/mace/mace.mdl"},
description = [[You are the one and only Mace Windu]],
weapons = {"weapon_lightsaber"},
command = "macewindu",
max = 1,
salary = 100,
admin = 0,
vote = false,

candemote = false,
customCheck = function(ply) return ply:GetNWString("usergroup") == "macewindu" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Mace Windu") end,
modelScale = 1,
category = "Hero Jobs",
sortOrder = 15,PlayerSpawn = function(ply)
ply:SetHealth(5000)
end
})

TEAM_JEDI = DarkRP.createJob("Anakin Skywalker", {
color = Color(227, 169, 232, 255),
model = {"models/kriegsyntax/sw_752/anakin_est.mdl"},
description = [[You are the one and only Anakin Skywalker]],
weapons = {"weapon_lightsaber"},
command = "anakinskywalker",
max = 1,
salary = 100,
admin = 0,
vote = false,

candemote = false,
customCheck = function(ply) return ply:GetNWString("usergroup") == "anakinskywalker" or ply:GetNWString("usergroup") == "donator" or ply:GetNWString("usergroup") == "trial-moderator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Anakin Skywalker") end,
modelScale = 1,
category = "Hero Jobs",
sortOrder = 15,
PlayerSpawn = function(ply)
ply:SetHealth(5000)
end
})

TEAM_JEDI = DarkRP.createJob("Obi Wan Kenobi", {
color = Color(227, 169, 232, 255),
model = {"models/player/generalkenobi/cgikenobi.mdl"},
description = [[You are Obi Wan Kenobi, Anakin Skywalker's master.]],
weapons = {"weapon_lightsaber"},
command = "obiwankenobi",
max = 1,
salary = 100,
admin = 0,
vote = false,

candemote = false,
customCheck = function(ply) return ply:GetNWString("usergroup") == "obiwankenobi" or ply:IsAdmin() or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Obi Wan Kenobi") end,
modelScale = 1,
category = "Hero Jobs",
sortOrder = 15,PlayerSpawn = function(ply)
ply:SetHealth(6500)
end
})
TEAM_JEDI = DarkRP.createJob("Grand Master Yoda", {
color = Color(227, 169, 232, 255),
model = {"models/hgn/swrp/swrp/jedi_yoda.mdl"},
description = [[You are grand master Yoda!]],
weapons = {"weapon_lightsaber"},
command = "yoda",
max = 1, 
salary = 100,
admin = 0,
vote = false,

candemote = false,
customCheck = function(ply) return ply:GetNWString("usergroup") == "yoda" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Grand Master Yoda")  end,
modelScale = 0.7,
category = "Hero Jobs",
sortOrder = 15,
PlayerSpawn = function(ply)
ply:SetHealth(8000)
end
})
TEAM_JEDI = DarkRP.createJob("Jedi Youngling", {
   color = Color(227, 169, 232, 255),
   model = {
	   "models/grealms/characters/padawan/padawan_01.mdl",
	   "models/grealms/characters/padawan/padawan_02.mdl",
           "models/grealms/characters/padawan/padawan_03.mdl",
           "models/grealms/characters/padawan/padawan_04.mdl",
           },
   description = [[You are a Jedi Youngling! Await your training to pass the first trials!]],
   weapons = {"weapon_lightsaber"},
   command = "jediyoung",
   max = 0,
   salary = 100,
   admin = 0,
   vote = false,
   candemote = true,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "jediyoungling" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Jedi Youngling") end,
   modelScale = 0.7,
   category = "Jedi",
   sortOrder = 15,
   PlayerSpawn = function(ply)
   ply:SetHealth(650)
   end
   })
TEAM_JEDI = DarkRP.createJob("Jedi Padawan", {
   color = Color(227, 169, 232, 255),
   model = {
	   "models/grealms/characters/padawan/padawan_05.mdl",
	   "models/grealms/characters/padawan/padawan_06.mdl",
           "models/grealms/characters/padawan/padawan_07.mdl",
           "models/grealms/characters/padawan/padawan_08.mdl",
           "models/grealms/characters/padawan/padawan_09.mdl",
	   },
   description = [[You are a Jedi Youngling! Await your training to pass the second trials!]],
   weapons = {"weapon_lightsaber"},
   command = "jedipad",
   max = 0,
   salary = 100,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "jedipadawan" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Jedi Padawan") end,
   category = "Jedi",
   sortOrder = 15,
   PlayerSpawn = function(ply)
   ply:SetHealth(1000)
   end
   })
TEAM_JEDI = DarkRP.createJob("Jedi Knight", {
   color = Color(227, 169, 232, 255),
   model = {"models/kriegsyntax/sw_752/kyle_est.mdl"},
   description = [[You are a Jedi Knight! you passed training and are now a full Jedi!]],
   weapons = {"weapon_lightsaber"},
   command = "jediknight",
   max = 0,
   salary = 100,
   admin = 0,
   vote = false,
   
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "jediknight" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Jedi Knight") end,
   category = "Jedi",
   sortOrder = 15,
   PlayerSpawn = function(ply)
   ply:SetHealth(1200)
   end
   })

TEAM_JEDI = DarkRP.createJob("Jedi Master", {
   color = Color(227, 169, 232, 255),
   model = {"models/grealms/characters/jedibattlelord/jedibattlelord_09.mdl"}, 
   description = [[You are a Jedi Master! Seek out a padawan and train him for his trials.]],
   weapons = {"weapon_lightsaber"},
   command = "jedimaster",
   max = 0,
   salary = 100,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "jedimaster" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Jedi Master") end,
   category = "Jedi",
   sortOrder = 15,  
   PlayerSpawn = function(ply)
   ply:SetHealth(1400)
   end
   })
--[[Dr0ids]]--
TEAM_R2D2 = DarkRP.createJob("R2D2", {
   color = Color(63, 61, 61, 255),
   model = {"models/player/r2d2.mdl"},
   description = [[You are a R2 unit!]],
   weapons = {"keys"},
   command = "r2d2",
   max = 1,
   salary = 60,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "r2d2" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"R2D2") end,
   category = "Republic Droids",
   sortOrder = 16,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
TEAM_C3PO = DarkRP.createJob("C3PO", {
   color = Color(63, 61, 61, 255),
   model = {"models/player/c3po.mdl"},
   description = [[You are C3PO, your creator is Darth... I mean...Anakin Skywalker!]],
   weapons = {"keys"},
   command = "c3po",
   max = 1,
   salary = 60,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "c3po" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"C3PO") end,
   category = "Republic Droids",
   sortOrder = 16,
    PlayerSpawn = function(ply)
    ply:SetHealth(500)
	end
})
--[[Evil]]--
TEAM_DROIDS = DarkRP.createJob("Battle droid", {
  color = Color(182,182,182,255),
  model = {"models/hgn/swrp/swrp/droid_b1_battle.mdl"},
  description = [[You are a battle droid]],
  weapons = {"weapon_752_e11"},
  command = "battle-droid",
  max = 0,
  salary = 50,
  admin = 0,
  vote = false,
  hasLicense = true,
  candemote = false,
  customCheck = function(ply) return ply:GetNWString("usergroup") == "battle-droid" or ply:GetNWString("usergroup") == "moderator" or ply:GetNWString("usergroup") == "trial-moderator" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or ply:IsAdmin() or PlychangeAllowed(ply,"Battle droid")  end,
  category = "Droids",
  sortOrder = 17,
  PlayerSpawn = function(ply)
  ply:SetHealth(500)
  end
})
TEAM_DROID = DarkRP.createJob("Battle Droid Commander", {
   color = Color(63, 61, 61, 255),
   model = {"models/player/sgg/starwars/battledroid_commander.mdl"},
   description = [[You are a Battle Droid Commander!]],
   weapons = {"weapon_752_e11"},
   command = "battle-droid-commander",
   max = 5,
   salary = 60,
   admin = 0,
   vote = false,
   candemote = false,
   customCheck = function(ply) return ply:GetNWString("usergroup") == "battle-droid-commander" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Battle Droid Commander") end,
   category = "Droids",
   sortOrder = 17,
    PlayerSpawn = function(ply)
    ply:SetHealth(650)
	end
})
TEAM_DROIDS = DarkRP.createJob("Super Battle droid", {
  color = Color(182,182,182,255),
  model = {"models/hgn/swrp/swrp/droid_b2.mdl"},
  description = [[You are a battle droid]],
  weapons = {"weapon_752_e11"},
  command = "super-battle-droid",
  max = 0,
  salary = 50,
  admin = 0,
  vote = false,
  hasLicense = true,
  candemote = false,
  customCheck = function(ply) return ply:GetNWString("usergroup") == "super-battle-droid" or ply:GetNWString("usergroup") == "moderator" or ply:GetNWString("usergroup") == "trial-moderator" or ply:GetNWString("usergroup") == "donator" or ply:IsAdmin() or ply:IsSuperAdmin() or PlychangeAllowed(ply,"Super Battle droid") end,
  category = "Droids",
  sortOrder = 17,
  PlayerSpawn = function(ply)
  ply:SetHealth(750)
  end
})
TEAM_STAFF = DarkRP.createJob("Staff On Duty", {
  color = Color(182,182,182,255),
  model = {"models/player/anon/anon.mdl"},
  description = [[You are Staff! Congrats!]],
  weapons = {"gmod_tool","weapon_physgun"},
  command = "staff",
  max = 0,
  salary = 500,
  admin = 0,
  vote = false,
  hasLicense = true,
  candemote = false,
  customCheck = function(ply) return ply:GetNWString("usergroup") == "moderator" or ply:GetNWString("usergroup") == "temp-mod" or ply:GetNWString("usergroup") == "trial-moderator" or ply:IsAdmin() or ply:IsSuperAdmin() end,
  category = "Staff On Duty",
  sortOrder = 17,
  PlayerSpawn = function(ply)
  ply:SetHealth(1000)
  end
})
--[[---------------------------------------------------------------------------
Define which team joining players spawn into and what team you change to if demoted
---------------------------------------------------------------------------]]
GAMEMODE.DefaultTeam = TEAM_CADET
