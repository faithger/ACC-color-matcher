import sys

class RGB:

def __init__(self, r, g, b):

self.r = r

self.g = g

self.b = b

def rgb_distance(color1, color2):

return sum((c1 - c2) ** 2 for c1, c2 in zip([color1.r, color1.g, color1.b], [color2.r, color2.g, color2.b]))

def find_closest_color(target_color, color_list):

closest_color = None

min_distance = sys.maxsize

for color_name, color_rgb in color_list.items():

distance = rgb_distance(target_color, color_rgb)

if distance < min_distance:

min_distance = distance

closest_color = color_name

return closest_color

#The colos you have chosen. You need to take the RGB values of the chosen color, decide on a name #and put it in this format: 'Name': RGB(Value1, Value2, Value3),
#If you can't do it, ask ChatGPT or comment on this post.

target_colors = {

'Golden Yellow': RGB(255, 215, 0),

'Royal Blue': RGB(65, 105, 225),

'Radiant White': RGB(255, 255, 255),

'Mustard': RGB(255, 173, 1),

'Sapphire Blue': RGB(0, 56, 168),

'Chrome Yellow': RGB(255, 205, 0),

}

# ACC Color list

reference_colors = {

'Color 1': RGB(3, 2, 2),

'Color 2': RGB(39, 49, 54),

'Color 3': RGB(38, 20, 15),

'Color 4': RGB(48, 35, 39),

'Color 5': RGB(31, 53, 57),

'Color 6': RGB(56, 45, 45),

'Color 7': RGB(63, 53, 54),

'Color 8': RGB(58, 57, 55),

'Color 9': RGB(68, 59, 60),

'Color 10': RGB(74, 68, 68),

'Color 11': RGB(79, 72, 73),

'Color 12': RGB(85, 79, 80),

'Color 13': RGB(92, 87, 87),

'Color 14': RGB(98, 93, 93),

'Color 15': RGB(102, 99, 98),

'Color 16': RGB(109, 105, 104),

'Color 17': RGB(115, 110, 109),

'Color 18': RGB(116, 111, 110),

'Color 19': RGB(132, 127, 125),

'Color 20': RGB(133, 133, 131),

'Color 21': RGB(184, 184, 182),

'Color 22': RGB(210, 209, 208),

'Color 23': RGB(230, 229, 227),

'Color 24': RGB(190, 200, 206),

'Color 25': RGB(154, 177, 201),

'Color 26': RGB(109, 124, 142),

'Color 27': RGB(101, 116, 132),

'Color 28': RGB(97, 109, 127),

'Color 29': RGB(100, 109, 127),

'Color 30': RGB(85, 109, 127),

'Color 31': RGB(116, 125, 163),

'Color 32': RGB(70, 99, 162),

'Color 33': RGB(38, 83, 127),

'Color 34': RGB(38, 53, 85),

'Color 35': RGB(13, 20, 83),

'Color 36': RGB(0, 0, 129),

'Color 37': RGB(48, 40, 127),

'Color 38': RGB(13, 45, 127),

'Color 39': RGB(13, 20, 142),

'Color 40': RGB(0, 0, 162),

'Color 41': RGB(0, 26, 196),

'Color 42': RGB(0, 63, 196),

'Color 43': RGB(31, 83, 201),

'Color 44': RGB(13, 105, 201),

'Color 45': RGB(38, 96, 223),

'Color 46': RGB(25, 67, 253),

'Color 47': RGB(105, 96, 237),

'Color 48': RGB(116, 106, 255),

'Color 49': RGB(49, 127, 201),

'Color 50': RGB(51, 140, 195),

'Color 51': RGB(70, 139, 201),

'Color 52': RGB(44, 145, 201),

'Color 53': RGB(101, 160, 201),

'Color 54': RGB(163, 177, 201),

'Color 55': RGB(150, 187, 201),

'Color 56': RGB(115, 144, 208),

'Color 57': RGB(38, 101, 237),

'Color 58': RGB(44, 110, 255),

'Color 59': RGB(13, 126, 237),

'Color 60': RGB(13, 126, 237),

'Color 61': RGB(100, 150, 238),

'Color 62': RGB(102, 154, 255),

'Color 63': RGB(53, 174, 237),

'Color 64': RGB(85, 167, 237),

'Color 65': RGB(92, 181, 255),

'Color 66': RGB(56, 187, 255),

'Color 67': RGB(122, 188, 237),

'Color 68': RGB(131, 204, 251),

'Color 69': RGB(131, 204, 255),

'Color 70': RGB(162, 209, 237),

'Color 71': RGB(185, 208, 237),

'Color 72': RGB(182, 209, 237),

'Color 73': RGB(196, 224, 255),

'Color 74': RGB(200, 223, 255),

'Color 75': RGB(177, 221, 237),

'Color 76': RGB(175, 224, 255),

'Color 77': RGB(191, 238, 255),

'Color 78': RGB(209, 237, 237),

'Color 79': RGB(225, 255, 255),

'Color 80': RGB(236, 245, 251),

'Color 81': RGB(241, 249, 255),

'Color 82': RGB(241, 255, 255),

'Color 83': RGB(206, 255, 255),

'Color 84': RGB(148, 255, 233),

'Color 85': RGB(156, 255, 255),

'Color 86': RGB(128, 255, 213),

'Color 87': RGB(0, 255, 255),

'Color 88': RGB(126, 254, 255),

'Color 89': RGB(86, 255, 255),

'Color 90': RGB(143, 236, 237),

'Color 91': RGB(79, 236, 237),

'Color 92': RGB(77, 227, 237),

'Color 93': RGB(130, 217, 209),

'Color 94': RGB(147, 201, 201),

'Color 95': RGB(120, 193, 201),

'Color 96': RGB(121, 201, 201),

'Color 97': RGB(70, 206, 207),

'Color 98': RGB(65, 200, 220),

'Color 99': RGB(68, 201, 201),

'Color 100': RGB(124, 206, 183),

'Color 101': RGB(65, 193, 201),

'Color 102': RGB(59, 171, 161),

'Color 103': RGB(56, 158, 158),

'Color 104': RGB(65, 142, 129),

'Color 105': RGB(48, 136, 130),

'Color 106': RGB(44, 126, 127),

'Color 107': RGB(94, 126, 127),

'Color 108': RGB(74, 121, 127),

'Color 109': RGB(0, 129, 129),

'Color 110': RGB(77, 138, 118),

'Color 111': RGB(121, 135, 107),

'Color 112': RGB(133, 140, 122),

'Color 113': RGB(97, 125, 87),

'Color 114': RGB(115, 141, 0),

'Color 115': RGB(102, 125, 33),

'Color 116': RGB(31, 63, 15),

'Color 117': RGB(44, 103, 83),

'Color 118': RGB(48, 115, 49),

'Color 119': RGB(65, 125, 15),

'Color 120': RGB(53, 125, 66),

'Color 121': RGB(48, 125, 39),

'Color 122': RGB(48, 125, 15),

'Color 123': RGB(48, 129, 15),

'Color 124': RGB(77, 147, 87),

'Color 125': RGB(106, 163, 27),

'Color 126': RGB(72, 162, 39),

'Color 127': RGB(63, 165, 15),

'Color 128': RGB(59, 162, 84),

'Color 129': RGB(108, 189, 57),

'Color 130': RGB(108, 198, 15),

'Color 131': RGB(74, 198, 15),

'Color 132': RGB(81, 209, 15),

'Color 133': RGB(74, 199, 81),

'Color 134': RGB(83, 199, 114),

'Color 135': RGB(155, 200, 143),

'Color 136': RGB(138, 197, 92),

'Color 137': RGB(134, 189, 101),

'Color 138': RGB(140, 181, 130),

'Color 139': RGB(158, 178, 114),

'Color 140': RGB(180, 196, 70),

'Color 141': RGB(159, 196, 2),

'Color 142': RGB(163, 203, 49),

'Color 143': RGB(128, 233, 15),

'Color 144': RGB(88, 233, 15),

'Color 145': RGB(86, 234, 100),

'Color 146': RGB(100, 234, 135),

'Color 147': RGB(94, 252, 110),

'Color 148': RGB(0, 255, 0),

'Color 149': RGB(95, 252, 15),

'Color 150': RGB(136, 248, 15),

'Color 151': RGB(139, 252, 15),

'Color 152': RGB(106, 252, 147),

'Color 153': RGB(154, 255, 154),

'Color 154': RGB(183, 235, 172),

'Color 155': RGB(197, 254, 186),

'Color 156': RGB(206, 252, 93),

'Color 157': RGB(179, 252, 15),

'Color 158': RGB(190, 234, 83),

'Color 159': RGB(238, 219, 117),

'Color 160': RGB(238, 227, 118),

'Color 161': RGB(255, 233, 125),

'Color 162': RGB(255, 255, 0),

'Color 163': RGB(255, 244, 129),

'Color 164': RGB(255, 255, 196),

'Color 165': RGB(255, 255, 206),

'Color 166': RGB(255, 249, 200),

'Color 167': RGB(255, 249, 221),

'Color 168': RGB(246, 246, 221),

'Color 169': RGB(252, 247, 218),

'Color 170': RGB(251, 236, 216),

'Color 171': RGB(248, 232, 208),

'Color 172': RGB(255, 236, 207),

'Color 173': RGB(244, 230, 173),

'Color 174': RGB(237, 230, 184),

'Color 175': RGB(255, 230, 182),

'Color 176': RGB(255, 220, 87),

'Color 177': RGB(255, 217, 0),

'Color 178': RGB(254, 209, 15),

'Color 179': RGB(235, 195, 15),

'Color 180': RGB(243, 189, 102),

'Color 181': RGB(252, 187, 15),

'Color 182': RGB(252, 179, 15),

'Color 183': RGB(255, 168, 43),

'Color 184': RGB(234, 173, 15),

'Color 185': RGB(227, 169, 111),

'Color 186': RGB(223, 186, 136),

'Color 187': RGB(255, 205, 166),

'Color 188': RGB(203, 192, 98),

'Color 189': RGB(233, 165, 15),

'Color 190': RGB(239, 156, 76),

'Color 191': RGB(202, 183, 96),

'Color 192': RGB(213, 162, 15),

'Color 193': RGB(196, 180, 129),

'Color 194': RGB(201, 165, 15),

'Color 195': RGB(200, 143, 15),

'Color 196': RGB(183, 168, 64),

'Color 197': RGB(175, 171, 110),

'Color 198': RGB(195, 156, 107),

'Color 199': RGB(207, 128, 46),

'Color 200': RGB(202, 130, 63),

'Color 201': RGB(199, 138, 15),

'Color 202': RGB(177, 157, 96),

'Color 203': RGB(177, 121, 15),

'Color 204': RGB(186, 116, 47),

'Color 205': RGB(151, 111, 47),

'Color 206': RGB(129, 101, 15),

'Color 207': RGB(131, 121, 54),

'Color 208': RGB(131, 124, 96),

'Color 209': RGB(121, 109, 95),

'Color 210': RGB(71, 58, 33),

'Color 211': RGB(70, 57, 46),

'Color 212': RGB(111, 77, 52),

'Color 213': RGB(132, 92, 56),

'Color 214': RGB(128, 81, 15),

'Color 215': RGB(128, 68, 39),

'Color 216': RGB(198, 117, 80),

'Color 217': RGB(197, 98, 63),

'Color 218': RGB(197, 87, 15),

'Color 219': RGB(202, 89, 15),

'Color 220': RGB(206, 102, 0),

'Color 221': RGB(230, 103, 15),

'Color 222': RGB(231, 108, 39),

'Color 223': RGB(249, 115, 15),

'Color 224': RGB(249, 117, 45),

'Color 225': RGB(231, 117, 80),

'Color 226': RGB(255, 129, 61),

'Color 227': RGB(249, 129, 15),

'Color 228': RGB(255, 128, 79),

'Color 229': RGB(249, 130, 87),

'Color 230': RGB(250, 151, 107),

'Color 231': RGB(232, 139, 97),

'Color 232': RGB(226, 140, 107),

'Color 233': RGB(232, 117, 114),

'Color 234': RGB(248, 93, 88),

'Color 235': RGB(230, 83, 80),

'Color 236': RGB(230, 90, 57),

'Color 237': RGB(255, 0, 0),

'Color 238': RGB(255, 30, 0),

'Color 239': RGB(247, 28, 15),

'Color 240': RGB(248, 4, 19),

'Color 241': RGB(247, 35, 15),

'Color 242': RGB(229, 28, 15),

'Color 243': RGB(229, 20, 15),

'Color 244': RGB(221, 53, 25),

'Color 245': RGB(197, 72, 39),

'Color 246': RGB(196, 68, 63),

'Color 247': RGB(194, 61, 0),

'Color 248': RGB(195, 20, 15),

'Color 249': RGB(161, 0, 6),

'Color 250': RGB(155, 0, 9),

'Color 251': RGB(141, 0, 19),

'Color 252': RGB(150, 67, 49),

'Color 253': RGB(127, 49, 15),

'Color 254': RGB(139, 63, 15),

'Color 255': RGB(127, 53, 15),

'Color 256': RGB(129, 0, 15),

'Color 257': RGB(130, 0, 63),

'Color 258': RGB(126, 0, 63),

'Color 259': RGB(127, 49, 76),

'Color 260': RGB(126, 0, 81),

'Color 261': RGB(128, 77, 81),

'Color 262': RGB(128, 89, 87),

'Color 263': RGB(128, 81, 93),

'Color 264': RGB(181, 133, 130),

'Color 265': RGB(199, 145, 143),

'Color 266': RGB(198, 130, 138),

'Color 267': RGB(198, 136, 148),

'Color 268': RGB(233, 175, 172),

'Color 269': RGB(237, 199, 194),

'Color 270': RGB(238, 203, 177),

'Color 271': RGB(254, 216, 229),

'Color 272': RGB(253, 224, 255),

'Color 273': RGB(255, 224, 222),

'Color 274': RGB(252, 189, 187),

'Color 275': RGB(251, 177, 198),

'Color 276': RGB(251, 177, 188),

'Color 277': RGB(250, 169, 178),

'Color 278': RGB(232, 163, 178),

'Color 279': RGB(232, 155, 165),

'Color 280': RGB(228, 139, 176),

'Color 281': RGB(248, 121, 163),

'Color 282': RGB(230, 110, 149),

'Color 283': RGB(247, 96, 173),

'Color 284': RGB(253, 108, 134),

'Color 285': RGB(247, 49, 139),

'Color 286': RGB(246, 35, 136),

'Color 287': RGB(229, 94, 159),

'Color 288': RGB(229, 35, 125),

'Color 289': RGB(246, 49, 172),

'Color 290': RGB(255, 0, 255),

'Color 291': RGB(228, 45, 159),

'Color 292': RGB(245, 47, 255),

'Color 293': RGB(210, 101, 136),

'Color 294': RGB(196, 89, 125),

'Color 295': RGB(204, 28, 107),

'Color 296': RGB(195, 35, 105),

'Color 297': RGB(195, 28, 103),

'Color 298': RGB(196, 81, 132),

'Color 299': RGB(195, 28, 132),

'Color 300': RGB(187, 56, 144),

'Color 301': RGB(127, 87, 127),

'Color 302': RGB(86, 20, 127),

'Color 303': RGB(87, 52, 88),

'Color 304': RGB(73, 0, 131),

'Color 305': RGB(68, 20, 127),

'Color 306': RGB(77, 53, 127),

'Color 307': RGB(97, 61, 80),

'Color 308': RGB(94, 89, 129),

'Color 309': RGB(106, 35, 127),

'Color 310': RGB(126, 20, 127),

'Color 311': RGB(169, 72, 201),

'Color 312': RGB(178, 70, 183),

'Color 313': RGB(108, 40, 201),

'Color 314': RGB(133, 40, 208),

'Color 315': RGB(142, 53, 203),

'Color 316': RGB(123, 93, 201),

'Color 317': RGB(128, 53, 237),

'Color 318': RGB(143, 49, 240),

'Color 319': RGB(138, 56, 255),

'Color 320': RGB(133, 103, 216),

'Color 321': RGB(164, 56, 237),

'Color 322': RGB(178, 63, 255),

'Color 323': RGB(193, 88, 231),

'Color 324': RGB(146, 115, 237),

'Color 325': RGB(160, 124, 255),

'Color 326': RGB(213, 98, 255),

'Color 327': RGB(227, 53, 237),

'Color 328': RGB(197, 143, 201),

'Color 329': RGB(202, 164, 202),

'Color 330': RGB(231, 171, 237),

'Color 331': RGB(225, 178, 255),

'Color 332': RGB(200, 176, 201),

'Color 333': RGB(250, 185, 255),

'Color 334': RGB(211, 187, 212),

'Color 335': RGB(218, 209, 237),

'Color 336': RGB(236, 222, 227),

'Color 337': RGB(228, 229, 251),

'Color 338': RGB(254, 239, 245),

'Color 339': RGB(255, 246, 239),

'Color 340': RGB(255, 253, 255),

'Color 341': RGB(250, 250, 250),

'Color 343': RGB(9, 9, 9),

'Color 344': RGB(20, 20, 20),

'Color 345': RGB(25, 25, 25),

'Color 346': RGB(43, 43, 43),

'Color 347': RGB(63, 63, 63),

'Color 348': RGB(75, 75, 75),

'Color 349': RGB(84, 84, 84),

'Color 350': RGB(93, 93, 93),

'Color 351': RGB(108, 108, 108),

'Color 352': RGB(124, 124, 124),

'Color 353': RGB(137, 137, 137),

'Color 354': RGB(149, 149, 149),

'Color 355': RGB(170, 170, 170),

'Color 356': RGB(188, 188, 188),

'Color 357': RGB(204, 204, 204),

'Color 358': RGB(218, 218, 218),

'Color 359': RGB(232, 232, 232),

'Color 342': RGB(0, 0, 255),

'Color 500': RGB(224, 97, 14),

'Color 501': RGB(0, 11, 66),

'Color 502': RGB(224, 231, 0),

'Color 503': RGB(230, 23, 65),

'Color 504': RGB(142, 231, 224),

'Color 505': RGB(230, 154, 0),

'Color 506': RGB(0, 231, 104),

'Color 507': RGB(38, 159, 230),

'Color 508': RGB(89, 0, 230),

'Color 509': RGB(133, 0, 230),

'Color 510': RGB(230, 71, 230),

'Color 512': RGB(230, 0, 191),

'Color 513': RGB(185, 17, 21),

'Color 514': RGB(48, 133, 35),

'Color 515': RGB(90, 166, 48),

'Color 516': RGB(205, 98, 13),

'Color 517': RGB(30, 112, 180),

'Color 518': RGB(23, 86, 160),

'Color 519': RGB(241, 185, 101),

'Color 520': RGB(125, 20, 17),

'Color 521': RGB(208, 250, 0),

'Color 522': RGB(117, 210, 0),

'Color 523': RGB(199, 13, 13),

'Color 524': RGB(251, 225, 0),

'Color 525': RGB(164, 129, 68),

'Color 526': RGB(210, 172, 55),

'Color 527': RGB(26, 67, 60),

'Color 528': RGB(82, 82, 84),

'Color 529': RGB(0, 152, 216),

'Color 530': RGB(210, 255, 21),

'Color 531': RGB(255, 100, 26),

'Color 532': RGB(169, 185, 197)

}

# Find the closest matching color for each target color

for color_name, color_rgb in target_colors.items():

closest_match = find_closest_color(color_rgb, reference_colors)

print(f"{color_name}: Closest Match - {closest_match}")