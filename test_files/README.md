## This part is included in the installation guide
Use following command to download these files.

```
wget https://raw.githubusercontent.com/qkx515/real-time-linux-kernel/master/test_files/cyclictest_plot.sh
wget https://raw.githubusercontent.com/qkx515/real-time-linux-kernel/master/test_files/cyclictest_run.sh
```

or

you can just open these links and save these files directly by ctrl + s

---

If you want to use these files. There are some commands you need to run first.

```
sudo -s
apt-get install rt-tests gnuplot
```

After download these files, I would suggest you put them in your home folder, which will make it easier to run. We need to use following command to make these files executable. 

**<~ or your download folder> is a placeholder here.**

```
chmod +x <~ or your download folder>/cyclictest_run.sh
chmod +x <~ or your download folder>/cyclictest_plot.sh
```

To run these files, you need to do the following commands.

```
sudo –s #we need root permission
./cyclictest_run.sh 100000 > result
```

Wait for a few minutes. This command creates a file named “result” containing the testing result. Then,

```
./cyclictest_plot.sh result
```

This command visualizes your data and put it in result.png in your current directory. Go see it!

---
There are some results in ../test_results folder for you to see.
