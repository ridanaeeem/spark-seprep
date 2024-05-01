# Rida Naeem Assignment 8

I was unable to complete the assignment due to some issues that I faced with my Macbook, as detailed below.

## Challenges

#### 1: M1 Preqreuisites

Regarding the prerequisites for having an M1 Macbook, I had trouble editing my `.config/containers/containers.conf` file as described in the instructions. Whenever I made this edit, Podman would stop working and kept saying that it could not find any machines, even though I had already created one and used it for previous assignments. When I tried intializing a new one I was stuck in the setup screen for over 45 minutes, so I had to revert the changes I made to my `.config/containers/containers.conf` file and then go through the next few steps with Podman working before I was able to make the change to the file.

#### 2: Podman Versions

Regardless of whether or not I had the change in my `.config/containers/containers.conf` file, I was unable to run the following command for the Deploy Model Service step:

```podman run --rm -it \
        -p 8001:8001 \
        -v /local/path/to/self-hosted-llms/models/ggml-small.bin:/models/ggml-small.bin:Z,ro \
        -e HOST=0.0.0.0 \
        -e PORT=8001 \
        whisper:image
```

I tried getting this part working before class on 4/24 and then worked with the instructors during class, staying after for nearly 45 minutes, but ultimately I was unable to move past this point because of some issues with Podman versions. When checking the Podman version with `podman --version`, it stated that they server and client were on different versions, with one being on 4 and the other on 5. We tried uninstalling Podman, but this step itself took a long time because simply uninstalling Podman from my Mac was not enough to actually remove it from my system, we had to delete the associated files manually.

After reinstalling Podman, both from the website, trying the generic Mac version and the ARM version, and with the brew command, I was still unable to get them both to be on the same version.

After looking into it further with the instructors, we realized that it was likely because my Mac was not up-to-date. I am on version 11.6 but am unable to update due to limited storage. Although I spent some time deleting some applications and large files, I still was unable to update my Mac.

When my system had Podman it was only on two separate versions, and although I tried both on my own outside of class and with the instructors in class, I was unable to just get one with one version or to update one version to the other because of the limiting factor of my Macbook not being up-to-date.
