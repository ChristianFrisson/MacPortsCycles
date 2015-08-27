# MacPortsCycles

Portfiles for [MacPorts](https://www.macports.org) (software manager for Mac OSX) related to the [numediart](https://www.numediart.org) Institute and [MediaCycle](https://www.mediacycle.org) framework from [UMONS](https://www.umons.ac.be), for cycles of [bug reports and updates](https://trac.macports.org).

## Available ports

Some ports may have been merged in the main MacPorts distribution after having been committed here.

* (2014/04/04) audio/phonon v4.7.1: major update, for use with qt4
* (2014/03/30) devel/vxl v1.17.0+ from [vxl/vxl](https://github.com/vxl/vxl): required openjpeg and ffmpeg fixes
* (2013/08/25) graphics/libfreenect v0.2.0 from [OpenKinect/libfreenect](https://github.com/OpenKinect/libfreenect): just needed an update
* (2013/08/30) graphics/openni-avin2sensorkinect v5.1.2.1 from [avin2/SensorKinect](https://github.com/avin2/SensorKinect): updated to the most recent unstable version
* (2013/08/25) graphics/openni2 v2.2.0.30 from [ChristianFrisson/OpenNI2](https://github.com/ChristianFrisson/OpenNI2): required fixes for clang to compile under OSX 10.8 and scripts for a clean installation
* (2013/08/25) graphics/openni2-freenectdriver v2.0.0.29 from [piedar/OpenNI2-FreenectDriver](https://github.com/piedar/OpenNI2-FreenectDriver): required waf fixes to compile
* (2013/08/25) graphics/tiff v4.0.3 from [tiff](http://www.remotesensing.org/libtiff/): required cleaned headerpad_max_install_names ldflags otherwise fixing up app bundles fails against this dependency
* (2014/04/26) multimedia/JamomaCore from [jamoma/JamomaCore](https://github.com/ChristianFrisson/JamomaCore): experimental, for now without its Jamoma extensions
* (2014/04/26) multimedia/JamomaScore from [OSSIA/Score](https://github.com/ChristianFrisson/Score): experimental, for now without its Jamoma extensions
* (2014/02/10) multimedia/JamomaScore from [OSSIA/i-score](https://github.com/ChristianFrisson/i-score): experimental (to be updated)
* (2014/04/04) multimedia/phonon-backend-vlc v.0.7.1: new port, for use with qt4
* (2014/04/04) multimedia/VLC v.2.1.4: patch update plus modification to use macosx audio rather than pulseaudio

## Installation

Once MacPorts is installed, open a terminal in a directory where you want to download MacPortsCycles:

### Install git if you don't have it
```bash
sudo port selfupdate; 
sudo port install git-core; 
```

### Clone this repository and add its path to the MacPorts sources before other entries
```bash
git clone https://github.com/ChristianFrisson/MacPortsCycles.git; 
sudo sh -c 'port=`which port`;echo "file://`pwd`/MacPortsCycles\n$(cat ${port%bin/port}etc/macports/sources.conf)" > ${port%bin/port}etc/macports/sources.conf'; 
sudo port selfupdate
```

### Install ports
Then to install a given port listed above, for instance openni-avin2sensorkinect:
```bash
sudo port install openni-avin2sensorkinect
```