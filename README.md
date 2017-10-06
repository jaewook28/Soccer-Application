# Soccer-Applicationimport MySQLdb

###############################DATABASE########################################
db = MySQLdb.connect(host="localhost", 
                     user="root", 
                     passwd="WJDwodnr5771^^", 
                     db="TEST")
###############################################################################





#################################Adding Score##################################
player = 17
id = 0
num = 8
s = 0
###############################################################################
playername = ['name','Simon', 'Jae', 'Youssif', 'Axell','Malcolm','Armon','Arthur','Dian','Ber','Tom','Mert','Eric','Carmen','Andrew','Josh','William','Charle']
num





##############################MYSQL############################################
cur = db.cursor()
#Insert varialbe in a DATATABLE
for player in range(0,player):
    id = id+1
    name = playername[id]
    cur.execute("INSERT INTO playerlist VALUES(%s,%s,%s,%s)",(id, name, num, s))
    #cur.execute("INSERT INTO playerlist SET  %s, name = 'Axell', num = 3, goal = 1"), (id)


cur.execute("SELECT * FROM playerlist") #SELECT TABE#
###############################################################################



















for row in cur.fetchall() :
    print row[0], "", row[1], "", row[2] ,row[3]
    
    


