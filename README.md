# top50_songs
Taking out some beautiful insights and analyzing and visualizing different genre of songs having movie rating sysytem


import numpy as np
import pandas as pd
top50=pd.read_csv('top50spotify.csv')
Assignment: 2
Problem:1
import numpy as np
!get https://www.dropbox.com/s/2hg67jin2n852mz/top50spotify.csv
import pandas as pd
top50=pd.read_csv('top50spotify.csv')
top50.head()

top50.drop(columns="SerialNo.",inplace=True)
top50.head()

top50.to_csv("top50.csv")
top50.iloc[:10]

Top_10=top50.head(10)
Top_10

Top_10[["Energy","Length."]].mean()

top50.groupby('Genre')['Length.'].sum().sort_values
top50.groupby('Genre')['Length.'].sum().sort_values(ascending=False)
result=top50.groupby(['Genre','Artist.Name'])['Track.Name'].count()
result
result.max()
result[result==result.max()]
top50[top50['Artist.Name']=='Ed Sheeran']
#problem2
import numpy as np
import pandas as pd


dict_of_values = {'English':{'Sam':60,'Jackson':74,'Ahree':85},
 'History':{'Gloria':83,'Sam':65,'Isla':78,'Aron':72,'Gray':61},
'Geography':{'Jackson':92,'Gloria':95,'Isla':82,'Aron':66}}
series=pn.Series(dict_of_values)
print(series)
