# np-weapons

> **NOTE**: This tutorial is only for learning purposes and only contains information on how to add the custom weapons that I could find in the NP Weapons Subscription (As of the 15/11/22), if there is a weapon that you were looking for, it could be a reskin of an MPX or a different weapon, so please ask the NP Support Team in the Official Asset Discord and they will help to the best of their ability when they have time. 
-------
> I will continue to update this overtime with updates where possible. I also plan on doing a tutorial on how to also change components to different weapons.



## Requirements

* NoPixel Weapons Subscription
* QBCore Framework

### Step 1
Add all the np weapons folders to a folder of your choice and ensure that the folders are being run on the server.

### Step 2

Add the following to qb-core > items.lua
```
	-- NP Weapons - Melee
	['weapon_sledgeham'] 		 	= {['name'] = 'weapon_sledgeham', 		 	['label'] = 'Sledgehammer', 	        	['weight'] = 15000, 	['type'] = 'weapon', 	['ammotype'] = nil,						['image'] = 'qr_sledgehammer.png', 		['unique'] = true, 		['useable'] = true, 	['created'] = nil, 	['decay'] = 30.0, 	['description'] = 'Great for cracking skulls...'},
	['weapon_bats'] 		 		= {['name'] = 'weapon_bats', 		 		['label'] = 'Baseball Bat', 	        	['weight'] = 15000, 	['type'] = 'weapon', 	['ammotype'] = nil,						['image'] = 'qr_sledgehammer.png', 		['unique'] = true, 		['useable'] = true, 	['created'] = nil, 	['decay'] = 30.0, 	['description'] = 'Great for cracking skulls...'},
	['weapon_katanas'] 		 		= {['name'] = 'weapon_katanas', 		 	['label'] = 'Katana', 	        			['weight'] = 15000, 	['type'] = 'weapon', 	['ammotype'] = nil,						['image'] = 'qr_sledgehammer.png', 		['unique'] = true, 		['useable'] = true, 	['created'] = nil, 	['decay'] = 30.0, 	['description'] = 'Great for cracking skulls...'},
	['weapon_katana'] 		 		= {['name'] = 'weapon_katana', 		 		['label'] = 'Lightsaber', 	        		['weight'] = 15000, 	['type'] = 'weapon', 	['ammotype'] = nil,						['image'] = 'qr_sledgehammer.png', 		['unique'] = true, 		['useable'] = true, 	['created'] = nil, 	['decay'] = 30.0, 	['description'] = 'Great for cracking skulls...'},
	['weapon_shiv'] 		 		= {['name'] = 'weapon_shiv', 		 		['label'] = 'Shiv', 	        			['weight'] = 15000, 	['type'] = 'weapon', 	['ammotype'] = nil,						['image'] = 'np_shiv.png', 				['unique'] = true, 		['useable'] = true, 	['created'] = nil, 	['decay'] = 30.0, 	['description'] = 'Great for cracking skulls...'},
	
	-- NP Weapons - Custom Pistols
	['weapon_glock'] 				= {['name'] = 'weapon_glock', 				['label'] = 'Glock 22', 					['weight'] = 4000, 		['type'] = 'weapon',	['ammotype'] = 'AMMO_PISTOL',			['image'] = 'np_glock.png', 			['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'A popular service pistol used by LSPD'},
	['weapon_dp9'] 				 	= {['name'] = 'weapon_dp9', 				['label'] = 'Diamondback DB9', 				['weight'] = 2000, 		['type'] = 'weapon',	['ammotype'] = 'AMMO_PISTOL',			['image'] = 'np_DB9.png', 				['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'The Generation 4 DB9 comes chambered in 9mm and is dubbed as one of the smallest micro-compact 9mm pistols on the market.'},
	['weapon_browning'] 			= {['name'] = 'weapon_browning', 			['label'] = 'Browning Hi-Power', 			['weight'] = 4000, 		['type'] = 'weapon',	['ammotype'] = 'AMMO_PISTOL',			['image'] = 'np_browning.png', 			['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'Single-action, semi-automatic pistol available in the 9×19mm Parabellum and .40 S&W calibers.'},
	-- NP Weapons - Custom SMGs
	['weapon_microsmg2'] 			= {['name'] = 'weapon_microsmg2', 			['label'] = 'Uzi', 							['weight'] = 10000, 	['type'] = 'weapon',	['ammotype'] = 'AMMO_SMG',				['image'] = 'np_micro-smg2.png', 		['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'A handheld lightweight compact machine gun that goes PEW PEW PEW'},
	['weapon_microsmg3'] 			= {['name'] = 'weapon_microsmg3', 			['label'] = 'Micro Uzi', 					['weight'] = 8000, 		['type'] = 'weapon',	['ammotype'] = 'AMMO_SMG',				['image'] = 'np_micro-smg.png', 		['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'A handheld lightweight compact machine gun that goes PEW PEW PEW'},
	['weapon_mp7'] 					= {['name'] = 'weapon_mp7', 				['label'] = 'Heckler & Koch MP7',			['weight'] = 10000, 	['type'] = 'weapon',	['ammotype'] = 'AMMO_SMG',				['image'] = 'np_mp7.png', 				['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'Developed as a genuine personal defense weapon, it far exceeds the LS Governments requirements profile.'},
	['weapon_minismg2'] 			= {['name'] = 'weapon_minismg2', 			['label'] = 'Skorpion',						['weight'] = 10000, 	['type'] = 'weapon',	['ammotype'] = 'AMMO_SMG',				['image'] = 'np_skorpion.png', 			['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'A foreign designated compact machine gun.'},
	-- NP Weapons - Custom ARs
	['weapon_assaultrifle2']		= {['name'] = 'weapon_assaultrifle2', 		['label'] = 'Zastava M70',					['weight'] = 25000, 	['type'] = 'weapon', 	['ammotype'] = 'AMMO_RIFLE',			['image'] = 'np_m70.png', 				['unique'] = true, 		['useable'] = true, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'A weaker copy of the AK-47.'},
	['weapon_m4']					= {['name'] = 'weapon_m4', 					['label'] = 'M4 Carbine',					['weight'] = 25000, 	['type'] = 'weapon', 	['ammotype'] = 'AMMO_RIFLE',			['image'] = 'np_m4.png', 				['unique'] = true, 		['useable'] = true, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'Standard LSPD issue firearm'},
	-- NP Weapons - Custom Snipers
	['weapon_sniperrifle2'] 		= {['name'] = 'weapon_sniperrifle2',		['label'] = 'Hunting Rifle', 				['weight'] = 15000, 	['type'] = 'weapon', 	['ammotype'] = 'AMMO_SNIPER',			['image'] = 'np_huntingrifle.png', 	 	['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0, 	['description'] = 'A high-precision, long-range rifle used for hunting animals'},
	['weapon_dragunov'] 			= {['name'] = 'weapon_dragunov',			['label'] = 'SVD', 							['weight'] = 15000, 	['type'] = 'weapon', 	['ammotype'] = 'AMMO_SNIPER',			['image'] = 'np_dragunov.png', 	 		['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0, 	['description'] = 'A foreign designated marksman rifle.'},
	['weapon_m14'] 					= {['name'] = 'weapon_m14',					['label'] = 'Mk14 Enhanced Battle Rifle', 	['weight'] = 15000, 	['type'] = 'weapon', 	['ammotype'] = 'AMMO_SNIPER',			['image'] = 'np_mk14.png', 	 			['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0, 	['description'] = 'A PD issued Designated Marksman Rifle'},
	['weapon_g22'] 					= {['name'] = 'weapon_g22',					['label'] = 'G22 Sniper Rifle', 			['weight'] = 15000, 	['type'] = 'weapon', 	['ammotype'] = 'AMMO_SNIPER',			['image'] = 'np_awm.png', 	 			['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0, 	['description'] = 'A PD issued Designated Marksman Rifle'},
	-- NP Weapons - Misc Weapons
	['weapon_nailgun'] 				= {['name'] = 'weapon_nailgun', 			['label'] = 'Nailgun', 						['weight'] = 5000, 		['type'] = 'weapon',	['ammotype'] = 'AMMO_PISTOL',			['image'] = 'np_nailgun.png', 			['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'Used to drive nails into wood.... or flesh'},
	['weapon_book'] 				= {['name'] = 'weapon_book', 				['label'] = 'Holy Bible', 					['weight'] = 1000, 		['type'] = 'weapon',	['ammotype'] = 'AMMO_BALL',				['image'] = 'qr_book.png', 				['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'Throwing knowledge into your enemies'},
	['weapon_brick'] 				= {['name'] = 'weapon_brick', 				['label'] = 'Concrete Brick', 				['weight'] = 1000, 		['type'] = 'weapon',	['ammotype'] = 'AMMO_BALL',				['image'] = 'brick.png', 				['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = 'Used for brick layering'},
	['weapon_cash'] 				= {['name'] = 'weapon_cash', 				['label'] = 'Cash', 						['weight'] = 1000, 		['type'] = 'weapon',	['ammotype'] = 'AMMO_BALL',				['image'] = 'cash.png', 				['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = ''},
	['weapon_staff'] 				= {['name'] = 'weapon_staff', 				['label'] = 'Staff', 						['weight'] = 1000, 		['type'] = 'weapon',	['ammotype'] = nil,				  		['image'] = 'np_staff01.png', 			['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0,	['description'] = ''},
	-- NP Weapons - Launchers
	['weapon_ltl'] 					= {['name'] = 'weapon_ltl',					['label'] = 'Rubber Slug Shotgun', 			['weight'] = 10000, 	['type'] = 'weapon', 	['ammotype'] = 'AMMO_SNIPER',			['image'] = 'np_lessthanlethal.png', 	 			['unique'] = true, 		['useable'] = false, 	['created'] = nil, 	['decay'] = 30.0, 	['description'] = ''},


```

