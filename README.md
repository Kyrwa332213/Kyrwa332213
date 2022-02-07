	#Category only allowed for GER
GER_mefo_bills_category = {

	GER_mefo_bills_mission = {

		allowed = { always = no }

		icon = ger_mefo_bills

		available = {
			NOT = { has_government = democratic }
			GER_can_delay_mefo_payment = yes
			has_political_power > 0
			hidden_trigger = { always = no }
		}

		#cost = GER_mefo_bill_counter?10

		days_mission_timeout = 180
		is_good = yes
		fire_only_once = yes

		cancel_trigger = {
			hidden_trigger = {
				OR = {
					NOT = { GER_has_mefo_bills = yes }
					has_idea = GER_mefo_bills_ended
				}
			}
		}

		days_remove = GER_extend_mefo_bills_days?0
		remove_effect = {
		}

		complete_effect = {
		}

		timeout_effect = {
			if = {
				limit = {
					has_country_flag = ger_has_cancelled_mefo
				}
				GER_remove_mefo_bills = yes
				#1
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 15 compare = less_than }
					}
					add_political_power = -20
					add_timed_idea = { idea = GER_mefo_bills_ended days = 60 }
				}
				#2
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 20 compare = equals }
					}
					add_political_power = -40
					add_timed_idea = { idea = GER_mefo_bills_ended days = 80 }
				}
				#3
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 30 compare = equals }
					}
					add_political_power = -60
					add_timed_idea = { idea = GER_mefo_bills_ended days = 100 }
				}
				#4
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 40 compare = equals }
					}
					add_political_power = -80
					add_timed_idea = { idea = GER_mefo_bills_ended days = 120 }
				}
				#5
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 50 compare = equals }
					}
					add_political_power = -100
					add_timed_idea = { idea = GER_mefo_bills_ended days = 140 }
				}
				#6
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 60 compare = equals }
					}
					add_political_power = -120
					add_timed_idea = { idea = GER_mefo_bills_ended days = 160 }
				}
				#7
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 70 compare = equals }
					}
					add_political_power = -140
					add_timed_idea = { idea = GER_mefo_bills_ended days = 180 }
				}
				#8
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 80 compare = equals }
					}
					add_political_power = -160
					add_timed_idea = { idea = GER_mefo_bills_ended days = 200 }
				}
				#9
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 90 compare = equals }
					}
					add_political_power = -180
					add_timed_idea = { idea = GER_mefo_bills_ended days = 220 }
				}
				#10
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 100 compare = equals }
					}
					add_political_power = -200
					add_timed_idea = { idea = GER_mefo_bills_ended days = 240 }
				}
				#11
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 110 compare = equals }
					}
					add_political_power = -220
					add_timed_idea = { idea = GER_mefo_bills_ended days = 260 }
				}
				#12
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 120 compare = equals }
					}
					add_political_power = -240
					add_timed_idea = { idea = GER_mefo_bills_ended days = 280 }
				}
				#13
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 130 compare = equals }
					}
					add_political_power = -260
					add_timed_idea = { idea = GER_mefo_bills_ended days = 300 }
				}
				#14
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 140 compare = equals }
					}
					add_political_power = -280
					add_timed_idea = { idea = GER_mefo_bills_ended days = 320 }
				}
				#15
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 150 compare = equals }
					}
					add_political_power = -300
					add_timed_idea = { idea = GER_mefo_bills_ended days = 340 }
				}
				#16
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 160 compare = equals }
					}
					add_political_power = -320
					add_timed_idea = { idea = GER_mefo_bills_ended days = 360 }
				}
				#17
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 170 compare = equals }
					}
					add_political_power = -340
					add_timed_idea = { idea = GER_mefo_bills_ended days = 380 }
				}
				#18
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 180 compare = equals }
					}
					add_political_power = -360
					add_timed_idea = { idea = GER_mefo_bills_ended days = 400 }
				}
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 180 compare = greater_than }
					}
					add_political_power = -380
					add_timed_idea = { idea = GER_mefo_bills_ended days = 420 }
				}
			}
			else = {
				custom_effect_tooltip = GER_mefo_bills_mission_tt
				custom_effect_tooltip = GER_mefo_bills_effect_in_days
				hidden_effect = {
					set_variable = { GER_extend_mefo_bills_days = days_mission_timeout@GER_mefo_bills_mission }
					set_country_flag = paid_for_mefo
				}
				GER_mefo_bills_level_up = yes
				if = {
					limit = {
						check_variable = { var = GER_mefo_bill_counter value = 15 compare = less_than }
					}
					hidden_effect = { set_variable = { var = GER_mefo_bill_counter value = 10 } }
				}
				add_to_variable = { var = GER_mefo_bill_counter value = 10 }

				hidden_effect = {
					activate_mission = GER_mefo_bills_mission
				}
			}
		}

		ai_will_do = {
			factor = 200
		}
	}

	GER_cancel_mefos = {

		icon = ger_mefo_bills

		available = {
			hidden_trigger = {
				NOT = { has_country_flag = ger_has_cancelled_mefo }
				NOT = {
					OR = {
						NOT = { GER_has_mefo_bills = yes }
						has_idea = GER_mefo_bills_ended
					}
				}
			}
		}

		cost = 0

		fire_only_once = no

		visible = {
			hidden_trigger = {
				NOT = { has_country_flag = ger_has_cancelled_mefo }
				NOT = {
					OR = {
						NOT = { GER_has_mefo_bills = yes }
						has_idea = GER_mefo_bills_ended
					}
				}
			}
		}

		cancel_if_not_visible = yes

		remove_effect = {
			set_country_flag = ger_has_cancelled_mefo
		}

		ai_will_do = {
			factor = 0
		}
	}

	GER_renew_mefos = {

		icon = ger_mefo_bills

		available = {
			hidden_trigger = {
				has_country_flag = ger_has_cancelled_mefo
				NOT = {
					OR = {
						NOT = { GER_has_mefo_bills = yes }
						has_idea = GER_mefo_bills_ended
					}
				}
			}
		}

		cost = 0

		fire_only_once = no

		visible = {
			hidden_trigger = {
				has_country_flag = ger_has_cancelled_mefo
				NOT = {
					OR = {
						NOT = { GER_has_mefo_bills = yes }
						has_idea = GER_mefo_bills_ended
					}
				}
			}
		}

		cancel_if_not_visible = yes

		remove_effect = {
			clr_country_flag = ger_has_cancelled_mefo
		}

		ai_will_do = {
			factor = 200
		}
	}
}

