--------Updated 15/04/21-----------
---SMG----
    local mp5_key = nil
    local Bizon_key = nil 
    local ump45_key = nil
    local Tommy_key = nil
    local uzi_key = nil
    local vector_key = nil

---Rifles----
    local akm_key = 4
    local m16a4_key = 7
    local mutant_key = nil
    local m416_key = 8
    local scarl_key = nil
    local qbz_key = nil
    local beryl_key = 5
    local g36c_key = nil 
    local groza_key = nil
    local aug_key = nil
    local DP28_key = nil
    local M249_key = nil
    local vss_key = nil
    local sks_key = nil
    local slr_key = nil 
    local mini_key = nil 
    local qbu_key = nil

    local set_off_key = 6

    local mp5_gkey = nil
    local Bizon_gkey = nil
    local ump45_gkey = nil
    local Tommy_gkey = nil
    local uzi_gkey = nil
    local vector_gkey = nil
    --==========================      ARs        ===============================--
    local akm_gkey = 3
    local m16a4_gkey = nil
    local mutant_gkey = nil
    local m416_gkey = nil
    local scarl_gkey = nil
    local qbz_gkey = nil
    local beryl_gkey = nil
    local g36c_gkey = nil
    local groza_gkey = nil
    local aug_gkey = nil
    --==========================      LMGs       ===============================--
    local DP28_gkey = 2
    local M249_gkey = 1
    --==========================      DMRs       ===============================--
    local vss_gkey = nil
    local sks_gkey = nil
    local slr_gkey = nil
    local mini_gkey = nil
    local qbu_gkey = nil

    local set_off_gkey = 6

    ---- Macro Settings (Do not touch) ----
    local control_key = "lctrl" 
    local ignore_key = "alt"
    local hold_breath_key = "lshift"
    local full_mode_key = "numlock" 
    local mode_switch_key = "capslock" 
    local lighton_key = "scrolllock"
    local vertical_sensitivity = 0.7
    local target_sensitivity = 50 
    local scope_sensitivity = 50 
    local scope4x_sensitivity = 50 
    local hold_breath_mode = true
    local full_mode = true
    local interval_ratio = 0.75
    local random_seed = 1
    local auto_mode = true 

