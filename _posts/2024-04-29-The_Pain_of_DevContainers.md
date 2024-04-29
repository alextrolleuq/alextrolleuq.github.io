# The Pain of Dev Containers

{% include alert.html text="Not recommended if you are easily frustrated" %}

This last week I have struggeled alot with dev containers. I used quite a few hours getting it to run on cpufrozen (from my assignment), 
and there was always something that went wrong. I asked chatgpt for help, but even one of the biggest LLM couldn't help to much with this.
Here I will relive some of my pain, hope you enjoy!

## Getting CPUFROZEN up and running
Our professor created the whole setup for us to use dev containers, which after struggeling so much myself I find impressiv. 

I followed his blog [Brian Lovell's Awesome fastai Blog](https://lovellbrian.github.io/2023/10/02/BYODImage.html). It helped with donwloading wsl, docker desktop and updating my nvidia drivers.
All this went pretty smoothly. My first headache was when I tried to connect to wsl in vscode, as it wouuld be an option for me. I solved this by simply installing wsl in vscode.

I guess something went wrong here, because when I tried to open up a dev container, I got an error that something unexpected happened. A few hours of debugging, my professor suggested
I uninstall and reinstall vscode, and it solved the problem. 

My next headache was that while my dev container was building, my pc said it didn't have enough storage space to continue. I found this a bit weird as I though I had stored it
somewhere with a lot of space. Sadly, it wouldn't go on and build my container, so I had to free some storage (some gopro videos from my awesome summer vacation) and restart everyhting.

Now it worked fine, and the sun was shining (metaforically as it was already dark because this took way to long).

## GPU problems

But when I though everything was good and nice, I encountered another problem when I tried to open up a brand new container for my GPU. It wsa a mounting problem, as I guess it though I was mounting a mount even though I don't agree with my machine.
I guess alot of people encountered this problem as I found alot of gold on ED. I solved it by installing jupyter in wsl, as I only had it on windows. My guess is that 
a part of the setup from my professor didn't get executed, so I had to manually install it. Anyhow, the container is now built, and everything is alot quicker.

My last real problem was that I couldnt get nvtop up and running, so I could overview my gpu performance. Firstly, nvtop wasn't installed/updated on my driver, so that was an annoying part of the problem as I dond't realize straight away.
Then it wouldn't run, and said it didn't have enough memory for it, which was b*llsh*t as I just had created a notebook which made sure it had 8GB of swap and not only 2.
I then found out it had saved the notebook as a .txt file, and not a configuration file, so well yeah.. my b ig

Now I can see my performance of my gpu (rtx2060), and I am happy that everything works. Exept the fact that when I increased the batch size it went slower and my optimum batch size was 64.
But anyhoops, it works and runs fine :)
