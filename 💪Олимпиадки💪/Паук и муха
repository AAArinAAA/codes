for x in range(1,21):
    if x<10:
        a=open('input_s1_0'+str(x)+'.txt','r')
    else:
        a=open('input_s1_'+str(x)+'.txt','r')

    R=[int(x) for x in a.readline().split()]
    P=[int(x) for x in a.readline().split()]
    M=[int(x) for x in a.readline().split()]
    def F(k,c,d):
        if (c[0]==d[0]==k[0] or c[0]==d[0]==0):
            return ((c[1]-d[1])**2 + (c[2]-d[2])**2)**0.5
        elif (c[1]==d[1]==k[1] or c[1]==d[1]==0):
            return ((c[0]-d[0])**2 + (c[2]-d[2])**2)**0.5
        elif (c[2]==d[2]==k[2] or c[2]==d[2]==0):
            return ((c[1]-d[1])**2 + (c[0]-d[0])**2)**0.5
        elif ((c[0]==k[0] or c[0]==0) and d[0]!=c[0] and (d[1]==k[1] or d[1]==0) and c[1]!=d[1]):
            p=(abs(c[0]-d[0])+abs(c[1]-d[1]))
            return ((p)**2 + (c[2]-d[2])**2)**0.5
        elif ((c[2]==k[2] or c[2]==0) and d[2]!=c[2] and (d[1]==k[1] or d[1]==0) and c[1]!=d[1]):
            p=(abs(c[2]-d[2])+abs(c[1]-d[1]))
            return ((p)**2 + (c[0]-d[0])**2)**0.5
        elif ((c[1]==k[1] or c[1]==0) and d[1]!=c[1] and (d[2]==k[2] or d[2]==0) and c[2]!=d[2]):
            p=(abs(c[1]-d[1])+abs(c[2]-d[2]))
            return ((p)**2 + (c[0]-d[0])**2)**0.5
        elif ((c[0]==k[0] or c[0]==0) and d[0]!=c[0] and (d[2]==k[2] or d[2]==0) and c[2]!=d[2]):
            p=(abs(c[0]-d[0])+abs(c[2]-d[2]))
            return ((p)**2 + (c[1]-d[1])**2)**0.5
        elif ((c[1]==k[1] or c[1]==0) and d[1]!=c[1] and (d[0]==k[0] or d[0]==0) and c[0]!=d[0]):
            p=(abs(c[1]-d[1])+abs(c[0]-d[0]))
            return ((p)**2 + (c[2]-d[2])**2)**0.5
        elif ((c[2]==k[2] or c[2]==0) and d[2]!=c[2] and (d[0]==k[0] or d[0]==0) and c[0]!=d[0]):
            p=(abs(c[2]-d[2])+abs(c[0]-d[0]))
            return ((p)**2 + (c[1]-d[1])**2)**0.5
        elif ((c[0]==k[0]   and d[0]==0) or (c[0]==0 and d[0]==k[0])):
            if (k[2]-c[2]+k[2]-d[2] <c[2]+d[2]):
                p=(k[2]-c[2]+k[2]-d[2] +k[0])
            else:
                p=(c[2]+d[2]+k[0])
            if (k[1]-c[1]+k[1]-d[1] <c[1]+d[1]):
                q=(k[1]-c[1]+k[1]-d[1] +k[0])
            else:
                q=(c[1]+k[1]+k[0])
            if p<=q:
                return ((p)**2 + (c[1]-d[1])**2)**0.5
            else:
                return ((q)**2 + (c[2]-d[2])**2)**0.5
        elif ((c[1]==k[1]   and d[1]==0) or (c[1]==0 and d[1]==k[1])):
            if (k[2]-c[2]+k[2]-d[2] <c[2]+d[2]):
                p=(k[2]-c[2]+k[2]-d[2] +k[1])
            else:
                p=(c[2]+d[2]+k[1])
            if (k[0]-c[0]+k[0]-d[0] <c[0]+d[0]):
                q=(k[0]-c[0]+k[0]-d[0] +k[1])
            else:
                q=(c[0]+k[0]+k[1])
            if p<=q:
                return ((p)**2 + (c[0]-d[0])**2)**0.5
            else:
                return ((q)**2 + (c[2]-d[2])**2)**0.5
        elif ((c[2]==k[2]   and d[2]==0) or (c[2]==0 and d[2]==k[2])):
            if (k[1]-c[1]+k[1]-d[1] <c[1]+d[1]):
                p=(k[1]-c[1]+k[1]-d[1] +k[2])
            else:
                p=(c[1]+k[1]+k[2])
            if (k[0]-c[0]+k[0]-d[0] <c[0]+d[0]):
                q=(k[0]-c[0]+k[0]-d[0] +k[2])
            else:
                q=(c[0]+d[0]+k[2])
            if p<=q:
                return ((p)**2 + (c[0]-d[0])**2)**0.5
            else:
                return ((q)**2 + (c[1]-d[1])**2)**0.5
    print(round(F(R,P,M),3))
