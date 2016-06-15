# finland--events
modifying in fin-scan war

event = {
id = 654987
random = no
country = FIN
style = 2
picture = "Vaino_Funeral"

trigger = { headofstate = 29001 }

date = { day = 29 month = may year = 1940 }

name = "The Death of The King"
desc = "The Funeral for King Vaino I of Finland was held today. The King died two days ago, on the 28th and died without making clear which of his sons will take the throne. The King's two twin sons, Philipp and Wolfgang have both shown interest in running the state after their father's death, although the King himself has shown more interest in Wolfgang as his heir, but made no clear statement regarding it."

action_a = {
ai_chance = 100
name = "The Eldest Twin, Philipp Takes the Throne!"
command = { type = headofstate which = 29035 }
command = { type = dissent value = 2 }
}
action_b = {
ai_chance = 0
name = "Crown Prince Wolfgang of Hesse is the heir!"
command = { type = headofstate which = 29036 }
command = { type = trigger which = 654901 }
command = { type = dissent value = 1 }
}
}

event = {
id = 654901
random = no
country = FIN
style = 2
picture = "Vaino_Funeral"

name = "The Lapua Movement's role in the government"
desc = "With the ascention of H.K.M. Moritz I to the throne, already questions are being raised about the Lapua Movement. While previously under Fredrik Kaarle I they led our nation, many are calling for the end of their rule and a parliamentary election to be held."

action_a = {
ai_chance = 80
name = "Dismiss the government and call an election!"
command = { type = set_domestic which = democratic value = 7 }
command = { type = set_domestic which = political_left value = 3 }
command = { type = headofstate which = 29036 }
command = { type = headofgovernment which = 29034 }
command = { type = dissent value = 3 }
}
action_b = {
ai_chance = 20
name = "They shall continue to guide our nation"
command = { type = dissent value = 5 }
command = { type = headofstate which = 29033 } #H.K.M. Moritz I
command = { type = sleepevent which = 654902 }

}
}

event = {
id = 654902
country = FIN
random = no
style = 2

trigger = {
OR = {
government = democratic
ideology = paternal_autocrat
}
event = 654901
}

name = "The parliamentary election of 1940"
desc = "The parliamentary election has been held and there are three parties that could win. The Social Democrats, the Agraian League, and the Young Finnnish Party. While previously forming the government of Finland, the Lapua Movement has lost much of it's support and has become a junior partner of a coalition with the Young Finnish Party. Who will win?"
picture = "rusdumaelect"

date = { day = 8 month = july year = 1940 }
offset = 2
deathdate = { day = 10 month = july year = 1940 }

action_a = {
ai_chance = 45
name = "The Social Democrats win!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29052 } #Mauno Pekkala
command = { type = foreignminister which = 29067 } #Anselmi Pitkäsilta
command = { type = armamentminister which = 29082 } #Viljam Sinisalo
command = { type = ministerofsecurity which = 29102 } #Urho K. Kekkonen
command = { type = ministerofintelligence which = 29120 } #Edvard Kajala
command = { type = set_domestic which = democratic value = 10 }
command = { type = set_domestic which = political_left value = 10 }
}
action_b = {
ai_chance = 30
name = "The Agrarian party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29032 } #Kaarlo Juho Stahlberg
command = { type = foreignminister which = 29071 } #Eino R. Holsti
command = { type = armamentminister which = 29086 } #Juho Niukkanen
command = { type = ministerofsecurity which = 29106 } #Richard Lorentz
command = { type = ministerofintelligence which = 29123 } #Hjalmar F. Procope
command = { type = set_domestic which = democratic value = 8 }
command = { type = set_domestic which = political_left value = 5 }
}
action_c = {
ai_chance = 25
name = "The Young Finnish Party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29034 } #Carl G. Mannerheim
command = { type = foreignminister which = 29078 } #Johan W. Rangell
command = { type = armamentminister which = 29091 } #Antti V. Hackzell
command = { type = ministerofsecurity which = 29113 } #Esko Riekki
command = { type = ministerofintelligence which = 29125 } #Yrjö W. Puhakka
command = { type = set_domestic which = democratic value = 7 }
command = { type = set_domestic which = political_left value = 4 }
}
}

event = {
id = 654903
country = FIN
random = no
style = 2

trigger = {
OR = {
government = democratic
ideology = paternal_autocrat
}
NOT = {
ispuppet = FIN
}
event = 654902
}

name = "The parliamentary election of 1944"
desc = "The parliamentary election has been held and there are three parties that could win. The Social Democrats, the Agraian League, and the Young Finnnish Party. Who will win?"
picture = "rusdumaelect"

date = { day = 12 month = august year = 1944 }
offset = 15
deathdate = { day = 12 month = september year = 1944 }

action_a = {
ai_chance = 45
name = "The Social Democrats win!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29052 } #Mauno Pekkala
command = { type = foreignminister which = 29067 } #Anselmi Pitkäsilta
command = { type = armamentminister which = 29082 } #Viljam Sinisalo
command = { type = ministerofsecurity which = 29102 } #Urho K. Kekkonen
command = { type = ministerofintelligence which = 29120 } #Edvard Kajala
command = { type = set_domestic which = democratic value = 10 }
command = { type = set_domestic which = political_left value = 10 }
}
action_b = {
ai_chance = 30
name = "The Agrarian party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29032 } #Kaarlo Juho Stahlberg
command = { type = foreignminister which = 29071 } #Eino R. Holsti
command = { type = armamentminister which = 29086 } #Juho Niukkanen
command = { type = ministerofsecurity which = 29106 } #Richard Lorentz
command = { type = ministerofintelligence which = 29123 } #Hjalmar F. Procope
command = { type = set_domestic which = democratic value = 8 }
command = { type = set_domestic which = political_left value = 5 }
}
action_c = {
ai_chance = 25
name = "The Young Finnish Party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29034 } #Carl G. Mannerheim
command = { type = foreignminister which = 29078 } #Johan W. Rangell
command = { type = armamentminister which = 29091 } #Antti V. Hackzell
command = { type = ministerofsecurity which = 29113 } #Esko Riekki
command = { type = ministerofintelligence which = 29125 } #Yrjö W. Puhakka
command = { type = set_domestic which = democratic value = 7 }
command = { type = set_domestic which = political_left value = 4 }
}
}

event = {
id = 654904
country = FIN
random = no
style = 2

trigger = {
OR = {
government = democratic
ideology = paternal_autocrat
}
NOT = {
ispuppet = FIN
}
}

name = "The parliamentary election of 1948"
desc = "The parliamentary election has been held and there are three parties that could win. The Social Democrats, the Agraian League, and the Young Finnnish Party. Who will win?"
picture = "rusdumaelect"

date = { day = 12 month = august year = 1948 }
offset = 15
deathdate = { day = 12 month = september year = 1948 }

action_a = {
ai_chance = 45
name = "The Social Democrats win!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29052 } #Mauno Pekkala
command = { type = foreignminister which = 29067 } #Anselmi Pitkäsilta
command = { type = armamentminister which = 29082 } #Viljam Sinisalo
command = { type = ministerofsecurity which = 29102 } #Urho K. Kekkonen
command = { type = ministerofintelligence which = 29120 } #Edvard Kajala
command = { type = set_domestic which = democratic value = 10 }
command = { type = set_domestic which = political_left value = 10 }
}
action_b = {
ai_chance = 30
name = "The Agrarian party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29051 } #Urho Kekkonen
command = { type = foreignminister which = 29071 } #Eino R. Holsti
command = { type = armamentminister which = 29086 } #Juho Niukkanen
command = { type = ministerofsecurity which = 29106 } #Richard Lorentz
command = { type = ministerofintelligence which = 29123 } #Hjalmar F. Procope
command = { type = set_domestic which = democratic value = 8 }
command = { type = set_domestic which = political_left value = 5 }
}
action_c = {
ai_chance = 35
name = "The Young Finnish Party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29061 } #Juho Kusti Paasikivi
command = { type = foreignminister which = 29078 } #Johan W. Rangell
command = { type = armamentminister which = 29091 } #Antti V. Hackzell
command = { type = ministerofsecurity which = 29113 } #Esko Riekki
command = { type = ministerofintelligence which = 29125 } #Yrjö W. Puhakka
command = { type = set_domestic which = democratic value = 7 }
command = { type = set_domestic which = political_left value = 4 }
}
}

event = {
id = 654905
country = FIN
random = no
style = 2

trigger = {
OR = {
government = democratic
ideology = paternal_autocrat
}
NOT = {
ispuppet = FIN
}
}

name = "The parliamentary election of 1952"
desc = "The next election is ready, who will win?"
picture = "rusdumaelect"

date = { day = 12 month = august year = 1952 }
offset = 15
deathdate = { day = 12 month = september year = 1952 }

action_a = {
ai_chance = 40
name = "The Social Democrats win!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29031 } #Väinö Tanner
command = { type = foreignminister which = 29067 } #Anselmi Pitkäsilta
command = { type = armamentminister which = 29082 } #Viljam Sinisalo
command = { type = ministerofsecurity which = 29102 } #Urho K. Kekkonen
command = { type = ministerofintelligence which = 29120 } #Edvard Kajala
command = { type = set_domestic which = democratic value = 10 }
command = { type = set_domestic which = political_left value = 10 }
}
action_b = {
ai_chance = 30
name = "The Agrarian party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29051 } #Urho Kekkonen
command = { type = foreignminister which = 29071 } #Eino R. Holsti
command = { type = armamentminister which = 29086 } #Juho Niukkanen
command = { type = ministerofsecurity which = 29106 } #Richard Lorentz
command = { type = ministerofintelligence which = 29123 } #Hjalmar F. Procope
command = { type = set_domestic which = democratic value = 8 }
command = { type = set_domestic which = political_left value = 5 }
}
action_c = {
ai_chance = 35
name = "The Young Finnish Party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29061 } #Juho Kusti Paasikivi
command = { type = foreignminister which = 29078 } #Johan W. Rangell
command = { type = armamentminister which = 29091 } #Antti V. Hackzell
command = { type = ministerofsecurity which = 29113 } #Esko Riekki
command = { type = ministerofintelligence which = 29125 } #Yrjö W. Puhakka
command = { type = set_domestic which = democratic value = 7 }
command = { type = set_domestic which = political_left value = 4 }
}
}