operations = {

	GER_barbarossa_mission = {

		icon = generic_operation

		allowed = {
			always = no
			#added through on_action
		}

		available = {
			219 = { is_controlled_by_ROOT_or_ally = yes }
			195 = { is_controlled_by_ROOT_or_ally = yes }
			202 = { is_controlled_by_ROOT_or_ally = yes }
			217 = { is_controlled_by_ROOT_or_ally = yes }
		}

		days_mission_timeout = 180
		fire_only_once = yes

		activation = {

		}

		is_good = no

		complete_effect = {
			add_war_support = 0.1
			custom_effect_tooltip = barbarossa_mission_tt
		}

		timeout_effect = {

		}

		ai_will_do = {
			factor = 1
		}
	}
}

GER_case_anton_category = {

	GER_case_anton = {

		icon = generic_operation

		available = {
			original_tag = GER
			has_war = yes
			has_government = fascism
			any_country_with_original_tag = {
				original_tag_to_check = FRA
				has_government = fascism
				OR = {
					is_subject_of = GER
					has_focus_tree = vichy_french_focus
				}
				NOT = { has_war_with = GER }
				NOT = { has_country_flag = case_anton }
				custom_trigger_tooltip = {
					tooltip = GER_case_anton_tt2
					count_triggers = {
						amount = 3 # lost control of ca half french north africa
						458 = { CONTROLLER = { has_war_with = ROOT } }
						459 = { CONTROLLER = { has_war_with = ROOT } }
						460 = { CONTROLLER = { has_war_with = ROOT } }
						461 = { CONTROLLER = { has_war_with = ROOT } }
						462 = { CONTROLLER = { has_war_with = ROOT } }
						513 = { CONTROLLER = { has_war_with = ROOT } }
						665 = { CONTROLLER = { has_war_with = ROOT } }
					}
				}
			}
			divisions_in_state = { state = 31 size < 1 }
			divisions_in_state = { state = 25 size < 1 }
			divisions_in_state = { state = 22 size < 1 }
			divisions_in_state = { state = 21 size < 1 }
			divisions_in_state = { state = 32 size < 1 }
			divisions_in_state = { state = 22 size < 1 }
			divisions_in_state = { state = 26 size < 1 }
			divisions_in_state = { state = 33 size < 1 }
			divisions_in_state = { state = 20 size < 1 }
			OR = {
				ITA = { owns_state = 735 }
				divisions_in_state = { state = 735 size < 1 }
			}
		}

		cost = 50
		fire_only_once = yes

		visible = {
			original_tag = GER
			has_government = fascism
			any_country_with_original_tag = {
				original_tag_to_check = FRA
				has_government = fascism
				OR = {
					is_subject_of = GER
					has_focus_tree = vichy_french_focus
				}
				NOT = { has_war_with = GER }
			}
		}
		ai_will_do = {
			factor = 25

			modifier = {
				factor = 0
				VIC = { is_ai = no }
			}
		}
		complete_effect = {
			custom_effect_tooltip = GER_case_anton_tt
			hidden_effect = {
				random_other_country = {
					limit = {
						original_tag = FRA
						has_government = fascism
						OR = {
							is_subject_of = GER
							has_focus_tree = vichy_french_focus
						}
					}
					set_country_flag = case_anton
					activate_mission = FRA_case_anton_mission
				}
			}
		}
	}
}

