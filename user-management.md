# User Management in Linux

## Create User
useradd testuser

## Set Password
passwd testuser

## Delete User
userdel testuser

## Create Group
groupadd devops

## Add user to group
usermod -aG devops testuser

## Check user id
id testuser

## Switch user
su - testuser