event = {
id = 654906
country = FIN
random = no
style = 2

trigger = {
OR = {
government = democratic
ideology = paternal_autocrat
}
NOT = {
ispuppet = FIN
}
}

name = "The parliamentary election of 1956"
desc = "The next election is ready, who will win?"
picture = "rusdumaelect"

date = { day = 12 month = august year = 1956 }
offset = 15
deathdate = { day = 12 month = september year = 1956 }

action_a = {
ai_chance = 40
name = "The Social Democrats win!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29031 } #Väinö Tanner
command = { type = foreignminister which = 29067 } #Anselmi Pitkäsilta
command = { type = armamentminister which = 29082 } #Viljam Sinisalo
command = { type = ministerofsecurity which = 29102 } #Urho K. Kekkonen
command = { type = ministerofintelligence which = 29120 } #Edvard Kajala
command = { type = set_domestic which = democratic value = 10 }
command = { type = set_domestic which = political_left value = 10 }
}
action_b = {
ai_chance = 30
name = "The Agrarian party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29051 } #Urho Kekkonen
command = { type = foreignminister which = 29071 } #Eino R. Holsti
command = { type = armamentminister which = 29086 } #Juho Niukkanen
command = { type = ministerofsecurity which = 29106 } #Richard Lorentz
command = { type = ministerofintelligence which = 29123 } #Hjalmar F. Procope
command = { type = set_domestic which = democratic value = 8 }
command = { type = set_domestic which = political_left value = 5 }
}
action_c = {
ai_chance = 35
name = "The Young Finnish Party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29061 } #Juho Kusti Paasikivi
command = { type = foreignminister which = 29078 } #Johan W. Rangell
command = { type = armamentminister which = 29091 } #Antti V. Hackzell
command = { type = ministerofsecurity which = 29113 } #Esko Riekki
command = { type = ministerofintelligence which = 29125 } #Yrjö W. Puhakka
command = { type = set_domestic which = democratic value = 7 }
command = { type = set_domestic which = political_left value = 4 }
}
}

event = {
id = 654907
country = FIN
random = no
style = 2

trigger = {
OR = {
government = democratic
ideology = paternal_autocrat
}
NOT = {
ispuppet = FIN
}
}

name = "The parliamentary election of 1960"
desc = "The next election is ready, who will win?"
picture = "rusdumaelect"

date = { day = 12 month = august year = 1960 }
offset = 15
deathdate = { day = 12 month = september year = 1960 }

action_a = {
ai_chance = 40
name = "The Social Democrats win!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29031 } #Väinö Tanner
command = { type = foreignminister which = 29067 } #Anselmi Pitkäsilta
command = { type = armamentminister which = 29082 } #Viljam Sinisalo
command = { type = ministerofsecurity which = 29102 } #Urho K. Kekkonen
command = { type = ministerofintelligence which = 29120 } #Edvard Kajala
command = { type = set_domestic which = democratic value = 10 }
command = { type = set_domestic which = political_left value = 10 }
}
action_b = {
ai_chance = 30
name = "The Agrarian party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29051 } #Urho Kekkonen
command = { type = foreignminister which = 29071 } #Eino R. Holsti
command = { type = armamentminister which = 29086 } #Juho Niukkanen
command = { type = ministerofsecurity which = 29106 } #Richard Lorentz
command = { type = ministerofintelligence which = 29123 } #Hjalmar F. Procope
command = { type = set_domestic which = democratic value = 8 }
command = { type = set_domestic which = political_left value = 5 }
}
action_c = {
ai_chance = 30
name = "The Young Finnish Party wins!"
command = { type = headofstate which = 29036 } #H.K.M. Moritz I
command = { type = headofgovernment which = 29061 } #Juho Kusti Paasikivi
command = { type = foreignminister which = 29078 } #Johan W. Rangell
command = { type = armamentminister which = 29091 } #Antti V. Hackzell
command = { type = ministerofsecurity which = 29113 } #Esko Riekki
command = { type = ministerofintelligence which = 29125 } #Yrjö W. Puhakka
command = { type = set_domestic which = democratic value = 7 }
command = { type = set_domestic which = political_left value = 4 }
}
}

event = {
id = 654988
random = no
country = FIN

name = "Black Monday hits Finland!"
desc = "Almost two weeks ago, the Berlin Stock Exchange plunged into bottomless depths, throwing Germany's economy into an unprecedented crisis. Now the crash's shockwaves have reached Finland. German-owned companies have closed down or laid-off their workers, the Finnish markka is losing value, and timber exports are shrinking..."
style = 2
picture = "economic"

date = { day = 21 month = february year = 1936 }

action_a = {
name = "The future looks bleak..."
command = { type = peacetime_ic_mod value = -10 }
command = { type = dissent value = 7 }
}
}


event = {
id = 654989
random = no
country = FIN

name = "The Lapua Party's economic policies."
desc = "More than a year after the economic breakdown, the situation has barely improved. By now even the Lapua party's most vocal supporters of the free market had to admit that the previous laissez-faire approach to the crisis has failed, and that measures have to be taken to lessen the plight of our people and stimulate the economy."
style = 2
picture = "Finnish Flag"

date = { day = 6 month = october year = 1937 }

action_a = {
name = "Start a series of economic expansion programs!"
ai_chance = 100
command = { type = trigger which = 654990 }
command = { type = sleepevent which = 654993 }
}
action_b = {
name = "Military expansion will stimulate our economy"
ai_chance = 0
command = { type = sleepevent which = 654990 }
}
action_c = {
name = "The free market will eventually solve the crisis"
ai_chance = 0
command = { type = dissent value = 5 }
command = { type = sleepevent which = 654993 }
command = { type = sleepevent which = 654990 }
}
}

event = {
id = 654990
random = no
country = FIN

name = "Industry or agriculture?"
desc = "Now that we have decided to expand Finland's economy, our government has to come up with a detailed plan for this endeavor. Considering our limited resources, we have to make a choice between whether to expand our agricultural production or the industrial base. While many in the Lapua movement had their roots in rural areas, one could hardly deny the importance of industrialization... "
style = 2
picture = "economic"

action_a = {
name = "The riches of Finland: expand farming and logging."
ai_chance = 0
command = { type = setflag which = FIN_agriculture }
command = { type = gain_tech which = 5030 }
command = { type = gain_tech which = 5040 }
command = { type = metalpool value = -1000 }
command = { type = energypool value = -1200 }
command = { type = supplies value = -1000 }
command = { type = money value = -120 }
}
action_b = {
name = "Indutry and mining create substantial growth."
ai_chance = 100
command = { type = setflag which = FIN_industry }
command = { type = gain_tech which = 5060 }
command = { type = gain_tech which = 5070 }
command = { type = metalpool value = -1600 }
command = { type = energypool value = -2000 }
command = { type = supplies value = -800 }
command = { type = money value = -250 }
}
}

event = {
id = 654991
random = no
country = FIN
trigger = {
flag = FIN_agriculture
}

name = "The growth of agriculture."
desc = "Our efforts have shown their first results. Agricultural output and efficiency have increased dramatically. While the economic crisis is not over yet, a ray of hope has appeared for our people. Finland can look towards a secure future."
style = 2
picture = "agriculture1"

date = { day = 1 month = december year = 1938 }
offset = 120
deathdate = { day = 29 month = december year= 1960 }

action_a = {
name = "The song our land shall sing."
command = { type = relative_manpower value = 10 }
command = { type = industrial_modifier which = total value = 3 }
command = { type = manpowerpool value = 25 }
command = { type = peacetime_ic_mod value = 4 }
command = { type = dissent value = -3 }
command = { type = clrflag which = FIN_agriculture }
}
}

event = {
id = 654992
random = no
country = FIN
trigger = {
flag = FIN_industry
}

name = "The growth of industry."
desc = "Our efforts have shown first results. Industrial output and efficiency have increased dramatically. While the economic crisis is not over yet, a ray of hope has appeared for our people. Finland can look towards a secure future."
style = 2
picture = "economic"

date = { day = 1 month = december year = 1938 }
offset = 100
deathdate = { day = 29 month = december year= 1960 }

action_a = {
name = "See! From our love once more shall grow!"
command = { type = add_prov_resource which = 520 value = 7 where = metal }
command = { type = add_prov_resource which = 521 value = 4 where = rare_materials }
command = { type = construct which = ic where = 525 value = 2 }
command = { type = construct which = ic where = 520 value = 1 }
command = { type = construct which = ic where = 521 value = 1 }
command = { type = peacetime_ic_mod value = 4 }
command = { type = clrflag which = FIN_industry }
}
}