#Category only allowed for GER
GER_reichskommissariats = {
	GER_reichskommissariat_norwegen = {

		icon = ger_reichskommissariats

		available = {
			has_completed_focus = GER_form_the_reichskommissariats
			has_government = fascism
			controls_state = 110
			controls_state = 142
			controls_state = 143
			controls_state = 144
		}

		cost = 0

		fire_only_once = yes

		ai_will_do = {
			factor = 0
			modifier = {
				add = 1
				ENG = { has_capitulated = yes }
			}
		}

		visible = {
			has_completed_focus = GER_form_the_reichskommissariats
			has_government = fascism
		}

		complete_effect = {
			every_state = {
                limit = {
                    is_core_of = NOR
                    is_controlled_by = GER
                }
                set_compliance = 100
		    }
		}
	}

	GER_reichskommissariat_niederlande = {

		icon = ger_reichskommissariats

		available = {
			has_completed_focus = GER_form_the_reichskommissariats
			has_government = fascism
			controls_state = 7
			controls_state = 35
			controls_state = 36
		}

		cost = 0

		fire_only_once = yes

		ai_will_do = {
			factor = 0
			modifier = {
				add = 1
				ENG = { has_capitulated = yes }
			}
		}

		visible = {
			has_completed_focus = GER_form_the_reichskommissariats
			has_government = fascism
		}

		complete_effect = {
			every_state = {
                limit = {
                    is_core_of = HOL
                    is_controlled_by = GER
                }
                set_compliance = 100
		    }
		}
	}

	GER_reichskommissariat_belgien_nordfrankreich = {

		icon = ger_reichskommissariats

		available = {
			has_completed_focus = GER_form_the_reichskommissariats
			has_government = fascism
			controls_state = 6
			controls_state = 29
			controls_state = 34
		}

		cost = 0

		fire_only_once = yes

		ai_will_do = {
			factor = 0
			modifier = {
				add = 1
				ENG = { has_capitulated = yes }
			}
		}

		visible = {
			has_completed_focus = GER_form_the_reichskommissariats
			has_government = fascism
		}

		complete_effect = {
			every_state = {
                limit = {
                    is_core_of = BEL
                    is_controlled_by = GER
                }
                set_compliance = 100
			}
			29 = { set_compliance = 100 }
		}
		
	}
}


political_actions = {

	recall_von_lettow_vorbeck = {

		allowed = {
			original_tag = GER
		}
		available = {
			has_civil_war = no
		}
		visible = {
			OR = {
				has_country_leader = { ruling_only = yes name = "Wilhelm II" }
				has_country_leader = { ruling_only = yes name = "Wilhelm III" }
				has_country_leader = { ruling_only = yes name = "Victoria" }
			}
		}
		cost = 25
		fire_only_once = yes
		ai_will_do = {
			factor = 1
		}
		complete_effect = {
			create_corps_commander = {
				name = "Paul von Lettow-Vorbeck"
				gfx = GFX_portrait_ger_von_lettow_vorbeck
				traits = { trickster war_hero media_personality jungle_rat}
				skill = 4
				id = 499
				attack_skill = 3
				defense_skill = 3
				planning_skill = 2
				logistics_skill = 5
			}
		}
	}

}


