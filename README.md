# package-error-rhel

If gives any package error in rhel, even while doing sudo yum update:
Like in my case docker is giving error: mirrors failed

![image](https://github.com/AdityaKoranga/package-error-rhel/assets/95766110/72cb4da5-f476-4c09-a70c-c10ee4aa9728)

Then go to the directory

```bash
cd /etc/yum.repos.d/
```

Then check the repos list by doing `ls`
Like in my case:

![image](https://github.com/AdityaKoranga/package-error-rhel/assets/95766110/699dad11-3f5b-42fa-b99d-ee8405c9af44)

select the one which is giving error and then remove it:

```bash
sudo rm -f docker-ce.repo
```

Finally do:

```bash
sudo yum clean all
```

then do:
```bash
sudo yum update
```