event = {
id = 654993
random = no
country = FIN

name = "Military Expansion"
desc = "Our general staff has prepared several plans for military expansion. While our landforces are more than decent both in quality and quantity, our navy and airforce have not reached yet a satisfactory level."
style = 2
picture = "finnish_flag"

date = { day = 1 month = june year = 1938 }

action_a = {
name = "Expand the navy, every nation's pride!"
ai_chance = 60
command = { type = gain_tech which = 3070 } # destroyer
command = { type = gain_tech which = 3060 } # destroyer
command = { type = gain_tech which = 3160 } # light cruiser
command = { type = gain_tech which = 3260 } # heavy cruiser
command = { type = money value = -100 }
command = { type = peacetime_ic_mod value = 3 }
command = { type = trigger which = 654996 }
command = { type = belligerence which = FIN value = 3 }
command = { type = setflag which = Fin_Naval_expansion }
}
action_b = {
name = "Airplanes are the weapon of tomorrow!"
ai_chance = 40
command = { type = gain_tech which = 4030 } # interceptor
command = { type = gain_tech which = 4130 } # bomber
command = { type = gain_tech which = 4140 } # bomber
command = { type = money value = -100 }
command = { type = peacetime_ic_mod value = 3 }
command = { type = trigger which = 655001 }
command = { type = belligerence which = FIN value = 3 }
command = { type = setflag which = Fin_airforce_expansion }
}
}

event = {
id = 654994
random = no
country = FIN

trigger = {
NOT = {
ispuppet = FIN
}
flag = Fin_Naval_expansion
technology = { country = FIN value = 3070 }
}

date = { day = 1 month = june year = 1938 }
offset = 30
deathdate = { day = 29 month = december year = 1960 }

name = "The new destoryer fleet."
desc = "Our naval design bureaus have finally completed the plans for a new class of destroyers! Construction shall begin immediately!"
style = 2
picture = "dd_transfer"

action_a = {
name = "We shall rule the Baltic!"
ai_chance = 100
command = { type = build_division which = destroyer }
command = { type = build_division which = destroyer }
command = { type = peacetime_ic_mod value = 1 }
}
action_b = {
ai_chance = 0
name = "We changed our minds, cancel the construction!"
command = { type = dissent value = 4 }
}
}

event = {
id = 654995
random = no
country = FIN
trigger = {
NOT = {
ispuppet = FIN
}
flag = Fin_Naval_expansion
technology = { country = FIN value = 3260 }
}
name = "The new cruiser fleet."
desc = "Our naval design bureaus have finally completed the plans for a new class of heavy cruisers! Construction shall begin immediately!"
style = 2
picture = "RegiaMarina"

date = { day = 1 month = june year = 1938 }
offset = 30
deathdate = { day = 29 month = december year = 1960 }

action_a = {
name = "We shall rule the Baltic!"
ai_chance = 100
command = { type = build_division which = heavy_cruiser }
command = { type = build_division which = heavy_cruiser }
command = { type = peacetime_ic_mod value = 3 }
command = { type = clrflag which = Fin_Naval_expansion }
}
action_b = {
ai_chance = 0
name = "We changed our minds, cancel the construction!"
command = { type = dissent value = 5 }
}
}

event = {
id = 654996
random = no
country = FIN

trigger = {
NOT = {
ispuppet = GER
government = communist
ispuppet = FIN
}
exists = GER
NOT = {
war = { country = FIN country = GER }
}

}

name = "Purchasing a German battlecruiser?"
desc = "Even with our current naval expansion program, we still lack the capability and know-how to produce major capital ships. For now, we could overcome this gap by purchasing an older German battlecruiser. If the German Reich agrees, this ship would strenghten our navy tremedously."
style = 2
picture = "RegiaMarina"

action_a = {
name = "We'll make the kaiserliche Marine a good offer!"
ai_chance = 80
command = { type = trigger which = 654997 }
}
action_b = {
name = "Nonsense, we want ships made in Finland!"
ai_chance = 20
command = { }
}
}

event = {
id = 654997
random = no
country = GER

name = "Finland seeks to expand its navy"
desc = "Our close friend, the Kingdom of Finland, currently seeks to expand its naval forces. The Finns would like to buy one of our battlecruisers. Finland is friendly towards the Reich, and we could use the extra cash. On the other hand, some German politicans are worried about the Lapua movement's expansionistic policies."
style = 2
picture = "RegiaMarina"
action_a = {
name = "Verkauft! It's a deal!"
ai_chance = 80
command = { type = relation which = FIN value = 20 }
command = { type = remove_division which = 14500 value = 206 } # SMS Prinz Eitel Friedrich
command = { type = metalpool value = 1000 }
command = { type = energypool value = 800 }
command = { type = supplies value = 800 }
command = { type = money value = 120 }
command = { type = rarematerialspool value = 200 }
command = { type = trigger which = 654998 }
}
action_b = {
name = "Niemals! Those ships are mine!"
ai_chance = 20
command = { type = relation which = FIN value = -50 }
}
}

event = {
id = 654998
random = no
country = FIN

name = "The Finnish Navy's pride!"
desc = "Our friends in Berlin have agreed to our proposal, and transfered our new battlecruiser to Helsinki! While costly, our navy has gained tremendous strength! The new ship shall be called Uusimaa!"
style = 2
picture = "RegiaMarina"

action_a = {
name = "Long live Finland, proud and strong!"
command = { type = relation which = GER value = 20 }
command = { type = add_division which = "Uusimaa" value = battlecruiser when = 2 }
command = { type = metalpool value = -1000 }
command = { type = energypool value = -800 }
command = { type = supplies value = -800 }
command = { type = money value = -120 }
command = { type = rarematerialspool value = -200 }
}
}

event = {
id = 654999
random = no
country = FIN
trigger = {
NOT = {
ispuppet = FIN
}
flag = Fin_airforce_expansion
technology = { country = FIN value = 4030 }
}

name = "Expanding our airforce."
desc = "Our aeronautical engineers have finally completed the designs for a new interceptor! Construction shall begin immediately!"
style = 2
picture = "canplane"

date = { day = 1 month = june year = 1938 }
offset = 30
deathdate = { day = 29 month = december year = 1960 }

action_a = {
name = "Construct the interceptors!"
ai_chance = 100
command = { type = build_division which = interceptor }
command = { type = build_division which = interceptor }
command = { type = peacetime_ic_mod value = 2 }
}
action_b = {
ai_chance = 0
name = "We changed our mind, cancel the order!"
command = { type = dissent value = 5 }
}
}

event = {
id = 655000
random = no
country = FIN
trigger = {
NOT = {
ispuppet = FIN
}
flag = Fin_airforce_expansion
technology = { country = FIN value = 4130 }
technology = { country = FIN value = 4140 }
}

name = "Expanding our airforce."
desc = "Our aeronautical engineers have finally completed the designs for a new bomber! Construction shall begin immediately!"
style = 2
picture = "canplane"

date = { day = 1 month = june year = 1938 }
offset = 30
deathdate = { day = 29 month = december year = 1960 }

action_a = {
name = "Construct the bombers!"
ai_chance = 100
command = { type = build_division which = tactical_bomber }
command = { type = peacetime_ic_mod value = 3 }
}
action_b = {
ai_chance = 0
name = "We changed our mind, cancel the order!"
command = { type = dissent value = 5 }
}
}

event = {
id = 655001
random = no
country = FIN

trigger = {
NOT = {
ispuppet = GER
government = communist
ispuppet = FIN
}
exists = GER
NOT = {
war = { country = FIN country = GER }
}

}

name = "Purchasing German interceptors?"
desc = "Even with our current airforce expansion program, we still lack the capability and know-how to quickly produce aircraft. For now, we could overcome this gap by purchasing aircraft from Germany. If the German Reich agrees, this planes would strenghten our airforce tremedously."
style = 2
picture = "canplane"

action_a = {
name = "We'll make the Luftstreitkräfte a good offer!"
ai_chance = 80
command = { type = trigger which = 655002 }
}
action_b = {
name = "Buying German won't help our economy!"
ai_chance = 20
command = { }
}
}

event = {
id = 655002
random = no
country = GER

name = "Finland seeks to expand it's airforce"
desc = "Our close friend, the Kingdom of Finland, currently seeks to expand its airforce. The Finns would like to buy some of our airplanes. Finland is friendly towards the Reich, and we could use the extra cash. On the other hand, our general staff is worried about Syndicalist air superiority."
style = 2
picture = "canplane"

action_a = {
name = "Verkauft! It's a deal!"
ai_chance = 40                # a matter of game balance, to prevent total syndicalist air superiority
command = { type = relation which = FIN value = 20 }
command = { type = remove_division which = 14500 value = 134 } #
command = { type = remove_division which = 14500 value = 136 } #
command = { type = metalpool value = 1000 }
command = { type = energypool value = 800 }
command = { type = supplies value = 800 }
command = { type = money value = 120 }
command = { type = rarematerialspool value = 200 }
command = { type = trigger which = 655003 }
}
action_b = {
name = "Nein!"
ai_chance = 60
command = { type = relation which = FIN value = -50 }
}
}

event = {
id = 655003
random = no
country = FIN

name = "The Finnish airforce grows!"
desc = "Our friends in Berlin have agreed to our proposal, and transfered our new interceptors to Helsinki! While costly, our airforce has gained tremendous strength!"
style = 2
picture = "canplane"

action_a = {
name = "Long live Finland, proud and strong!"
command = { type = relation which = FIN value = 20 }
command = { type = add_division which = "Lentorykmentti 2" value = interceptor when = 8 }
command = { type = add_division which = "Lentorykmentti 3" value = interceptor when = 8 }
command = { type = metalpool value = -1000 }
command = { type = energypool value = -800 }
command = { type = supplies value = -800 }
command = { type = money value = -120 }
command = { type = rarematerialspool value = -200 }
}
}


