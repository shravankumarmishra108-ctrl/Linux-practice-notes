# File Permissions in Linux

## View permissions
ls -l

Example output:
-rwxr-xr-- 1 shravan devops 0 Apr 26 file.txt

Explanation:
- First part: permissions
- shravan → owner (user)
- devops → group

---

## Change permissions

chmod 755 file.txt

### What is 755?

755 is a numeric representation of permissions.

Breakdown:
- 7 = owner permissions
- 5 = group permissions
- 5 = others permissions

Now convert numbers:

7 = 4 + 2 + 1 = rwx (read, write, execute)  
5 = 4 + 0 + 1 = r-x (read, execute)

So:

chmod 755 file.txt means:
- Owner → read, write, execute (rwx)
- Group → read, execute (r-x)
- Others → read, execute (r-x)

---

## Change ownership

chown shravan:devops file.txt

Explanation:
- shravan → new owner
- devops → new group

---

## Example workflow

# Create file
touch file.txt

# Change owner and group
chown shravan:devops file.txt

# Set permissions
chmod 755 file.txt

# Why useing 755 ?
Number 755 Meaning     
4	- read (r)
2	- write (w)
1	- execute (x)

# Check result
ls -l file.txt