------------recoil table-----------------

    local all_recoil_times = .6
    local recoil_table = {}
     
     recoil_table["m416"] = {
       basic={51.7,51.3,52.3,55.0, 65.0,68.5,69.7,71.2,72.5, 72.5,72.3,74.0,74.0, 75.0,75.5,76.0,77.0, 78},	
    basictimes = 2.1,
    full={51.7,51.3,52.3,55.0, 65.0,68.5,69.7,71.2,72.5, 72.5,72.3,69.8,69.6,76.6, 67.5,68.3,69.0,71.0,72.0, 73.0,74.5},
    fulltimes = 1*0.65,	
    quadruple={51.7,51.3,52.3,55.0, 65.0,68.5,69.7,71.2,72.5, 72.5,72.3,69.8,69.6,76.6, 67.5,68.3,69.0,71.0,72.0, 73.0,74.5,52.0,54.0,0},
    quadrupletimes = 1*0.99,
    fullof4x={41.1,41.3,41.3,42.3, 46.0,45.0,49.2,50.3,49.5, 58.5,51.0,50.5,59.4,55.1, 51.4,51.4,51.5,51.5,52.3, 53.3,54.0,52.0,52.0,0},
    fullof4xtimes = 2.9*1.15,
    speed = 90,
    maxbullets = 40,
    holdbreathtimes = 1.25,
    fullholdbreathtimes = 1.25,	
    }
     recoil_table["akm"] = {
         basic={41,32,36,42.9,42.6, 42,46,43.4,46,52, 51,51,52,53,45 ,45,53,53,53,53,53,53,53,53,53,53},
	basictimes = 2.8,
    full={41,32,36,42.9,42.6, 42,46,43.4,46,52, 51,51,52,53,45 ,45,53,53,53,53,53,53,53,53,53,53},
    fulltimes = 1.09*1.38,
    quadruple={41,32,36,42.9,42.6, 42,46,43.4,46,52, 51,51,52,53,45 ,45,53,53,53,53,53,53,53,53,53,53,0},
    quadrupletimes = 1.09*1.37,
    fullof4x={45.3,45.2,52.5,54.0,56.5, 59.0,59.5,59.0,61.5,61.9, 71.5,61.6,62.3,73.3,63.6 ,59,79,59,59,59,59,59,59,59,59,59,0},
    fullof4xtimes = 4*.77,
    speed = 96,
    maxbullets = 40,
    holdbreathtimes = 1.25,
    fullholdbreathtimes = 1.25,
    }
    recoil_table["beryl"] = {
        --basic 3x
        basic={41,32,36,42.9,42.6, 42,46,43.4,46,52, 51,51,52,53,45 ,45,53,53,53,53,53,53,53,53,53,53},
        basictimes = 4.9,
        full={41,32,36,42.9,42.6, 42,46,43.4,46,52, 51,51,52,53,45 ,45,53,53,53,53,53,53,53,53,53,53},
        fulltimes = 1.8,
        --quadruple 1x
        quadruple={41,32,36,42.9,42.6, 42,46,43.4,46,52, 51,51,52,53,45 ,45,53,53,53,53,53,53,53,53,53,53},
        quadrupletimes = 2,
       fullof4x={63,65,66,72.0,78.6, 83.6,88,88,87,89.9, 89.6,90.8,91,92.3,94,95,95,95,95,95,95,95,95,0},
    fullof4xtimes = 10*.24,
        speed = 65,
        maxbullets = 40,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    }
     recoil_table["m16a4"] = {
         basic={51.7,51.3,52.3,55.0, 65.0,68.5,69.7,71.2,72.5, 72.5,72.3,74.0,74.0, 75.0,75.5,76.0,77.0, 78},	
    basictimes = 2.3,
    full={41,32,36,42.9,42.6, 42,46,43.4,46,52, 51,51,52,53,45 ,45,53,53,53,53,53,53,53,53,53,53,0},
    fulltimes = 1.09*1.38,
    quadruple={41,32,36,42.9,42.6, 42,46,43.4,46,52, 51,51,52,53,45 ,45,53,53,53,53,53,53,53,53,53,53,0},
    quadrupletimes = 1.3,
    fullof4x={45.3,45.2,52.5,54.0,56.5, 59.0,59.5,59.0,61.5,61.9, 71.5,61.6,62.3,73.3,63.6 ,59,79,59,59,59,59,59,59,59,59,59,0},
    fullof4xtimes = 4*.77,
    speed = 96,
    maxbullets = 40,
    holdbreathtimes = 1.25,
    fullholdbreathtimes = 1.25,
    }
    recoil_table["mp5"] = { 
      basic={41,41,45,41,45, 45,41,45,41, 51, 41,51,41,41,46},
        basictimes = 1.8,
        full={40,45,44,45,44, 45,45,45,44,45, 44,45,44,45,44},
        fulltimes = 1.13,
        quadruple={56.5,44.6,46.5,45.7,42.6, 52.8,42.6,55.8,41.8,52, 43.7,46.8,48.8,42.6,52.2},
        quadrupletimes = 4*.6,
        fullof4x={56.5,44.6,46.5,45.7,42.6, 52.8,42.6,55.8,41.8,52, 43.7,46.8,48.8,42.6,52.2},
        fullof4xtimes = 2.8,
        speed = 90,
        maxbullets = 35,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,
    } 
    recoil_table["Bizon"] = { 
      basic={36.5,34.6,36.5,41.8,41.6, 42.8,41.6,45.8,41.8,42, 43.7,41.8,41.8,42.6,42.2},
        basictimes = 1.45,
        full={36.5,34.6,36.5,41.8,41.6, 42.8,41.6,45.8,41.8,42, 43.7,41.8,41.8,42.6,42.2},
        fulltimes = 1.18,
        quadruple={56.5,44.6,46.5,45.7,42.6, 52.8,42.6,55.8,41.8,52, 43.7,46.8,48.8,42.6,52.2},
        quadrupletimes = 4*.6,
        fullof4x={56.5,44.6,46.5,45.7,42.6, 52.8,42.6,55.8,41.8,52, 43.7,46.8,48.8,42.6,52.2},
        fullof4xtimes = 4*.5,
        speed = 90,
        maxbullets = 35,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,
    } 