###############
###  FINNISH-SWEDISH TENSION - ARILOU
##############

####Finnish Prerequisite event####

event = {
id = 654908
random = no
country = FIN
style = 2

trigger = {
exists = SWE
government = fascist
control = { province = 526 data = FIN }
control = { province = 525 data = FIN }
NOT = {
ispuppet = FIN
atwar = FIN
}
}

name = "The Swedish-Finnish minority question"
desc = "Finland contains within its borders a sizable Swedish-speaking minority that has come to be seen as outsiders. Under the pretext of purging foreign influences, many have considered revoking the special autonomy of the Swedish-speaking minority. While this would reinforce our national unity it could possibly spark conflicts with Sweden. What should we do?"
picture = "Aland"

date = { day = 1 month = january year = 1938 }
offset = 10
deathdate = { day = 29 month = december year = 1960 }


action_a = {
ai_chance = 69
name = "Revoke their rights!"
command = { type = dissent value = -5 }#Ultranationalists are mollified#
command = { type = domestic which = freedom value = -2 }
command = { type = relation which = SWE value = -50 }#Strained relations#
command = { type = trigger which = 654909 }
}

action_b = {
ai_chance = 31
name = "Let us not risk a conflict with our western brothers!"
command = { type = domestic which = freedom value = 2 }
command = { type = dissent value = 5 }
}
}

####Bourgesie track####
event = {
id = 654909
random = no
country = SWE
style = 2

trigger = {
control = { province = 2159 data = SWE }
NOT = {
ispuppet = SWE
atwar = SWE
}
}

name = "The Aland Affair"
desc = "After a hundred years of Russian occupation and two decades of independence, a significant Swedish-speaking minority still remains in the Finland, especially on the Aland archipelago. The new Finnish government's rather oppressive policy against the Swedish minority has given us an excellent opportunity to intervene.... "
picture = "Aland"


action_a = {
ai_chance = 80
name = "We must protect our countrymen on Aland!"
command = { type = end_non_aggression which = FIN where = SWE }
command = { type = end_non_aggression which = SWE where = FIN }
command = { type = addcore which = 526 }#Aland#
command = { type = domestic which = interventionism value = 1 }
command = { type = relation which = FIN value = -50 }
command = { type = trigger which = 654910 }
}

action_b = {
ai_chance = 20
name = "Bah! The finns can keep those worthless rocks!"
command = { type = domestic which = interventionism value = -1 }
command = { type = relation which = FIN value = 50 }
}
}


####Finnish response####

event = {
id = 654910
random = no
country = FIN
style = 2
picture = "Aland"

name = "The Swedes claim Aland"
desc = "The controversy over the Swedish minority has reached new heights! The Swedish government has demanded that Aland, with its large Swedish population, be handed over. Our ministers are divided. Some prefer handing the islands over directly, others an outright refusal. Some say we should let the Germans mediate our discussions."


action_a = {
ai_chance = 30
name = "We refuse listen to others meddling in our internal affairs!!"
command = { type = domestic which = defense_lobby value = 2 }
command = { type = relation which = SWE value = -50 }
command = { type = trigger which = 654911 }
}



action_b = {
ai_chance = 30
name = "Let the Germans mediate this dispute!"
trigger = {
exists = GER
control = { province = 163 data = GER }
NOT = {
ispuppet = GER
government = communist
}
}
command = { type = trigger which = 654912 }
command = { type = relation which = GER value = 50 }
}


action_c = {
ai_chance = 0
name = "Let's just give them the islands!"
command = { type = secedeprovince which = SWE value = 526 }
command = { type = relation which = SWE value = 50 }
command = { type = dissent value = 10 }
command = { type = domestic which = interventionism value = -2 }
command = { type = domestic which = defense_lobby value = -2 }
command = { type = trigger which = 654921 }
}

action_d = {
ai_chance = 20
name = "Let us restore the privilegies of their minority"
command = { type = trigger which = 654922 }
command = { type = relation which = SWE value = 50 }
command = { type = dissent value = 5 }
command = { type = domestic which = freedom value = 2 }
}
}



####Finnish refusal to negotiate####

event = {
id = 654911
random = no
country = SWE
style = 2



name = "The Finns refuse to negotiate!"
desc = "Despite our peaceful attempts to resolve the dispute over Aland and the Swedish-Finnish minority, Kosola's government is refusing to negoiate. At this point there are only two options: Back down or reach for our swords!"
picture = "Aland"


action_a = {
ai_chance = 30
name = "We must liberate our brothers! To war!"
command = { type = war which = FIN }
}

action_b = {
ai_chance = 10
name = "Let us back down"
command = { type = domestic which = interventionism value = -1 }
command = { type = domestic which = defense_lobby value = -2 }
command = { type = relation which = FIN value = 50 }
command = { type = removecore which = 526 }
}

action_c = {
ai_chance = 60
name = "Back down, but keep an eye on Aland"
command = { type = relation which = FIN value = -50 }
}
}



###German mediation###
###Reaction events to german mediation follows###

event = {
id = 654912
random = no
country = GER
style = 2


name = "Averting a war?"
desc = "It has come to our attention that the Finns and Swedes has come perilously close to a war over the Aland archipelago. Surprisingly the Kosola government has asked us to mediate the dispute. We could side with the Swedes, handing the archipelago over to them, or with the finns, letting them keep it. There is no guarantee that our ruling will sway the two countries and we would be obliged to support one. What should we do?"
picture = "Aland"


action_a = {
ai_chance = 40
name = "Stay out of this quagmire"
command = { type = domestic which = interventionism value = -1 }
command = { type = end_guarantee which = GER where = SWE }
command = { type = end_guarantee which = GER where = FIN }
command = { type = relation which = FIN value = -25 }
command = { type = trigger which = 654913 }
}

action_b = {
ai_chance = 40
name = "Rule in favour of Sweden!"
command = { type = guarantee which = GER where = SWE }
command = { type = end_guarantee which = GER where = FIN }
command = { type = relation which = SWE value = 50 }
command = { type = relation which = FIN value = -100 }
command = { type = trigger which = 654914 }
}

action_c = {
ai_chance = 20
name = "Rule in favour of Finland!"
command = { type = guarantee which = GER where = FIN }
command = { type = end_guarantee which = GER where = SWE }
command = { type = relation which = SWE value = -100 }
command = { type = relation which = FIN value = 50 }
command = { type = trigger which = 654916 }
}
}

###Germany refuses to get involved###

event = {
id = 654913
random = no
country = FIN
style = 2

name = "The Germans refuse to mediate"
desc = "Despite our pleas the German government has refused to mediate the Aland dispute. What should we do then?"
picture = "Aland"



action_a = {
ai_chance = 0
name = "It is no use! Let's hand the islands over!"
command = { type = secedeprovince which = SWE value = 526 }
command = { type = dissent value = 5 }
command = { type = domestic which = interventionism value = -1 }
command = { type = domestic which = defense_lobby value = -1 }
command = { type = trigger which = 654921 }
}

action_b = {
ai_chance = 40
name = "We refuse to negotiate any further!"
command = { type = domestic which = defense_lobby value = 2 }
command = { type = trigger which = 654911 }
}

action_c = {
ai_chance = 40
name = "Let us restore the Alanders' privileges!"
command = { type = trigger which = 654922 }
command = { type = dissent value = 5 }
command = { type = domestic which = freedom value = 2 }
}
}

###Germany supports Sweden###


event = {
id = 654914
random = no
country = FIN
style = 2


name = "Germany rules in favour of Sweden"
desc = "Disaster! The Germans have ruled in favour of the Swedes and demand that we hand over the archipelago! If we choose to refuse, we will fight a significantly stronger Sweden, and perhaps the Kaiserreich itself! What should we do?"
picture = "Wehrmacht"


action_a = {
ai_chance = 80
name = "The Germans are too dangerous, let's cave in!"
command = { type = secedeprovince which = SWE value = 526 } #Aland#
command = { type = domestic which = interventionism value = -1 }
command = { type = domestic which = defense_lobby value = -1 }
command = { type = trigger which = 654921 }
}

action_b = {
ai_chance = 20
name = "Damn the Germans! We will not give up an inch!"
command = { type = trigger which = 654915 }
command = { type = domestic which = interventionism value = 6 }
command = { type = domestic which = defense_lobby value = 6 } #Full war-footing#
}
}

###The Finns defy the german ruling###

event = {
id = 654915
random = no
country = SWE
style = 2

name = "The Finns defy the German ruling!"
desc = "Despite the German ruling the Finns have refused to hand the Aland archipelago over. The choice is now yours: War or peace?"
picture = "Wehrmacht"



action_a = {
ai_chance = 50
name = "WAR!"
command = { type = domestic which = interventionism value = 2 }
command = { type = domestic which = defense_lobby value = 2 }
command = { type = war which = FIN }
command = { type = trigger which = 654917 }
}

action_b = {
ai_chance = 0
name = "We abhor violence.... let us have peace."
command = { type = domestic which = interventionism value = -2 }
command = { type = domestic which = defense_lobby value = -2 }
command = { type = dissent value = 15 }
command = { type = removecore which = 526 }#Aland#
}

action_c = {
ai_chance = 50
name = "Back down, but keep an eye on Aland"
command = { type = relation which = FIN value = -50 }
}
}


###The Germans support Finland###

