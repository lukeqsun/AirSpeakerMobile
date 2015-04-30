# AirSpeakerMobile
Turn Android phone into an AirPlay speaker for Macs.

This project is based on the work done by fenggit's project: AirPlayService.

References & Acknowledgements
-----------------------------

* AirPlayService written by fenggit (fenggit@163.com)
  https://github.com/fenggit/AirPlayService
  Fix a few bugs in DroidAirPlay.

* DroidAirPlay written by Rafael Almeida (rafael@iswe.co.nz)
  https://github.com/pentateu/DroidAirPlay
  The idea is to develop a AirPlay Receiver that runs on Android tablet and is part of a wider range of apps for in-car-systems.
  The idea is that the tablet is used as a car dashboard to control all car functions and the ability to stream audio, video e fotos from iOS devices is achieved throught this project.

* AirReceiver written by Florian G. Pflug <fgp [at] phlo.org>
  https://github.com/fgp/AirReceiver
  AirReceiver is an AirPort Express emulator, i.e. it allows streaming audio
  from iTunes and iOS devices to a computer running AirReceiver. It does so by
  implementing a RAOP/AirTunes2 server.

* ShairPort written by James Laird
  http://mafipulation.org/blagoblig/reversing, https://github.com/albertz/shairport
  AirReceiver wouldn't haven been possible to write without the work James Laird
  put into reverse-engineering the protocol and encryption.

* ALAC Decoder written David Hammerton and ported to Java by soiaf
  https://github.com/soiaf/Java-Apple-Lossless-decoder

* Java mDNS - ZeroConf (Bonjour(TM) in Apple terms) implementation for Java
  http://jmdns.sourceforge.net/
  Provides AirReceiver with the ability to announce it's service on the
  local network without having to resort to platform-specific code
  like Apple's Bonjour Java bindings (which aren't available on Linux
  anyway)

* Netty by the JBoss Community
  http://www.jboss.org/netty
  Netty makes writing network server in Java pure joy. Writing the RTSP server
  component was a breeze with netty's built-in support for HTTP and RTSP.

* BouncyCastle Java Cryptography Provider
  http://www.bouncycastle.org/
  BouncyCastle included all of the RSA and AES variants used by RAOP/AirTunes2

* Base64 Encoder/Decoder by iharder
  http://iharder.sourceforge.net/current/java/base64/
  iharder's Base64 decode saved me a few hours it'd otherwise probably have spent
  writing and debugging an base64 encoder/decoder myself.

* Maven
  http://maven.apache.org/
  Hassle-free dependency management. And a helluva lot of plugins, usually
  just a few google searches away.

* OneJar packaging plugin for maven
  http://one-jar.sourceforge.net/
  Provides the double-clickable .jar files, and all that's required was adding
  a few lines to AirReceiver's .pom

* Mac OS X application packaging plugin for maven
  http://mojo.codehaus.org/osxappbundle-maven-plugin/
  Add a few lines to your .pom and, there, you've built a Mac OS X application
  bundle from your Java application. Cool!