recoil_table["M249"] = { 
       basic={53,55, 54,56,57,61,60, 51,60,58,55,60, 58,60,60,60,60,55,55,55,55,57,57,57,57},
        basictimes = 1.6,
        full={59,44,42,50,55, 50,56,57,61,60, 51,60,58,55,60, 58,60,60,60,60,55,55,55,55,57,57,57,57},
        fulltimes = 1*0.89,
        quadruple={53,44,48,49,49,48, 47,46,47,45,47, 45,45, 45,45,45,46,46,46,47,45,47, 45,45, 45,45,45,46,46,46,47,45,47, 45,45, 45,45,45,46,46},
        quadrupletimes = 0.88,
        fullof4x={58,25,31,41,45, 50,51,52,52,52, 51,51,51,51,51, 53,48,48,48,48, 48,48,48,48,48},
        fullof4xtimes = 2.45*1*1.04,
        speed = 100,
        maxbullets = 40,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    } 
     recoil_table["uzi"] = { 
        basic={12.0,12.0,12.0,21.6,26.6, 28.4,28.4,31.9,29.8,31.6, 36.6,36.9,38.0,43.8,43.8,46,47,46,45,46,45,46,45,46,45,46,45,46,45,46,45,46,45,46,45,46,45},
        basictimes = 4.3,
        full={12.0,12.0,12.0,21.6,26.6, 28.4,28.4,31.9,29.8,31.6, 36.6,36.9,38.0,43.8,43.8,46,47,46,45,46,45,46,45,46,45,46,45,46,45,46,45,46,46,45},
        fulltimes = 3.1,
        quadruple={20.7,16.5,16.5,17.9,18.6, 20.4,22.4,22.9,25.8,27.6, 32.6,36.9,38.0,38.8,39.8,39.9},
        quadrupletimes = 0.78,
        fullof4x={20.7,16.5,16.5,17.9,18.6, 20.4,22.4,22.9,25.8,27.6, 32.6,36.9,38.0,38.8,39.8,39.9},
        fullof4xtimes = 0.89*0.76*0.76,
        speed = 48,
        maxbullets = 35,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    } 
     recoil_table["vector"] = {
        basic={23,26,29,31, 45,41,41,41,41, 39,42,42,42,42, 37,38,38,38,38, 38,38,38,38,38},
        basictimes = 3,
        full={23,26,29,31, 45,41,41,41,41, 39,42,42,42,42, 37,38,38,38,38, 38,38,38,38,38},
        fulltimes = 1.75,
        quadruple={22.0,15.3,22.0,25, 23.0,28.0,30.0,26.5,36.5, 27.5,32.5,33.0,40,35, 41,39.8,39.9,49,43.5, 38,50,34,41.5,49},
        quadrupletimes = 1.55*0.87,
        fullof4x={23,26,29,31, 45,41,41,41,41, 39,42,42,42,42, 37,38,38,38,38, 38,38,38,38,38},
        fullof4xtimes = 4.9,
        speed = 55,
        maxbullets = 25,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    } 
     recoil_table["ump45"] = {
        basic={33.5,34.2,34.5,37.7,41.3, 45.0,42.7,42.2,42.8,42.0, 42,42,42,41,41,38,42,42,42,42,41,42,41,41,42,41,42,41,41},
        basictimes = 1.9,
        full={29,29,29,29,32,36,36,36,36,36,36,36,36,35,35,35,35,35,35,35,35,35,39,},
        fulltimes = 1.4,
        quadruple={33.1,19.2,28.5,33.7, 37.3,37.0,38.7,40.2,41.8,44.0, 43.8,43.8,46.5,44.5,44.943},
        quadrupletimes = 1.95,
        fullof4x={32.3,18.8,28.5,34.0,36.0,36.0,38.7,39.2,39.8,44.0,41.8,42.5,44.5,42.5,44.943,43.1,44.00,43.00,46,42,43,43,41,45,43,45,45,42,45,42,45,45,44,41},
        fullof4xtimes = 3,
        speed = 90,
        maxbullets = 40,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    } 
    recoil_table["Tommy"] = {
        basic={45,45,65,65,85,83,83,83,85,85, 90,90,90,90,90},
        basictimes = 1.21,
        full={50,50,45,60,80,80,78,78,78,78, 82,82,82,82,82},
        fulltimes = 1.05,
        quadruple={33.1,19.2,28.5,33.7, 37.3,37.0,38.7,40.2,41.8,44.0, 43.8,43.8,46.5,44.5,44.943},
        quadrupletimes = 1.75*1*0.89,
        fullof4x={32.3,18.8,28.5,34.0,36.0,36.0,38.7,39.2,39.8,44.0,41.8,42.5,44.5,42.5,44.943,43.1,44.00,43.00,46,42,43,43,41,45,43,45,45,42,45,42,45,45,44,41},
        fullof4xtimes = 2.63*1*0.85,
        speed = 90,
        maxbullets = 40,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    } 
    
     recoil_table["DP28"] = {
        basic={33,32,36,36.9,36.6, 42,46,43.4,46,52, 48,48,48,48,48 ,51},
    	basictimes = 1.05,
        full={48,32,36,36.9,36.6, 35,38.7,33.4,36,39, 32,37,42,37,46 ,47},
        fulltimes = 1.09*1.28,
        quadruple={61.3,51.2,52.5,54.0,56.5, 54.0,53.5,52.0,56.5,57.9, 56.5,58.6,58.3,62.3,63.6 ,70},
        quadrupletimes = 4*.62,
        fullof4x={61.3,51.2,52.5,54.0,56.5, 54.0,53.5,52.0,56.5,57.9, 56.5,58.6,58.3,62.3,63.6 ,70},
        fullof4xtimes = 4*0.62,
        speed = 96,
        maxbullets = 40,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,
    }
     recoil_table["scarl"] = {
        basic={50.2,31.0,34.0,43.0, 45.5,54.9,55.0,56.2,57.0, 58.6,58.9,60.9,61.9,62.9, 63.8,53.5,55.5,59.3,59.3, 61.3,60.3,60.3,60.3,60.3,60.3,60.3,60.3,60.3,60.3},
    basictimes = 1.58,
    full={55.0,55.5,56.6,57.0,58.1, 69.9,62.0,65.2,69.8,66.4, 67.9,78.9,69.9,81.5,72.8, 68.5,66.5,66.5,66.5,66.5,68.5,68.5,68.5,68.5,68.5,68.5,60.5,60.5},
    fulltimes = 1*0.876,
    quadruple={53.0,22.3,33.5,40.0, 44.0,48.1,49.5,49.0,55.0, 58.4,55.1,51.3,57.0,57.1, 58.4,60.5,64.0,62.0,60.0, 61.5,61.5,63.5,63.5,62.5, 60.5,60.5,61.5,61.5,61.5},
    quadrupletimes = 1.03*0.812,
    fullof4x={58.0,35.3,35.4,48.3, 49.1, 54.9,55.0,56.4,62.8,64.1, 64.4,67.4,66.6,56.9,51.8, 61.0,61.0,61.0,59.5,61.5, 61.5,60.0,61.5,61.5,61.5, 60.0,60.0,61.5,61.5,61.5},
    fullof4xtimes = 2.45*1*1.151,
    speed = 100,
    maxbullets = 40,
    holdbreathtimes = 1.25,
    fullholdbreathtimes = 1.25,	
    }
     recoil_table["g36c"] = {
        basic={51.1,24.0,32.0,41.0, 42.5,46.9,51.0,52.2,51.8, 47.4,49.9,56.9,58.9,58.9, 62.8,57.5,57.5,60.3,60.3, 62.3,62.3,62.3,60.3,60.3,60.3,60.3,60.3,60.3,60.3},
        basictimes = 1.20,
        full={53.0,22.3,34.1,43.0, 46.0,48.1,48.5,47.0,53.0, 56.4,53.1,51.3,54.0,55.1, 57.4,57.5,57.0,54.0,54.0, 56.5,57.5,57.5,57.5,57.5, 57.5,57.5,57.5,57.5,57.5},
        fulltimes = 1*0.88,
        quadruple={53.0,22.3,33.7,41.4, 45.0,48.7,49.5,49.0,55.0, 58.4,55.1,51.3,57.0,57.1, 58.4,60.5,61.0,60.0,60.0, 60.5,60.5,61.5,61.5,61.5, 60.5,60.5,61.5,61.5,61.5},
        quadrupletimes = 1.0*0.9,
        fullof4x={58.2,24.3,31.4,41.3, 45.1, 50.9,51.0,52.4,60.8,60.1, 54.4,57.4,56.6,56.9,51.8, 61.0,61.0,61.0,59.5,61.5, 61.5,60.0,61.5,61.5,61.5, 60.0,60.0,61.5,61.5,61.5},
        fullof4xtimes = 2.45*1*0.837,
        speed = 100,
        maxbullets = 40,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    }
     recoil_table["mutant"] = {
        basic={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,69.0, 70.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0},
        basictimes = 0.8,
        full={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        fulltimes = 1*0.77,
        quadruple={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        quadrupletimes = 2.45*0.77,
        fullof4x={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        fullof4xtimes = 3.45*1*0.75,
        speed = 90,
        maxbullets = 30,
        clickspeed = 30,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    } 
     recoil_table["qbz"] = {
        basic={27,28,30,33, 39,39,43,40,52, 45,45,41,41,41,41,41,41,41,41,41,41,41,41},
        basictimes = 2.3,
        full={27,28,30,33, 39,39,43,40,52, 55,53,49,49,49},
        fulltimes = 1.48,
        quadruple={46.0,21.0,29.1,34.0, 39.1,39.0,40.0,40.0,40.6, 47.1,47.0,45.3,47.0,50.0, 50.1,51,48,51,50.2, 51,51.3,51,52,52.5, 51,51,51,51,51},
        quadrupletimes = 2.45,
        fullof4x={27,28,30,33, 39,39,43,40,52, 55,53,49,49,49},
        fullof4xtimes = 3.7,
        speed = 100,
        maxbullets = 40,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,		
    } 

     recoil_table["groza"] = {
        basic={41,32,36,42.9,42.6, 42,46,43.4,46,52, 51,51,52,53,58 ,53},
    	basictimes = 1.91,
        full={41,32,36,42.9,42.6, 42,46,43.4,46,52, 51,51,52,53,58 ,53},
        fulltimes = 1.09*1.48,
        quadruple={61.3,51.2,52.5,54.0,56.5, 54.0,53.5,52.0,56.5,57.9, 56.5,58.6,58.3,62.3,63.6 ,70},
        quadrupletimes = 4*.66,
        fullof4x={61.3,51.2,52.5,54.0,56.5, 54.0,53.5,52.0,56.5,57.9, 56.5,58.6,58.3,62.3,63.6 ,70},
        fullof4xtimes = 4*.78,
        speed = 96,
        maxbullets = 40,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,
    }
     recoil_table["aug"] = {
          basic={39,39,39,54,54,54,54,57,57,59,61,61,61,55,55,55,55,55,55,55,55,55,55},	
        basictimes = 1.6,
        full={39,39,39,54,54,54,54,57,57,59,61,61,61,55,55,55,55,55,55,55,55,55,55},
        fulltimes = 1.13,	
        quadruple={45.0,29.3,36.3,42.3, 45.0,47.0,46.2,48.3,48.5, 48.5,50.0,50.5,50.4,55.1, 51.4,50.4,51.5,51.5,52.3, 53.3,54.0,52.0,52.0,52.0, 52.0,53.0,52.0,52.0,52.0},
        quadrupletimes = 1.2*0.74,
        fullof4x={55,55,69,69,84,84,84,84,92,92,92,92,92,95,95,95,95,95,95,95,95,95,95,95,95,95},
        fullof4xtimes = 1.8,
        speed = 100,
        maxbullets = 40,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,
    }
     recoil_table["vss"] = {
        basic={48,34.5,43.3,74, 84,93,103,105.3,106, 115,93,118,109,107, 115,111,113,115,107, 103,117},
        basictimes = 1.383,
        full={43,23,40,71, 87,98,106,105,106, 117,108,116,107,111, 117,116,117,119,107},
        fulltimes = 1*1.05,
        quadruple={43,23,40,71, 87,98,106,105,106, 117,108,116,107,111, 117,116,117,119,107},
        quadrupletimes = 1*1.05,
        fullof4x={43,23,40,71, 87,98,106,105,106, 117,108,116,107,111, 117,116,117,119,107},
        fullof4xtimes = 1*1.05,
        speed = 90,
        maxbullets = 20,
        clickspeed = 45,
        holdbreathtimes = 1.0,
        fullholdbreathtimes = 1.0,	
    }
     recoil_table["sks"] = {
        basic={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,69.0, 70.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0},
        basictimes = 1.05,
        full={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        fulltimes = 1*0.77,
        quadruple={49.9,38.9,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        quadrupletimes = 2.65*0.77,
        fullof4x={51.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        fullof4xtimes = 3.8*1*0.75,
        speed = 90,
        maxbullets = 20,
        clickspeed = 45,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    }
     recoil_table["slr"] = {
        basic={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,69.0, 70.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0},
        basictimes = 1.05,
        full={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        fulltimes = 1*0.77,
        quadruple={49.9,38.9,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        quadrupletimes = 2.65*0.77,
        fullof4x={51.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        fullof4xtimes = 3.8*1*0.75,
        speed = 100,
        maxbullets = 20,
        clickspeed = 50,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    }
     recoil_table["mini"] = {
        basic={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,69.0, 70.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0},
        basictimes = 1.05,
        full={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        fulltimes = 1*0.77,
        quadruple={49.9,38.9,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        quadrupletimes = 2.65*0.77,
        fullof4x={51.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        fullof4xtimes = 3.8*1*0.75,
        speed = 135,
        maxbullets = 30,
        clickspeed = 70,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    }
     recoil_table["qbu"] = {
        basic={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,69.0, 70.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0,69.0},
        basictimes = 1.05,
        full={41.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        fulltimes = 1*0.77,
        quadruple={49.9,38.9,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        quadrupletimes = 2.65*0.77,
        fullof4x={51.9,36.5,37.1,50.5,55.9, 62.9,66.9,69.5,69.5,70.0, 71.2,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0,70.0},
        fullof4xtimes = 3.8*1*0.75,
        speed =135,
        maxbullets = 20,
        clickspeed = 70,
        holdbreathtimes = 1.25,
        fullholdbreathtimes = 1.25,	
    }

    --------------FUNCTIONS-------------

    --- Math Library ---
    do
        local state_8, state_45, cached_bits, cached_bits_qty = 2, 0, 0, 0
        local prev_width, prev_bits_in_factor, prev_k = 0
        for c in GetDate():gmatch"." do
           state_45 = state_45 % 65537 * 23456 + c:byte()
        end
 
        local function get_53_random_bits()
           local value53 = 0
           for shift = 26, 27 do
              local p = 2^shift
              state_45 = (state_45 * 233 + 7161722017421) % 35184372088832
              repeat state_8 = state_8 * 76 % 257 until state_8 ~= 1
              local r = state_8 % 32
              local n = state_45 / 2^(13 - (state_8 - r) / 32)
              n = (n - n%1) % 2^32 / 2^r
              value53 = value53 * p + ((n%1 * 2^32) + (n - n%1)) % p
           end
           return value53
        end
        
        for j = 1, 10 do get_53_random_bits() end
 
        local function get_random_bits(number_of_bits)
           local pwr_number_of_bits = 2^number_of_bits
           local result
           if number_of_bits <= cached_bits_qty then
              result = cached_bits % pwr_number_of_bits
              cached_bits = (cached_bits - result) / pwr_number_of_bits
           else
              local new_bits = get_53_random_bits()
              result = new_bits % pwr_number_of_bits
              cached_bits = (new_bits - result) / pwr_number_of_bits * 2^cached_bits_qty + cached_bits
              cached_bits_qty = 53 + cached_bits_qty
           end
           cached_bits_qty = cached_bits_qty - number_of_bits
           return result
        end
 
        table = table or {}
        table.getn = table.getn or function(x) return #x end
 
        math = math or {}
        math.huge  = math.huge  or 1/0
        math.abs   = math.abs   or function(x)    return x < 0 and -x or x end
        math.floor = math.floor or function(x)    return x - x%1           end
        math.ceil  = math.ceil  or function(x)    return x + (-x)%1        end
        math.min   = math.min   or function(x, y) return x < y and x or y  end 
        math.max   = math.max   or function(x, y) return x > y and x or y  end
        math.sqrt  = math.sqrt  or function(x)    return x^0.5             end
        math.pow   = math.pow   or function(x, y) return x^y               end
 
        math.frexp = math.frexp or
           function(x)
              local e = 0
              if x == 0 then
                 return x, e
              end
              local sign = x < 0 and -1 or 1
              x = x * sign
              while x >= 1 do
                 x = x / 2
                 e = e + 1
              end
              while x < 0.5 do
                 x = x * 2
                 e = e - 1
              end
              return x * sign, e
           end
 
        math.exp = math.exp or 
           function(x)
              local e, t, k, p = 0, 1, 1
              repeat e, t, k, p = e + t, t * x / k, k + 1, e
              until e == p
              return e
           end
 
        math.log = math.log or
          function(x)
             assert(x > 0)
             local a, b, c, d, e, f = x < 1 and x or 1/x, 0, 0, 1, 1
             repeat
                repeat
                   c, d, e, f = c + d, b * d / e, e + 1, c
                until c == f
                b, c, d, e, f = b + 1 - a * c, 0, 1, 1, b
             until b <= f
             return a == x and -f or f
          end

        math.log10 = math.log10 or
          function(x)
             return math.log(x) / 2.3025850929940459
          end

        math.random = math.random or
          function(m, n)
             if m then
                if not n then
                   m, n = 1, m
                end
                local k = n - m + 1
                if k < 1 or k > 2^53 then
                   error("Invalid arguments for function 'random()'", 2)
                end
         local width, bits_in_factor, modk
                if k == prev_k then
                   width, bits_in_factor = prev_width, prev_bits_in_factor
                else
                   local pwr_prev_width = 2^prev_width
                   if k > pwr_prev_width / 2 and k <= pwr_prev_width then
                      width = prev_width
                   else
                      width = 53
                      local width_low = -1
                      repeat
                         local w = (width_low + width) / 2
                         w = w - w%1
                         if k <= 2^w then
                            width = w
                         else
                            width_low = w
                         end
                      until width - width_low == 1
                      prev_width = width
                   end
                   bits_in_factor = 0
                   local bits_in_factor_high = width + 1
                   while bits_in_factor_high - bits_in_factor > 1 do
                      local bits_in_new_factor = (bits_in_factor + bits_in_factor_high) / 2
                      bits_in_new_factor = bits_in_new_factor - bits_in_new_factor%1
                      if k % 2^bits_in_new_factor == 0 then
                         bits_in_factor = bits_in_new_factor
                      else
                         bits_in_factor_high = bits_in_new_factor
                      end
                   end
                   prev_k, prev_bits_in_factor = k, bits_in_factor
                end
                local factor, saved_bits, saved_bits_qty, pwr_saved_bits_qty = 2^bits_in_factor, 0, 0, 2^0
                k = k / factor
                width = width - bits_in_factor
                local pwr_width = 2^width
                local gap = pwr_width - k
                repeat
                   modk = get_random_bits(width - saved_bits_qty) * pwr_saved_bits_qty + saved_bits
                   local modk_in_range = modk < k
                   if not modk_in_range then
                      local interval = gap
                      saved_bits = modk - k
                      saved_bits_qty = width - 1
                      pwr_saved_bits_qty = pwr_width / 2
                      repeat
                         saved_bits_qty = saved_bits_qty - 1
                         pwr_saved_bits_qty = pwr_saved_bits_qty / 2
                         if pwr_saved_bits_qty <= interval then
                            if saved_bits < pwr_saved_bits_qty then
                               interval = nil
                            else
                               interval = interval - pwr_saved_bits_qty
                               saved_bits = saved_bits - pwr_saved_bits_qty
                            end
                         end
                      until not interval
                   end
                until modk_in_range
                return m + modk * factor + get_random_bits(bits_in_factor)
             else
                return get_53_random_bits() / 2^53
             end
          end

        local orig_Sleep = Sleep
        function Sleep(x)
          return orig_Sleep(x - x%1)
    end

    ---- Round Values ----

    function round(x)
        return x>=0 and math.floor(x+0.5) or math.ceil(x-0.5)
    end

    ---- Convert Sens ----
    function convert_sens(unconvertedSens) 
        return 0.002 * math.pow(10, unconvertedSens / 50)
    end

    ---- Calc Sens Scale ----
    function calc_sens_scale(sensitivity)
        return convert_sens(sensitivity)/convert_sens(50)
    end
    
    local target_scale = calc_sens_scale(target_sensitivity)
    local scope_scale = calc_sens_scale(scope_sensitivity)
    local scope4x_scale = calc_sens_scale(scope4x_sensitivity)

    ---- Recoil Mode ---- 
    function recoil_mode()
        if not IsKeyLockOn(mode_switch_key) then
            if IsKeyLockOn(full_mode_key) and full_mode then
    	       return "full";
    	else
    	       return "basic";
            end
        end	
    	
        if IsKeyLockOn(mode_switch_key) then
            if IsKeyLockOn(full_mode_key) and full_mode then
    	       return "fullof4x"
    	else
    	       return "quadruple"
            end 
        end		
    end
     
    ---- Single Value ---- 
    function single_value(value)
        return 10 * math.floor(( value / 10 ) + 0.9)
    end
    
    ---- Recoil Value ---- 
    function recoil_value(_weapon,_duration)
        local _mode = recoil_mode()
        local step = (math.floor(_duration/recoil_table[_weapon]["speed"])) + 1

        if step > #recoil_table[_weapon][_mode] then step = #recoil_table[_weapon][_mode] end

        local weapon_recoil = recoil_table[_weapon][_mode][step]
        local weapon_speed = recoil_table[_weapon]["speed"]
        local weapon_clickspeed = recoil_table[_weapon]["clickspeed"]
        local weapon_maxbullets = recoil_table[_weapon]["maxbullets"]
        local weapon_basictimes = recoil_table[_weapon]["basictimes"]
        local weapon_fulltimes = recoil_table[_weapon]["fulltimes"]
        local weapon_quadrupletimes = recoil_table[_weapon]["quadrupletimes"]
        local weapon_fullof4xtimes = recoil_table[_weapon]["fullof4xtimes"]
        local weapon_holdbreathtimes = recoil_table[_weapon]["holdbreathtimes"]
        local weapon_fullofholdbreathtimes = recoil_table[_weapon]["fullholdbreathtimes"]
       
        recoil_times = all_recoil_times * 0.7 / vertical_sensitivity 

        if recoil_mode() == "basic" and not IsModifierPressed(hold_breath_key) then weapon_recoil = weapon_recoil * recoil_times * weapon_basictimes end
        if recoil_mode() == "basic" and hold_breath_mode and IsModifierPressed(hold_breath_key) then weapon_recoil = weapon_recoil * weapon_holdbreathtimes * recoil_times * weapon_basictimes end
        if recoil_mode() == "full" and not IsModifierPressed(hold_breath_key) then weapon_recoil = weapon_recoil * recoil_times * weapon_fulltimes end
        if recoil_mode() == "full" and hold_breath_mode and IsModifierPressed(hold_breath_key) then weapon_recoil = weapon_recoil * weapon_fullofholdbreathtimes * recoil_times * weapon_fulltimes end
        if recoil_mode() == "quadruple" then weapon_recoil = weapon_recoil * recoil_times * weapon_quadrupletimes end
        if recoil_mode() == "fullof4x" then weapon_recoil = weapon_recoil * recoil_times * weapon_fullof4xtimes end 
         
        if IsMouseButtonPressed(2) then weapon_recoil = weapon_recoil / target_scale
        elseif recoil_mode() == "basic" then weapon_recoil = weapon_recoil / scope_scale 
        elseif recoil_mode() == "full" then weapon_recoil = weapon_recoil / scope_scale
        elseif recoil_mode() == "quadruple" then weapon_recoil = weapon_recoil / scope4x_scale
        elseif recoil_mode() == "fullof4x" then weapon_recoil = weapon_recoil / scope4x_scale 
        end

        return weapon_speed,weapon_recoil,weapon_clickspeed,weapon_maxbullets
    end
    

    --------------binds------------------------

    function OnEvent(event, arg)
        OutputLogMessage("event = %s, arg = %d\n", event, arg)

        --- checking if profile is active ---
        if (event == "PROFILE_ACTIVATED") then
            EnablePrimaryMouseButtonEvents(true)
            Fire = false
            current_weapon = "none"
            shoot_duration = 0.0

        --- checking firing mode ---
        if IsKeyLockOn(lighton_key) 
            then PressAndReleaseKey(lighton_key) elseif IsKeyLockOn(full_mode_key) 
                then PressAndReleaseKey(full_mode_key) elseif IsKeyLockOn(mode_switch_key) 
                    then PressAndReleaseKey(mode_switch_key)
                        end
 
        --- cancel if deactivated ---
        elseif event == "PROFILE_DEACTIVATED" then
            ReleaseMouseButton(1)
        end 


        --- get weapon based on key ---
        if (event == "MOUSE_BUTTON_PRESSED" and arg == set_off_key) or (event == "G_PRESSED" and arg == set_off_gkey) then current_weapon = "none" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == akm_key) or (event == "G_PRESSED" and arg == akm_gkey) then current_weapon = "akm" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == M249_key) or (event == "G_PRESSED" and arg == M249_gkey) then current_weapon = "M249" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == DP28_key) or (event == "G_PRESSED" and arg == DP28_gkey) then current_weapon = "DP28" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == m16a4_key) or (event == "G_PRESSED" and arg == m16a4_gkey) then current_weapon = "m16a4" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == Tommy_key) or (event == "G_PRESSED" and arg == Tommy_gkey) then current_weapon = "Tommy" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == mutant_key) or (event == "G_PRESSED" and arg == mutant_gkey) then current_weapon = "mutant" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == m416_key) or (event == "G_PRESSED" and arg == m416_gkey) then current_weapon = "m416" 
    	elseif (event == "MOUSE_BUTTON_PRESSED" and arg == Bizon_key) or (event == "G_PRESSED" and arg == Bizon_gkey) then current_weapon = "Bizon" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == g36c_key) or (event == "G_PRESSED" and arg == g36c_gkey) then current_weapon = "g36c"
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == ump45_key) or (event == "G_PRESSED" and arg == ump45_gkey) then current_weapon = "ump45" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == uzi_key) or (event == "G_PRESSED" and arg == uzi_gkey) then current_weapon = "uzi" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == vector_key) or (event == "G_PRESSED" and arg == vector_gkey) then current_weapon = "vector" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == scarl_key) or (event == "G_PRESSED" and arg == scarl_gkey) then current_weapon = "scarl" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == qbz_key) or (event == "G_PRESSED" and arg == qbz_gkey) then current_weapon = "qbz" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == beryl_key) or (event == "G_PRESSED" and arg == beryl_gkey) then current_weapon = "beryl"
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == groza_key) or (event == "G_PRESSED" and arg == groza_gkey) then current_weapon = "groza"
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == aug_key) or (event == "G_PRESSED" and arg == aug_gkey) then current_weapon = "aug"
    	elseif (event == "MOUSE_BUTTON_PRESSED" and arg == mp5_key) or (event == "G_PRESSED" and arg == mp5_gkey) then current_weapon = "mp5"  
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == vss_key) or (event == "G_PRESSED" and arg == vss_gkey) then current_weapon = "vss" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == sks_key) or (event == "G_PRESSED" and arg == sks_gkey) then current_weapon = "sks" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == slr_key) or (event == "G_PRESSED" and arg == slr_gkey) then current_weapon = "slr" 
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == mini_key) or (event == "G_PRESSED" and arg == mini_gkey) then current_weapon = "mini"  
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == qbu_key) or (event == "G_PRESSED" and arg == qbu_gkey) then current_weapon = "qbu"
        
        elseif (event == "MOUSE_BUTTON_PRESSED" and arg == 1) then
            --- check if script is active ---
            if ((current_weapon == "none") or IsModifierPressed(ignore_key)) then
                PressMouseButton(1)
                repeat
                    Sleep(30)
                until not IsMouseButtonPressed(1)
            else    
                while IsMouseButtonPressed(1) do 

                    --- getting new recoil ---
                    local intervals,recovery,clicktime,bullets = recoil_value(current_weapon,shoot_duration)

                    --- parsing new Y coordonate ---
                    local recoveryParsed = round(recovery / 10)
                    
                    --- updating mouse location ---
                    MoveMouseRelative(0, recoveryParsed)  

                    --- updating sleep schedule ---
                    Sleep(intervals/10)

                    ---updating duration ---
                    shoot_duration = shoot_duration + (intervals/10)
                end
            end 
        elseif (event == "MOUSE_BUTTON_RELEASED" and arg == 1) then
            --- reset everything if disabled ---
            Fire = false
            shoot_duration = 0.0 
        end 

        --- deactivate script in case something went wrong ---
        if (current_weapon == "none") then
            if IsKeyLockOn(lighton_key) then
            PressAndReleaseKey(lighton_key)
            end 
        else
            if not IsKeyLockOn(lighton_key) then
            PressAndReleaseKey(lighton_key)
            end
        end
    end 
end