event = {
id = 654916
random = no
country = SWE
style = 2


name = "The Germans back Finland"
desc = "The German Empire has pledged it's support to the Finns: Pressing our claims on Aland would mean we would fight a significantly strengthened Finland, and even risk war with the Kaiserreich itself. What should we do?"
picture = "Wehrmacht"



action_a = {
ai_chance = 20
name = "The Germans are too dangerous; Back down."
command = { type = domestic which = interventionism value = -2 }
command = { type = domestic which = defense_lobby value = -2 }
command = { type = removecore which = 526 }
}

action_b = {
ai_chance = 10
name = "Damn the Germans! We go to war!"
command = { type = war which = FIN }
command = { type = trigger which = 654918 }
}

action_c = {
ai_chance = 80
name = "Back down, but keep an eye on Aland"
command = { type = relation which = FIN value = -50 }
}
}

###German support for Sweden###

event = {
id = 654917
random = no
country = GER
style = 2


name = "Swedish-Finnish war: Support for Sweden"
desc = "The Swedish-Finnish conflict has escalated into a full-blown war, we have pledged our support for the swedes, and it is now time to decide what form it will take."
picture = "Wehrmacht"

action_a = {
ai_chance = 50
name = "Send material and volunteers!"
command = { type = domestic which = interventionism value = 1 }
command = { type = supplies value = -2000 }
command = { type = money value = -200 }
command = { type = manpowerpool value = -50 }
command = { type = trigger which = 654919 }
}

action_b = {
ai_chance = 0
name = "Intervene directly!"
command = { type = alliance which = SWE }
command = { type = war which = FIN }
}

action_c = {
ai_chance = 50
name = "Do not intervene"
command = { type = dissent value = -1 }
command = { type = relation which = SWE value = -50 }
}
}

###German Support to Finland###

event = {
id = 654918
random = no
country = GER
style = 2


name = "Swedish-Finnish war: Support for Finland"
desc = "The Swedish-Finnish conflict has escalated into a full-blown war, we have pledged our support for the Finns, and it is now time to decide what form it will take."
picture = "Wehrmacht"

action_a = {
ai_chance = 50
name = "Send material and volunteers!"
command = { type = domestic which = interventionism value = 1 }
command = { type = supplies value = -2000 }
command = { type = money value = -200 }
command = { type = manpowerpool value = -50 }
command = { type = trigger which = 654920 }
}


action_b = {
ai_chance = 0
name = "Intervene directly!"
command = { type = alliance which = FIN }
command = { type = war which = SWE }
}

action_c = {
ai_chance = 50
name = "Do not intervene"
command = { type = dissent value = -1 }
command = { type = relation which = FIN value = -50 }
}
}

###German material support to Sweden###

event = {
id = 654919
random = no
country = SWE
style = 2

name = "German material support arrives"
desc = "The Germans have decided to support us in our war against Finland by sending us material and volunteers. This will strengthen us greatly!"
picture = "Wehrmacht"

action_a = {
name = "Excellent!"
command = { type = relation which = GER value = 100 }
command = { type = money value = 100 }
command = { type = supplies value = 1000 }
command = { type = add_corps which = "Deutsche Freiwillgkorps" value = land when = -1 where = 2159 }
command = { type = add_division which = "1 Freiwilligdivision" value = infantry when = 8 where = artillery }
command = { type = add_division which = "2. Freiwilligdivision" value = infantry when = 8 where = artillery }
}
}

###German material support to Finland###

event = {
id = 654920
random = no
country = FIN
style = 2

name = "German material support arrives"
desc = "The germans have decided to support us in our war against Sweden by sending us material and volunteers. This will strengthen us greatly!"
picture = "Wehrmacht"

action_a = {
name = "Excellent!"
command = { type = relation which = GER value = 100 }
command = { type = money value = 100 }
command = { type = supplies value = 1000 }
command = { type = add_corps which = "Deutsche Freiwillgkorps" value = land when = -1 where = 525 }
command = { type = add_division which = "1. Freiwilligdivision" value = infantry when = 8 where = artillery }
command = { type = add_division which = "2. Freiwilligdivision" value = infantry when = 8 where = artillery }
}
}

event = {
id = 654921
random = no
country = SWE
style = 2

name = "The Finns cave in."
desc = "The Finns have caved in to our demands and ceded Aland to us."
picture = "Aland"

action_a = {
name = "Wonderful!"
command = { type = construct which = ic where = 526 value = 1 }#Just so the island isn't totally worthless #
}
}

###The finns rescind their policies###


event = {
id = 654922
random = no
country = SWE
style = 2


name = "The Finns rescind their policies"
desc = "The Finns have chosen to rescind their policies and restored the privilegies of the swedish-speaking minority."
picture = "Aland"

action_a = {
ai_chance = 10
name = "How Nice! Then let us back down!"
command = { type = relation which = FIN value = 100 }
command = { type = removecore which = 526 }
}

action_b = {
ai_chance = 80
name = "Back down, but keep an eye on Aland"
command = { type = relation which = FIN value = -50 }
}

action_c = {
ai_chance = 0
name = "Too late! We go to war!"
command = { type = war which = FIN }
command = { type = belligerence which = SWE value = 10 }#Unprovoked war#
command = { type = relation which = GER value = -100 }
command = { type = relation which = RUS value = -100 }#Local big boys not amused#
command = { type = dissent value = 10 }
}
}


##### Swedish-Finnish war: Bourgesie track: Possibly resolutions#####


#####Swedes are victorious, no german support chain#####

event = {
id = 654923
random = no
country = SWE
style = 2

trigger = {
war = { country = FIN country = SWE }
control = { province = 2159 data = SWE }
OR = {
control = { province = 525 data = SWE }
AND = {
control = { province = 515 data = SWE }
control = { province = 516 data = SWE }
control = { province = 520 data = SWE }
}
}
NOT = {
ispuppet = SWE
ispuppet = FIN
alliance = { country = FIN country = GER }
alliance = { country = FIN country = RUS }
alliance = { country = FIN country = SOV }
alliance = { country = FIN country = FRA }
alliance = { country = SWE country = GER }
alliance = { country = SWE country = RUS }
alliance = { country = SWE country = SOV }
alliance = { country = SWE country = FRA }
}
}

name = "The Three Crowns Victorious!"
desc = "Our war against the Finns has been brought to an almost certain conclusion, we have now only to decide what demands to make of the finns."
picture = "urbanwarfare1"

date = { day = 1 month = january year = 1936 }
offset = 2
deathdate = { day = 29 month = december year = 1960 }

action_a = {
ai_chance = 50
name = "Let us demand Aland, as we originally planned."
command = { type = money value = 300 }
command = { type = addcore which = 526 }
command = { type = trigger which = 654924 }
}

action_b = {
ai_chance = 30
name = "Let us demand all Swedish-speaking areas!"
command = { type = money value = 100 }
command = { type = trigger which = 654925 }
command = { type = addcore which = 511 }#Aland#
command = { type = addcore which = 516 }#Abo#
command = { type = addcore which = 526 }#Vaasa#
command = { type = addcore which = 524 }#Tornio#
}

action_c = {
ai_chance = 0
name = "Let us go for total victory!"
command = { type = belligerence which = SWE value = 2 }
command = { type = addcore which = 511 }#Aland#
command = { type = addcore which = 516 }#Abo#
command = { type = addcore which = 526 }#Vaasa#
command = { type = addcore which = 524 }#Tornio#
}
}
#### Finnish Response to demands on Aland ####

event = {
id = 654924
random = no
country = FIN
style = 2

name = "The Swedes Demand Aland"
desc = "With our armies beaten in the field and our major cities in the hands of the swedes, they have nonetheless chosen to settle only for the Aland archipelago. Should we accept?"
picture = "politics2"

action_a = {
ai_chance = 90
name = "Yes, let us bring an end to this war!"
command = { type = secedeprovince which = SWE value = 525 } #Aland#
command = { type = domestic which = interventionism value = -6 }
command = { type = domestic which = defense_lobby value = -6 }
command = { type = domestic which = freedom value = 1 }
command = { type = trigger which = 654926 }
command = { type = peace which = SWE value = 0 }#Peace#
}

action_b = {
ai_chance = 10
name = "No! We must fight until the bitter end!"
command = { type = trigger which = 654928 }
command = { type = dissent value = 15 }
}
}

####The Swedes demand swedish-speaking Finland####

event = {
id = 654925
random = no
country = FIN
style = 2

name = "The Swedes demand Swedish-speaking Finland"
desc = "With our armies defeated in the field and our major cities in the hands of the enemy, the Swedes have decided to demand the provinces with the largest Swedish-speaking minorities. What should we do?"
picture = "politics2"

action_a = {
ai_chance = 70
name = "We have no choice but to hand them over!"
command = { type = secedeprovince which = SWE value = 511 }
command = { type = secedeprovince which = SWE value = 516 }
command = { type = secedeprovince which = SWE value = 526 }
command = { type = secedeprovince which = SWE value = 524 } #Swedish-speaking Finland -Helsinki + Tornea#
command = { type = domestic which = interventionism value = -6 }
command = { type = domestic which = defense_lobby value = -6 }
command = { type = domestic which = freedom value = 1 }
command = { type = trigger which = 654927 }
command = { type = peace which = SWE value = 0 }#Peace#
}

action_b = {
ai_chance = 30
name = "Never! We will fight to the bitter end!"
command = { type = trigger which = 654928 }
command = { type = dissent value = 10 }
}
}
####Sweden recieves Aland####