#Category only allowed for GER
GER_military_buildup = {

	GER_plan_z = {

		icon = generic_naval

		available = {
			has_navy_size = {
				unit = battleship
				size > 9
			}
			has_navy_size = {
				unit = battle_cruiser
				size > 2
			}
			has_navy_size = {
				unit = carrier
				size > 3
			}
			has_navy_size = {
				unit = heavy_cruiser
				size > 19
			}
			has_navy_size = {
				unit = light_cruiser
				size > 19
			}
			has_navy_size = {
				unit = destroyer
				size > 99
			}
		}

		fire_only_once = yes
		days_mission_timeout = 1800
		is_good = no
		activation = {
			has_completed_focus = GER_plan_z
		}


		visible = {
			has_completed_focus = GER_plan_z
		}

		complete_effect = {
			add_war_support = 0.05
			navy_experience = 150
		}


	}

	GER_jaegernotprogramm = {

		icon = generic_air

		available = {
			has_war = yes
			AND = {
				has_deployed_air_force_size = {
					type = fighter
					size < 750
				}
				has_equipment = {
					fighter_equipment < 250
				}
			}
			NOT = {
				has_idea = GER_jaegernotprogramm
			}
		}

		cost = 50
		fire_only_once = yes
		ai_will_do = {
			factor = 1
		}

		visible = {
			has_war = yes
			AND = {
				has_deployed_air_force_size = {
					type = fighter
					size < 750
				}
				has_equipment = {
					fighter_equipment < 250
				}
			}
			NOT = {
				has_idea = GER_jaegernotprogramm
			}
		}

		complete_effect = {
			add_stability = -0.05
			add_war_support = -0.05
			add_timed_idea = { idea = GER_jaegernotprogramm days = 90 }
		}
	}
}

