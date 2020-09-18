# algo
**Knutt-Moris-Pratt**
**Prefix-function**

def create_suffix(str_):
    pis = [0]*len(str_)
    for ind, elem in enumerate(str_):
        if (ind > 0):
            j = pis[ind - 1]
            while((j > 0) & (str_[j] != str_[ind])):
                j = pis[j - 1]
            if (str_[j] == str_[ind]):
                j += 1
            pis[ind] = j
        
return pis