event = {
id = 654926
random = no
country = SWE
style = 2

name = "The Finns cede Aland"
desc = "Intimidated by our victories, the Finns have decided to cede Aland. Celebrations have sponteanously broken out in Stockholm at these joyuous news!"
picture = "politics2"

action_a = {
name = "Wondrous news!"
command = { type = set_relation which = FIN value = 25 }#Relations normalization#
command = { type = construct which = ic where = 526 value = 1 }#Just so the island isn't totally worthless #
}
}

####Sweden recieves Swedish-Speaking Finland####

event = {
id = 654927
random = no
country = SWE
style = 2

name = "The Finns hand over Swedish-speaking Finland"
desc = "After our glorious victory, the Finns have ceded the provinces with the largest Swedish-speaking minorities to us! Celebrations have been held in Stockholm at this joyous occasion!"
picture = "politics2"

action_a = {
name = "Excellent!"
command = { type = set_relation which = FIN value = -50 }
command = { type = construct which = ic where = 526 value = 1 }#Just so the island isn't totally worthless #
command = { type = belligerence which = SWE value = 2 }
}
}
####The Finns fight to the bitter end####

event = {
id = 654928
random = no
country = SWE
style = 2

name = "The Finns fight on!"
desc = "Despite our overwhelming military victory and our generous peace-terms the Finns have decided to fight on."
picture = "politics2"

action_a = {
name = "If it is war they want..."
command = { type = addcore which = 511 }#Aland#
command = { type = addcore which = 516 }#Abo#
command = { type = addcore which = 526 }#Vaasa#
command = { type = addcore which = 524 }#Tornio#
}

}

##########Finno-Swedish War: Finland Wins################

Event = {
id = 654929
random = no
country = FIN
style = 2

trigger = {
war = { country = FIN country = SWE }
control = { province = 525 data = FIN }
OR = {
control = { province = 2159 data = FIN }
AND = {
control = { province = 2166 data = FIN }
control = { province = 2167 data = FIN }
control = { province = 2165 data = FIN }
}
}
NOT = {
ispuppet = SWE
ispuppet = FIN
alliance = { country = SWE country = GER }
alliance = { country = SWE country = RUS }
alliance = { country = SWE country = SOV }
alliance = { country = SWE country = FRA }
alliance = { country = FIN country = GER }
alliance = { country = FIN country = RUS }
alliance = { country = FIN country = SOV }
alliance = { country = FIN country = FRA }
}
}

name = "The Lion Victorious!"
desc = "Our glorious armies has easily defeated the Swedes, and we are now in a position to make demands of them."
picture = "urbanwarfare1"

date = { day = 1 month = january year = 1936 }
offset = 2
deathdate = { day = 29 month = december year = 1960 }

action_a = {
ai_chance = 60
name = "Demand Norrbottens Lan, with its finnish-speaking minority!"
command = { type = addcore which = 2166 }
command = { type = addcore which = 2167 }#Norrbottens Lan#
command = { type = trigger which = 654934 }
}

action_b = {
ai_chance = 30
name = "Demand territories and install a government more to our liking!"
command = { type = addcore which = 2166 }
command = { type = addcore which = 2167 }#Norrbottens Lan#
command = { type = trigger which = 654930 }
command = { type = belligerence which = FIN value = 2 }
}

action_c = {
ai_chance = 10
name = "Let us push for total victory!"
command = { type = belligerence which = FIN value = 10 }
command = { type = addcore which = 2166 }
command = { type = addcore which = 2167 }#Norrbottens Lan#
command = { type = dissent value = 5 }
}
}

####Finland demands Norrbotten####

event = {
id = 654934
random = no
country = SWE
style = 2

name = "Finland demands Norrbotten!"
desc = "With our armies defeated and most of our major cities in the hands of the enemy, the Finns have offered us terms of surrender; They demand Norrbotten, including the rich iron-mines of Kiruna. Should we accept this?"
picture = "politics2"


action_a = {
ai_chance = 90
name = "We have no choice but to accept!"
command = { type = secedeprovince which = FIN value = 2166 }
command = { type = secedeprovince which = FIN value = 2167 }#Norrbotten#
command = { type = money value = -300 }
command = { type = trigger which = 654932 }
command = { type = peace which = FIN value = 0 }#Peace#
}

action_b = {
ai_chance = 10
name = "We will fight to the end!"
command = { type = dissent value = 15 }
command = { type = trigger which = 654931 }
}
}
###Finland demands swedish submission###

event = {
id = 654930
random = no
country = SWE
style = 2

name = "Finland demands our submission"
desc = "The finns have decisively beaten us in the field and most of our important cities are in their hands. They have offered us peace but on harsh terms: We must not only cede them Norrbotten with its Finnish minority, but they also reserve the right to appoint a new government.... One which will surely have their best interests at heart. What should we do?"
picture = "politics2"

action_a = {
ai_chance = 70
name = "We have no choice..."
command = { type = secedeprovince which = FIN value = 2166 }
command = { type = secedeprovince which = FIN value = 2167 }#Norrbotten#
command = { type = money value = -100 }
command = { type = trigger which = 654933 }
command = { type = peace which = FIN value = 0 }#Peace#
}

action_b = {
ai_chance = 30
name = "You can take our lives but you can never take our freedom!"
command = { type = dissent value = 15 }
command = { type = trigger which = 654931 }
}
}

###Sweden refuses finnish demands###

event = {
id = 654931
random = no
country = FIN
style = 2

name = "Sweden has refused our terms"
desc = "The Swedish government has refused our generous peace-terms. We have no choice but to continue the war."
picture = "politics2"

action_a = {
name = "So be it then!"
command = { type = dissent value = 3 }#longer war#
}
}

###Sweden cedes Norrbotten###

event = {
id = 654932
random = no
country = FIN
style = 2

name = "Sweden cedes Norrbotten"
desc = "The Swedes have caved in to our demands and ceded Norrbotten, with its Finnish-speaking minority, to us. Our entire country is celebrating this great achievement by our Great Leader!"
picture = "politics2"

action_a = {
name = "A great day!"
command = { type = dissent value = -5 }
}
}
###Sweden submits to Finland###

event = {
id = 654933
random = no
country = FIN
style = 2

name = "Sweden submits!"
desc = "After our glorious victory, Sweden has caved in and ceded us the territories we demanded, in addition they have allowed us to appoint their next government. These great news has caused spontaneous celebrations to erupt all over Finland, honouring our Great Leader!"
picture = "politics2"

action_a = {
name = "Excellent!"
command = { type = dissent value = -5 }
command = { type = make_puppet which = SWE }
}
}




################################
# Extending Ostwall
################################
event = {
id = 654935
random = no
country = FIN
save_date = yes

decision = {
OR = {
AND = {
exists = RUS
owned = { province = 553 data = RUS }
owned = { province = 572 data = RUS }
owned = { province = 1162 data = RUS }
control = { province = 553 data = RUS }
control = { province = 572 data = RUS }
control = { province = 1162 data = RUS }
NOT = {
exists = SOV
flag = RUS_ISO
alliance = { country = FIN country = RUS }
ispuppet = RUS
exists = SIB
exists = U13
}
}
AND = {
exists = SOV
owned = { province = 553 data = SOV }
owned = { province = 572 data = SOV }
owned = { province = 1162 data = SOV }
control = { province = 553 data = SOV }
control = { province = 572 data = SOV }
control = { province = 1162 data = SOV }
NOT = {
exists = RUS
flag = SOV_ISO
alliance = { country = FIN country = SOV }
ispuppet = SOV
exists = SIB
exists = U13
}
}
}
NOT = {
atwar = FIN
ispuppet = FIN
}
}

decision_trigger = {
OR = {
AND = {
control = { province = 530 data = FIN }
control = { province = 532 data = FIN }
control = { province = 538 data = FIN }
control = { province = 540 data = FIN }
control = { province = 519 data = FIN }
control = { province = 514 data = FIN }
control = { province = 517 data = FIN }
}
AND = {
control = { province = 530 data = FIN }
control = { province = 539 data = FIN }
control = { province = 541 data = FIN }
}
}
}

trigger = {
OR = {
AND = {
exists = RUS
owned = { province = 553 data = RUS }
owned = { province = 572 data = RUS }
owned = { province = 1162 data = RUS }
control = { province = 553 data = RUS }
control = { province = 572 data = RUS }
control = { province = 1162 data = RUS }
NOT = {
exists = SOV
flag = RUS_ISO
alliance = { country = FIN country = RUS }
ispuppet = RUS
exists = SIB
exists = U13
}
}
AND = {
exists = SOV
owned = { province = 553 data = SOV }
owned = { province = 572 data = SOV }
owned = { province = 1162 data = SOV }
control = { province = 553 data = SOV }
control = { province = 572 data = SOV }
control = { province = 1162 data = SOV }
NOT = {
exists = RUS
flag = SOV_ISO
alliance = { country = FIN country = SOV }
ispuppet = SOV
exists = SIB
exists = U13
}
}
}
NOT = {
atwar = FIN
ispuppet = FIN
}
OR = {
AND = {
control = { province = 530 data = FIN }
control = { province = 532 data = FIN }
control = { province = 538 data = FIN }
control = { province = 540 data = FIN }
control = { province = 519 data = FIN }
control = { province = 514 data = FIN }
control = { province = 517 data = FIN }
}
AND = {
control = { province = 530 data = FIN }
control = { province = 539 data = FIN }
control = { province = 541 data = FIN }
}
}
}

name = "Border fortification program"
desc = "With Russian armed forces emerging from previous years of neglect as fearsome force it is high time for us to improve our weak border defences. Our top military leaders propose to solve this situation via improving existing net of fortifications along borders with Russia, known as Mannerheim line. Once finished, such massive fortifications will surely stop any kind of Russian assault."
style = 2
picture = "Ostwall"
decision_picture = "decision_ostwall"

date = { day = 1 month = july year = 1938 }
offset = 40
deathdate = { day = 29 month = december year = 1963 }

action = {
name = "Launch Border fortification program!"
ai_chance = 90
command = { trigger = { ai = no } type = money value = -200 }
command = { trigger = { ai = no } type = metalpool value = -1500 }
command = { type = local_setflag which = FINost_const }
}

action = {
name = "This is not needed..."
ai_chance = 10
command = {  }
}
}