### Step 3
Add the following to qb-core > weapons.lua
```
	-- NP Weapons - Custom Melee
	[`weapon_sledgeham`] 		 	= {['name'] = 'weapon_sledgeham', 			['label'] = 'Sledgehammer', 		['ammotype'] = nil,						['damagereason'] = 'Hammered / Pummelled'},
	[`weapon_bats`] 		 		= {['name'] = 'weapon_bats', 		 		['label'] = 'Baseball Bat', 	    ['ammotype'] = nil,						['damagereason'] = 'Hammered / Pummelled'},
	[`weapon_katanas`] 		 		= {['name'] = 'weapon_katanas', 		 	['label'] = 'Katana', 	        	['ammotype'] = nil,						['damagereason'] = 'Sliced / Murdered'},
	[`weapon_katana`] 		 		= {['name'] = 'weapon_katana', 		 		['label'] = 'Lightsaber', 	        ['ammotype'] = nil,						['damagereason'] = 'Sliced / Murdered'},
	[`weapon_shiv`] 		 		= {['name'] = 'weapon_shiv', 		 		['label'] = 'Shiv', 	        	['ammotype'] = nil,						['damagereason'] = 'Shanked / Murdered'},
	-- NP Weapons - Custom Pistols
	[`weapon_glock`] 				= {['name'] = 'weapon_glock', 				['label'] = 'Glock 22', 			['ammotype'] = 'AMMO_PISTOL',			['damagereason'] = 'Pistoled / Blasted / Plugged / Bust a cap in'},
	[`weapon_dp9`] 				 	= {['name'] = 'weapon_dp9', 				['label'] = 'Diamondback DB9', 		['ammotype'] = 'AMMO_PISTOL',			['damagereason'] = 'Pistoled / Blasted / Plugged / Bust a cap in'},
	[`weapon_browning`] 			= {['name'] = 'weapon_browning', 			['label'] = 'Browning Hi-Power', 	['ammotype'] = 'AMMO_PISTOL',			['damagereason'] = 'Pistoled / Blasted / Plugged / Bust a cap in'},
	-- NP Weapons - Custom SMGs
	[`weapon_microsmg2`] 			 = {['name'] = 'weapon_microsmg2', 			['label'] = 'Uzi', 					['ammotype'] = 'AMMO_SMG',				['damagereason'] = 'Riddled / Drilled / Finished / Submachine Gunned'},
	[`weapon_microsmg3`] 			 = {['name'] = 'weapon_microsmg3', 			['label'] = 'Micro Uzi', 			['ammotype'] = 'AMMO_SMG',				['damagereason'] = 'Riddled / Drilled / Finished / Submachine Gunned'},
	[`weapon_mp7`] 			 		 = {['name'] = 'weapon_mp7', 				['label'] = 'Heckler & Koch MP7', 	['ammotype'] = 'AMMO_SMG',				['damagereason'] = 'Riddled / Drilled / Finished / Submachine Gunned'},
	[`weapon_minismg2`] 			 = {['name'] = 'weapon_minismg2', 			['label'] = 'Skorpion', 			['ammotype'] = 'AMMO_SMG',				['damagereason'] = 'Riddled / Drilled / Finished / Submachine Gunned'},
    -- NP Weapons - Custom ARs
	[`weapon_assaultrifle2`] 		 = {['name'] = 'weapon_assaultrifle2', 	 	['label'] = 'Zastava M70', 			['ammotype'] = 'AMMO_RIFLE',			['damagereason'] = 'Ended / Rifled / Shot down / Floored'},
	[`weapon_m4`] 		 			 = {['name'] = 'weapon_m4', 	 			['label'] = 'M4 Carbine', 			['ammotype'] = 'AMMO_RIFLE',			['damagereason'] = 'Ended / Rifled / Shot down / Floored'},
	-- NP Weapons - Custom Snipers
	[`weapon_sniperrifle2`]		 	 = {['name'] = 'weapon_sniperrifle2', 		['label'] = 'Hunting Rifle',		['ammotype'] = 'AMMO_SNIPER',			['damagereason'] = 'Sniped / Picked off / Scoped'},
	[`weapon_dragunov`]		 		 = {['name'] = 'weapon_dragunov', 			['label'] = 'SVD',					['ammotype'] = 'AMMO_SNIPER',			['damagereason'] = 'Sniped / Picked off / Scoped'},
	[`weapon_m14`]		 		 	 = {['name'] = 'weapon_m14', 				['label'] = 'Mk14 Enhanced Battle Rifle',	['ammotype'] = 'AMMO_SNIPER',	['damagereason'] = 'Sniped / Picked off / Scoped'},
	[`weapon_g22`]		 		 	 = {['name'] = 'weapon_g22', 				['label'] = 'G22 Sniper Rifle',		['ammotype'] = 'AMMO_SNIPER',			['damagereason'] = 'Sniped / Picked off / Scoped'},
	-- NP Weapons - Misc Weapons
	[`weapon_nailgun`]				= {['name'] = 'weapon_nailgun',				['label'] = 'Nailgun',				['ammotype'] = nil,				['damagereason'] = 'Nailed'},
	[`weapon_book`]					= {['name'] = 'weapon_book',				['label'] = 'Holy Bible',			['ammotype'] = nil,				['damagereason'] = 'Converted'},
	[`weapon_brick`]				= {['name'] = 'weapon_brick',				['label'] = 'Concrete Brick',		['ammotype'] = nil,				['damagereason'] = 'Died'},
	[`weapon_cash`]					= {['name'] = 'weapon_cash',				['label'] = 'Cash',					['ammotype'] = nil,				['damagereason'] = 'Slapped By Cash'},
	[`weapon_staff`] 				= {['name'] = 'weapon_staff', 				['label'] = 'Staff', 				['ammotype'] = nil,				['damagereason'] = 'Ended'},
	-- NP Weapons - Shotguns
	[`weapon_ltl`] 		 			= {['name'] = 'weapon_ltl', 	  			['label'] = 'Rubber Slug Shotgun', 	['ammotype'] = nil,				['damagereason'] = 'Exploded'},


```

