# A New Software Serial Library for Arduino

Forked from: https://github.com/sirleech/NewSoftSerial
which was originally forked from: http://arduiniana.org/libraries/newsoftserial/
but no longer exists in November 2025.

This fork has minor changes to get the library operational in up-to-date Arduino IDE versions.

NewSoftSerial is the latest of three Arduino libraries providing “soft” serial port support. It’s the direct descendant of ladyada’s AFSoftSerial, which introduced interrupt-driven receives – a dramatic improvement over the polling required by the native SoftwareSerial.

Without interrupts, your program’s design is considerably restricted, as it must continually poll the serial port at very short, regular intervals. This makes it nearly impossible, for example, to use SoftwareSerial to receive GPS data and parse it into a usable form. Your program is too busy trying to keep up with NMEA characters as they arrive to actually spend time assembling them into something meaningful. This is where AFSoftSerial’s (and NewSoftSerial’s) interrupt architecture is a godsend. Using interrupt-driven RX, your program fills its buffer behind the scenes while processing previously received data.