event = {
id = 654936
random = no
country = FIN
style = 2
save_date = yes
picture = "Ostwall"


trigger = {
event = { id = 654935 days = 250 }
local_flag = FINost_const
OR = {
AND = {
control = { province = 530 data = FIN }
control = { province = 532 data = FIN }
control = { province = 538 data = FIN }
control = { province = 540 data = FIN }
control = { province = 519 data = FIN }
control = { province = 514 data = FIN }
control = { province = 517 data = FIN }
}
AND = {
control = { province = 530 data = FIN }
control = { province = 539 data = FIN }
control = { province = 541 data = FIN }
}
}
OR = {
exists = RUS
exists = SOV
}
NOT = {
alliance = { country = FIN country = SOV }
alliance = { country = FIN country = RUS }
}
}

name = "Improving Border fortifications"
desc = "Our dilligent engineers and soldiers have completed another part of fortification line along borders of Finland with Russia. Shall we continue with its expansion or are such fortifications sufficient ?"

date = { day = 1 month = january year = 1936 }
offset = 40
deathdate = { day = 29 month = december year = 1963 }

action_a = {
name = "Further improve our defenses !"
ai_chance = 100
command = { trigger = { NOT = { control = { province = 539 data = FIN } control = { province = 541 data = FIN } } } type = construct which = land_fort where = 530 value = 1 }
command = { trigger = { NOT = { control = { province = 539 data = FIN } control = { province = 541 data = FIN } } } type = construct which = land_fort where = 532 value = 1 }
command = { trigger = { NOT = { control = { province = 539 data = FIN } control = { province = 541 data = FIN } } } type = construct which = land_fort where = 538 value = 1 }
command = { trigger = { control = { province = 539 data = FIN } } type = construct which = land_fort where = 539 value = 1 }
command = { trigger = { control = { province = 541 data = FIN } } type = construct which = land_fort where = 541 value = 1 }
command = { trigger = { ai = no } type = money value = -200 }
command = { trigger = { ai = no } type = metalpool value = -1500 }
command = { trigger = { ai = FIN NOT = { ai = RUS } } type = add_division value = infantry when = 9 }
command = { trigger = { ai = FIN NOT = { ai = RUS } } type = add_division value = infantry when = 9 }
}

action_b = {
name = "This is not needed..."
ai_chance = 0
command = { type = local_clrflag which = FINost_const }
}
}



event = {
id = 654937
random = no
country = FIN
style = 2
save_date = yes
picture = "Ostwall"


trigger = {
event = { id = 654936 days = 250 }
local_flag = FINost_const
alliance = { country = FIN country = GER }
OR = {
AND = {
control = { province = 530 data = FIN }
control = { province = 532 data = FIN }
control = { province = 538 data = FIN }
control = { province = 540 data = FIN }
control = { province = 519 data = FIN }
control = { province = 514 data = FIN }
control = { province = 517 data = FIN }
}
AND = {
control = { province = 530 data = FIN }
control = { province = 539 data = FIN }
control = { province = 541 data = FIN }
}
}
OR = {
exists = RUS
exists = SOV
}
NOT = {
alliance = { country = FIN country = SOV }
alliance = { country = FIN country = RUS }
}
}

name = "Improving Border fortifications"
desc = "Our dilligent engineers and soldiers have completed another part of fortification line along borders of Finland with Russia. Shall we continue with its expansion or are such fortifications sufficient ?"

date = { day = 1 month = january year = 1936 }
offset = 40
deathdate = { day = 29 month = december year = 1963 }

action_a = {
name = "Further improve our defenses !"
ai_chance = 80
command = { type = construct which = land_fort where = 530 value = 1 }
command = { type = construct which = land_fort where = 532 value = 1 }
command = { type = construct which = land_fort where = 538 value = 1 }
command = { trigger = { control = { province = 539 data = FIN } } type = construct which = land_fort where = 539 value = 1 }
command = { trigger = { control = { province = 541 data = FIN } } type = construct which = land_fort where = 541 value = 1 }
command = { type = construct which = land_fort where = 540 value = 1 }
command = { type = construct which = land_fort where = 519 value = 1 }
command = { type = construct which = land_fort where = 514 value = 1 }
command = { type = construct which = land_fort where = 517 value = 1 }
command = { trigger = { ai = no } type = money value = -300 }
command = { trigger = { ai = no } type = metalpool value = -1600 }
command = { trigger = { ai = FIN NOT = { ai = RUS } } type = add_division value = infantry when = 9 }
command = { trigger = { ai = FIN NOT = { ai = RUS } } type = add_division value = infantry when = 9 }
command = { type = dissent value = 2 }
}

action_b = {
name = "This is not needed..."
ai_chance = 20
command = { type = local_clrflag which = FINost_const }
command = { type = dissent value = -2 }
}
}


event = {
id = 654938
random = no
country = FIN
style = 2
save_date = yes
picture = "Ostwall"


trigger = {
event = { id = 654937 days = 250 }
local_flag = FINost_const
alliance = { country = FIN country = GER }
OR = {
AND = {
control = { province = 530 data = FIN }
control = { province = 532 data = FIN }
control = { province = 538 data = FIN }
control = { province = 540 data = FIN }
control = { province = 519 data = FIN }
control = { province = 514 data = FIN }
control = { province = 517 data = FIN }
}
AND = {
control = { province = 530 data = FIN }
control = { province = 539 data = FIN }
control = { province = 541 data = FIN }
}
}
OR = {
exists = RUS
exists = SOV
}
NOT = {
alliance = { country = FIN country = SOV }
alliance = { country = FIN country = RUS }
}
}

name = "Improving Border fortifications"
desc = "Our dilligent engineers and soldiers have completed another part of fortification line along borders of Finland with Russia. Shall we continue with its expansion or are such fortifications sufficient ?"

date = { day = 1 month = january year = 1936 }
offset = 40
deathdate = { day = 29 month = december year = 1963 }

action_a = {
name = "Further improve our defenses !"
ai_chance = 50
command = { type = construct which = land_fort where = 530 value = 1 }
command = { type = construct which = land_fort where = 532 value = 1 }
command = { type = construct which = land_fort where = 538 value = 1 }
command = { type = construct which = land_fort where = 540 value = 1 }
command = { type = construct which = land_fort where = 519 value = 1 }
command = { type = construct which = land_fort where = 514 value = 1 }
command = { type = construct which = land_fort where = 517 value = 1 }
command = { type = construct which = land_fort where = 531 value = 1 }
command = { type = construct which = land_fort where = 533 value = 1 }
command = { type = construct which = land_fort where = 528 value = 1 }
command = { type = construct which = land_fort where = 529 value = 1 }
command = { trigger = { control = { province = 539 data = FIN } } type = construct which = land_fort where = 539 value = 1 }
command = { trigger = { control = { province = 541 data = FIN } } type = construct which = land_fort where = 541 value = 1 }
command = { trigger = { ai = no } type = money value = -350 }
command = { trigger = { ai = no } type = metalpool value = -1900 }
command = { trigger = { ai = FIN NOT = { ai = RUS } } type = add_division value = infantry when = 9 }
command = { trigger = { ai = FIN NOT = { ai = RUS } } type = add_division value = infantry when = 9 }
command = { type = dissent value = 4 }
}

action_b = {
name = "This is not needed..."
ai_chance = 50
command = { type = local_clrflag which = FINost_const }
command = { type = dissent value = -4 }
}
}



event = {
id = 654939
random = no
country = FIN
style = 2
picture = "Ostwall"


trigger = {
event = { id = 654938 days = 250 }
local_flag = FINost_const
alliance = { country = FIN country = GER }
OR = {
AND = {
control = { province = 530 data = FIN }
control = { province = 532 data = FIN }
control = { province = 538 data = FIN }
control = { province = 540 data = FIN }
control = { province = 519 data = FIN }
control = { province = 514 data = FIN }
control = { province = 517 data = FIN }
}
AND = {
control = { province = 530 data = FIN }
control = { province = 539 data = FIN }
control = { province = 541 data = FIN }
}
}
OR = {
exists = RUS
exists = SOV
}
NOT = {
alliance = { country = FIN country = SOV }
alliance = { country = FIN country = RUS }
}
}

name = "Border fortification program completed"
desc = "Our dilligent engineers and soldiers have completed fortification line along borders of Finland with Russia. With such protections in place, our independence is secured."

date = { day = 1 month = january year = 1936 }
offset = 40
deathdate = { day = 29 month = december year = 1963 }

action_a = {
name = "Excellent !"
command = { type = construct which = land_fort where = 530 value = 1 }
command = { type = construct which = land_fort where = 532 value = 1 }
command = { type = construct which = land_fort where = 538 value = 1 }
command = { type = construct which = land_fort where = 540 value = 1 }
command = { type = construct which = land_fort where = 519 value = 1 }
command = { type = construct which = land_fort where = 514 value = 1 }
command = { type = construct which = land_fort where = 517 value = 1 }
command = { type = construct which = land_fort where = 531 value = 1 }
command = { type = construct which = land_fort where = 533 value = 1 }
command = { type = construct which = land_fort where = 528 value = 1 }
command = { type = construct which = land_fort where = 529 value = 1 }
command = { type = construct which = land_fort where = 520 value = 1 }
command = { type = construct which = land_fort where = 523 value = 1 }
command = { trigger = { control = { province = 539 data = FIN } } type = construct which = land_fort where = 539 value = 1 }
command = { trigger = { control = { province = 541 data = FIN } } type = construct which = land_fort where = 541 value = 1 }
command = { trigger = { ai = no } type = money value = -250 }
command = { trigger = { ai = no } type = metalpool value = -1700 }
command = { trigger = { ai = FIN NOT = { ai = RUS } } type = add_division value = infantry when = 9 }
command = { trigger = { ai = FIN NOT = { ai = RUS } } type = add_division value = infantry when = 9 }
command = { type = local_clrflag which = FINost_const }
}
}