special_projects = {
	GER_begin_heavy_water_production = {
		allowed = {
			original_tag = GER
			has_dlc = "La Resistance"
		}
		available = {
			110 = {
				CONTROLLER = {
					OR = {
						tag = ROOT
						is_subject_of = ROOT
					}
				}
			}
		}
		visible = { has_tech = atomic_research }
		cost = 0
		ai_will_do = {
			factor = 5
		}
		cancel_trigger = { NOT = { has_global_flag = GER_heavy_water_production_underway } } #can be removed via intelligence ops
		days_remove = 365
		remove_effect = {
			add_tech_bonus = {
				name = GER_heavy_water
				category = nuclear
				uses = 2
				bonus = 2
			}
		}
		complete_effect = { set_global_flag = GER_heavy_water_production_underway }
	}
	GER_dismantle_maginot = {

		icon = generic_construction

		available = {
			#has_war = yes
			controls_state = 28
			if = {
				limit = {
					FRA = { has_completed_focus = FRA_extend_the_maginot_line }
				}
				controls_state = 18
				controls_state = 29
			}
		}

		cost = 50
		fire_only_once = yes

		ai_will_do = {
			factor = 0
		}
		visible = {
			#has_war = yes
			controls_state = 28
			if = {
				limit = {
					FRA = { has_completed_focus = FRA_extend_the_maginot_line }
				}
				controls_state = 18
				controls_state = 29
			}
		}
		days_remove = 180
		modifier = {
			civilian_factory_use = 5
		}
		remove_effect = {
			28 = {
				set_building_level = {
					type = bunker
					level = 2
					province = {
						all_provinces = yes
						limit_to_border = no
						level > 2
					}
				}
			}
			if = {
				limit = {
					FRA = { has_completed_focus = FRA_extend_the_maginot_line }
				}
				18 = {
					set_building_level = {
						type = bunker
						level = 2
						province = {
							all_provinces = yes
							limit_to_border = no
							level > 2
						}
					}
				}
				29 = {
					set_building_level = {
						type = bunker
						level = 2
						province = {
							all_provinces = yes
							limit_to_border = no
							level > 2
						}
					}
				}
			}
			if = {
				limit = {
					has_idea = FRA_protected_by_the_maginot_line
				}
				remove_ideas = FRA_protected_by_the_maginot_line
			}
		}
		complete_effect = {
			if = {
				limit = { FRA = { has_completed_focus = FRA_extend_the_maginot_line } }
				add_timed_idea = { idea = GER_dismantle_maginot days = 270 }
				else = {
					add_timed_idea = { idea = GER_dismantle_maginot days = 180 }
				}
			}
		}
	}
	GER_dismantle_czechoslovakian_forts = {

		icon = generic_construction

		available = {
			#has_war = yes
			controls_state = 69 # Sudetenland
			controls_state = 74 # Eastern Sudetenland
			controls_state = 9 # Bohemia
			controls_state = 75 # Moravia
		}

		cost = 50
		fire_only_once = yes

		ai_will_do = {
			factor = 0
		}
		visible = {
			#has_war = yes
			controls_state = 69 # Sudetenland
			controls_state = 74 # Eastern Sudetenland
			controls_state = 9 # Bohemia
			controls_state = 75 # Moravia
		}
		days_remove = 180
		modifier = {
			civilian_factory_use = 3
		}
		remove_effect = {
			69 = {
				set_building_level = {
					type = bunker
					level = 1
					province = {
						all_provinces = yes
						limit_to_border = no
						level > 1
					}
				}
			}
			74 = {
				set_building_level = {
					type = bunker
					level = 1
					province = {
						all_provinces = yes
						limit_to_border = no
						level > 1
					}
				}
			}
			9 = {
				set_building_level = {
					type = bunker
					level = 1
					province = {
						all_provinces = yes
						limit_to_border = no
						level > 1
					}
				}
			}
			75 = {
				set_building_level = {
					type = bunker
					level = 1
					province = {
						all_provinces = yes
						limit_to_border = no
						level > 1
					}
				}
			}
			if = {
				limit = {
					72 = {
						controller = {
							OR = {
								tag = ROOT
								is_subject_of = ROOT
							}
						}
					}
					71 = {
						controller = {
							OR = {
								tag = ROOT
								is_subject_of = ROOT
							}
						}
					}
				}
				72 = {
					set_building_level = {
						type = bunker
						level = 1
						province = {
							all_provinces = yes
							limit_to_border = no
							level > 1
						}
					}
				}
				71 = {
					set_building_level = {
						type = bunker
						level = 1
						province = {
							all_provinces = yes
							limit_to_border = no
							level > 1
						}
					}
				}
			}
			if = {
				limit = {
					70 = {
						controller = {
							OR = {
								tag = ROOT
								is_subject_of = ROOT
							}
						}
					}
				}
				70 = {
					set_building_level = {
						type = bunker
						level = 1
						province = {
							all_provinces = yes
							limit_to_border = no
							level > 1
						}
					}
				}
			}
			if = {
				limit = {
					73 = {
						controller = {
							OR = {
								tag = ROOT
								is_subject_of = ROOT
							}
						}
					}
					664 = {
						controller = {
							OR = {
								tag = ROOT
								is_subject_of = ROOT
							}
						}
					}
				}
				73 = {
					set_building_level = {
						type = bunker
						level = 1
						province = {
							all_provinces = yes
							limit_to_border = no
							level > 1
						}
					}
				}
				664 = {
					set_building_level = {
						type = bunker
						level = 1
						province = {
							all_provinces = yes
							limit_to_border = no
							level > 1
						}
					}
				}
			}
		}
		complete_effect = {
			add_timed_idea = { idea = GER_dismantle_czechoslovakian_forts days = 180 }
		}
	}
}
GER_BLAU = {
	GER_Egyptyanin = {

			icon = generic_construction

			available = {
				date > 1940.1.1
				date < 1940.6.1
			}

			cost = 1
			fire_only_once = yes

			ai_will_do = {
				factor = 0
			}
			visible = {
				always = yes
			}
			days_remove = 1

			complete_effect = {
			add_timed_idea = { idea = GER_Egyptyanin days = 90 }
		}
	}

	GER_fall_blau = {

			icon = generic_construction

			available = {
				date > 1942.4.1
				date < 1942.9.1
			}

			cost = 1
			fire_only_once = yes

			ai_will_do = {
				factor = 0
			}
			visible = {
				always = yes
			}
			days_remove = 1

			complete_effect = {
			add_timed_idea = { idea = GER_Fall_Blau days = 90 }
		}
	}

	GER_Citadel = {

			icon = generic_construction

			available = {
				date > 1943.6.1
				date < 1943.9.1
			}

			cost = 1
			fire_only_once = yes

			ai_will_do = {
				factor = 0
			}
			visible = {
				always = yes
			}
			days_remove = 1

			complete_effect = {
			add_timed_idea = { idea = GER_Citadel days = 90 }
		}
	}

	
	GER_iraq = {
		
			icon = oil
		
			available = {
				# eng fra dont control suez syria
				453 = {
					NOT = { is_controlled_by = ENG}
				}
				454 = {
					NOT = { is_controlled_by = ENG}
				}
				455 = {
					NOT = { is_controlled_by = ENG}
				}
				553 = {
					NOT = { is_controlled_by = FRA}
				}
				554 = {
					NOT = { is_controlled_by = FRA}
				}
				680 = {
					NOT = { is_controlled_by = FRA}
				}
				677 = {
					NOT = { is_controlled_by = FRA}
				}
				799 = {
					NOT = { is_controlled_by = FRA}
				}			
			}
		
			fire_only_once = yes
			days_remove    = -1
		
			complete_effect = {
				annex_country = { target = IRQ }
				every_state = {
					limit = {
						is_core_of = IRQ
						is_controlled_by = GER
						}
					add_compliance = 100
				}
				#675 = {
				#	add_resource = {
				#		type = oil
				#		amount = 50
				#	}
				#}			
			}
		}
		NO_ASIA
		{
		icon = generic_army_support
		
		available = {
				date > 1936.1.1 
			}

			fire_only_once = yes
			days_remove    = -1
		
		complete_effect = {
		ENG = {
				add_research_slot = 2
				add_offsite_building = { type = industrial_complex level = 70 }

				}
				
			351 = {
				add_resource = {
					type = aluminium
					amount = 250
				}
			}
			6320 = {
				add_resource = {
					type = aluminium
					amount = 250
				}
			}
			6320 = {
				add_resource = {
					type = rubber
					amount = 100
				}
			}
		}
		WST = {
			annex_country = { target = USA }
			annex_country = { target = JAP }
			annex_country = { target = CHI }
			transfer_state = 289
			transfer_state = 724
			transfer_state = 671
			transfer_state = 670
			transfer_state = 741
			transfer_state = 286
			transfer_state = 334
			transfer_state = 672
			transfer_state = 335
			transfer_state = 334
			transfer_state = 673
			transfer_state = 668
			transfer_state = 669
		}	
	}
}



		
			

				
			
		
		
		BLAU_MINI
		{
			icon = generic_army_support

			available = {
				date > 1936.1.1 
			}
		
			fire_only_once = yes
			days_remove    = -1
		
			complete_effect = {
				annex_country = { target = HUN }
				every_state = {
					limit = {
						is_core_of = HUN
						is_controlled_by = GER
						}
					add_core_of = GER

				}
	add_research_slot = 1
				annex_country = { target = ROM }
				every_state = {
					limit = {
						is_core_of = ROM
						is_controlled_by = GER
						}
					add_core_of = GER
				}	
	set_technology = {
                			fuel_refining2 = 1
					fuel_refining3 = 1
					fuel_refining4 = 1
				}			
				ENG = {
				add_research_slot = 1
					annex_country = {
						target = AST
						transfer_troops = yes
					}
					every_state = {
					limit = {
						is_core_of = AST
						is_controlled_by = ENG
						}
					add_core_of = ENG

								}
					annex_country = {
						target = RAJ
						transfer_troops = yes
					}
					every_state = {
					limit = {
						is_core_of = RAJ
						is_controlled_by = ENG
						}
					add_core_of = ENG

				}		
	annex_country = {
						target = CAN
						transfer_troops = yes
					}
					every_state = {
					limit = {
						is_core_of = CAN
						is_controlled_by = ENG
						}
					add_core_of = ENG

				}	
	annex_country = {
						target = NZL
						transfer_troops = yes
					}
					every_state = {
					limit = {
						is_core_of = NZL
						is_controlled_by = ENG
						}
					add_core_of = ENG

				}
	annex_country = {
						target = SAF
						transfer_troops = yes
					}
					every_state = {
					limit = {
						is_core_of = SAF
						is_controlled_by = ENG
						}
					add_core_of = ENG

				}			
				
				}
	ITA = {
				annex_country = {
						target = BUL
						transfer_troops = yes
					}
					every_state = {
					limit = {
						is_core_of = BUL
						is_controlled_by = ITA
						}
						add_core_of = ITA
		}
		
		
	}
}
		