### Step 4
Add to qb-weapons > config.lua > Config.DurabilityMultiplier
```

	 -- NP Weapons
	['weapon_sledgeham'] 	= 0.15,
	['weapon_bats'] 	= 0.15,
	['weapon_katana'] 	= 0.15,
	['weapon_katanas'] 	= 0.15,
	['weapon_shiv'] 	= 0.15,
	['weapon_glock'] 	 = 0.15,
	['weapon_dp9'] 		= 0.15,
	['weapon_browning'] 	= 0.15,
	['weapon_microsmg2'] 	= 0.15,
	['weapon_microsmg3'] 	= 0.15,
	['weapon_mp7'] 	        = 0.15,
	['weapon_minismg2'] 	= 0.15,
	['weapon_assaultrifle2'] = 0.15,
	['weapon_m4'] 		= 0.15,
	['weapon_sniperrifle2'] = 0.15,
	['weapon_dragunov'] 	= 0.15,
	['weapon_m14'] 		= 0.15,
	['weapon_g22'] 	        = 0.15,
	['weapon_nailgun'] 	= 0.15,
	['weapon_book'] 	= 0.15,
	['weapon_brick'] 	= 0.15,
	['weapon_brick'] 	 = 0.15,
	['weapon_cash'] 	= 0.15,
	['weapon_ltl'] 	        = 0.15,

```