######################654939################################################################654939#######################################################################################
######################654939################################################################654939#######################################################################################
######################654939################################################################654939#######################################################################################
######################654939################################################################654939#######################################################################################
######################654939################################################################654939#######################################################################################
######################654939################################################################654939#######################################################################################


####Finnish Prerequisite event####

event = {
id = 654940
random = no
country = FIN
style = 2

trigger = {
exists = SCA
flag = sca_synd
government = fascist
control = { province = 526 data = FIN }
control = { province = 525 data = FIN }
NOT = {
ispuppet = FIN
atwar = FIN
}
}

name = "The Swedish-Finnish minority question"
desc = "Syndicalist have taken control of both Norway and Sweden! This alarming turn of evenst calls for an immidiate and directed response to curtail syndicalist influence in our country, starting with the swedes of Aland"
picture = "Aland"

date = { day = 1 month = january year = 1938}
offset = 10
deathdate = { day = 29 month = december year = 1960 }


action_a = {
ai_chance = 100
name = "Revoke their rights!"
command = { type = dissent value = -5 }#Ultranationalists are mollified#
command = { type = domestic which = freedom value = -2 }
command = { type = relation which = SCA value = -50 }#Strained relations#
command = { type = trigger which = 654941 }
}

action_b = {
ai_chance = 0
name = "Let us not risk a conflict with our western brothers!"
command = { type = domestic which = freedom value = 2 }
command = { type = dissent value = 5 }
command = { type = trigger which = 654921 }
}
}

####Bourgesie track####
event = {
id = 654941
random = no
country = SCA
style = 2

trigger = {
control = { province = 2159 data = SCA }
NOT = {
ispuppet = SCA
atwar = SCA
}
}

name = "The Aland Affair"
desc = "The reactionary bourgeoise government of Finalnd has recently announced their intention to remove the rights of the swedish speaking minority within their borders, citing security concerns as their reasons. We must respond to defend the freedom of wour countrymen."
picture = "Aland"


action_a = {
ai_chance = 100
name = "We must protect our countrymen on Aland!"
command = { type = end_non_aggression which = FIN where = SCA }
command = { type = end_non_aggression which = SCA where = FIN }
command = { type = addcore which = 526 }#Aland#
command = { type = domestic which = interventionism value = 1 }
command = { type = relation which = FIN value = -50 }
command = { type = trigger which = 654942 }
}

action_b = {
ai_chance = 0
name = "Bah! The finns can keep those worthless rocks!"
command = { type = domestic which = interventionism value = -1 }
command = { type = relation which = FIN value = 50 }
command = { type = dissent value = 10 }
}
}


####Finnish response####

event = {
id = 654942
random = no
country = FIN
style = 2
picture = "Aland"

name = "The Syndicalists claim Aland"
desc = "The Scandinavian government has condemned our move against syndicalist forces in our nation and lain claim to the aland islands. how should we respond?"


action_a = {
ai_chance = 55
name = "We refuse listen to others meddling in our internal affairs!!"
command = { type = domestic which = defense_lobby value = 2 }
command = { type = relation which = SCA value = -50 }
command = { type = trigger which = 654943 }
}


action_b = {
ai_chance = 40
name = "Contact the Germans and ask for their backing"
trigger = {
exists = GER
control = { province = 163 data = GER }
NOT = {
ispuppet = GER
government = communist
}
}
command = { type = trigger which = 654944 }
}


action_c = {
ai_chance = 0
name = "Let's just give them the islands!"
command = { type = secedeprovince which = SCA value = 526 }
command = { type = relation which = SCA value = 50 }
command = { type = dissent value = 10 }
command = { type = domestic which = interventionism value = -2 }
command = { type = domestic which = defense_lobby value = -2 }
command = { type = trigger which = 654921 }
}

action_d = {
ai_chance = 5
name = "Let us restore the privilegies of their minority"
command = { type = trigger which = 654922 }
command = { type = relation which = SCA value = 50 }
command = { type = dissent value = 5 }
command = { type = domestic which = freedom value = 2 }
}
}



####Finnish refusal to negotiate####

event = {
id = 654943 
random = no
country = SCA
style = 2



name = "The Finns refuse to negotiate!"
desc = "Despite our peaceful attempts to resolve the dispute over Aland and the Swedish minority, Kosola's government is refusing to negoiate. We must now use other means to protect our comrades in Finland!"
picture = "Aland"


action_a = {
ai_chance = 60
name = "We must liberate our brothers! To war!"
command = { type = war which = FIN }
command = { type = trigger which = 654948 }
}

action_b = {
ai_chance = 10
name = "Let us back down"
command = { type = domestic which = interventionism value = -1 }
command = { type = domestic which = defense_lobby value = -2 }
command = { type = relation which = FIN value = 50 }
command = { type = removecore which = 526 }
}

action_c = {
ai_chance = 20
name = "Back down, but keep an eye on Aland"
command = { type = relation which = FIN value = -50 }
command = { type = setflag which = eyeonaland }
}
}

Germany gets involved

event = {
id = 654944
random = no
country = GER
style = 2


name = "Syndicalist agression in the north"
desc = "It has come to our attention that Syndicalist Scandinavia has threatened Finland with war over swedish rights on the aland islands, and the Finnish government has requested our support in case of a syndicalist invasion. how should we respond?"
picture = "Aland"


action_a = {
ai_chance = 5
name = "Its the Finns problem"
command = { type = domestic which = interventionism value = -1 }
command = { type = end_guarantee which = GER where = FIN }
command = { type = relation which = FIN value = -25 }
command = { type = dissent value = 5 }
command = { type = trigger which = 654945 }
}

action_b = {
ai_chance = 0
name = "The islands are swedish"
command = { type = end_guarantee which = GER where = FIN }
command = { type = relation which = SCA value = 50 }
command = { type = relation which = FIN value = -100 }
command = { type = trigger which = 654946 }
}

action_c = {
ai_chance = 80
name = "We must stop syndicalism"
command = { type = guarantee which = GER where = FIN }
command = { type = relation which = SCA value = -100 }
command = { type = relation which = FIN value = 50 }
command = { type = trigger which = 654947 }
}
}

event = {
id = 654945 
random = no
country = FIN
style = 2

name = "The Germans refuse to support us"
desc = "Despite our pleas the German government has refused to mediate the Aland dispute. What should we do then?"
picture = "Aland"



action_a = {
ai_chance = 0
name = "It is no use! Let's hand the islands over!"
command = { type = secedeprovince which = SCA value = 526 }
command = { type = dissent value = 5 }
command = { type = domestic which = interventionism value = -1 }
command = { type = domestic which = defense_lobby value = -1 }
command = { type = trigger which = 654921 }
}

action_b = {
ai_chance = 80
name = "We refuse to negotiate any further!"
command = { type = domestic which = defense_lobby value = 2 }
command = { type = trigger which = 654943 }
}

action_c = {
ai_chance = 20
name = "Let us restore the Alanders' privileges!"
command = { type = trigger which = 654922 }
command = { type = dissent value = 5 }
command = { type = domestic which = freedom value = 2 }
}
}

event = {
id = 654947 
random = no
country = SCA
style = 2


name = "The Germans back Finland"
desc = "The German Empire has pledged it's support to the Finns: Pressing our claims on Aland would mean we would fight a significantly strengthened Finland, and even risk war with the Kaiserreich itself. What should we do?"
picture = "Wehrmacht"



action_a = {
ai_chance = 19
name = "The Germans are too dangerous; Back down."
command = { type = domestic which = interventionism value = -2 }
command = { type = domestic which = defense_lobby value = -2 }
command = { type = removecore which = 526 }
}

action_b = {
ai_chance = 1
name = "Damn the Germans! We go to war!"
command = { type = war which = FIN }
command = { type = trigger which = 654918 }
}

action_c = {
ai_chance = 80
name = "Back down, but keep an eye on Aland"
command = { type = relation which = FIN value = -50 }
command = { type = setflag which = eyeonaland }
}
}

##########################################################################################################################################################################################
progress
##########################################################################################################################################################################################
progress
##########################################################################################################################################################################################



eevent = {
id = 654948 
random = no
country = FIN
style = 2

name = "Syndicalist attack!"
desc = "The Syndicalist swine have responded to our steadfastness by declaring war on us. Many in our government believe we can defeat them easily, but others think we should ask for german help."
picture = "Wehrmacht"

action_a = {
ai_chance = 40
name = "Finland will be victorious!"
command = { type = dissent value = -5 }
}

action_b = {
ai_chance = 60
name = "Contact the Germans"
command = { type = trigger which = 654948 }





