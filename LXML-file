from lxml import etree

def myfood_menu(xmlfile):
    with open(xmlfile) as food_menu:
        xml = food_menu.read()
    root = etree.fromstring(xml)
    food_dic = {}
    foods = []
    for food in root.getchildren():
        for elem in food.getchildren():
            if elem.text:
                text = elem.text
            else:
                text = " "
            print(elem.tag + ": " + text)
            food_dic[elem.tag] = text
        if food.tag == "food":
            foods.append(food_dic)
            food_dic = {}
    return food
    
myfood = myfood_menu('F:\\hhh\\food.xml')    
