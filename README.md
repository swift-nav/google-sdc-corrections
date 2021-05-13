# GNSS corrections data for the Google Smartphone Decimeter Challenge (SDC)

This repo contains the GNSS corrections data for [Google's 2021 Smartphone Decimeter Challenge (SDC)](https://www.swiftnav.com/google-smartphone-decimeter-challenge). The data in this repo is provided by Swift Navigation as is and without support.

The repo contains _SSR_ and _OSR_ corrections data. OSR corrections data is provided as Swift's protocol messages in binary format (SBP) and human readable JSON format. Where possible, the data is also provided in RTCM3 MSM5. The SSR data is provided as Swift's protocol messages in binary format (SBP) and human readable JSON format.

In the _spec_ folder there is a PDF document with a description of all messages. There are also YAML files with the message definition for those who want to automate the loading or conversion of the data. You can also use the client libraries from Swift's open-source [libsbp](https://github.com/swift-nav/libsbp) to read the binary data in Swift Navigation Binary Protocol (SBP) format directly. The client libraries are available in a variety of languages (Python, C, Java, Rust, ...).

Note that not all drives of the Google Smartphone Decimeter Challenge have both SSR and OSR corrections. An overview is provided below.


## Folder structure
* _osr_: SBP, JSON, RTCM3 MSM5 and RINEX v3.03 files containing the OSR data.
* _ssr_: SBP and JSON files containing the SSR messages.
* _spec_: description of all messages in PDF and YAML format.


## Corrections

### OSR
The OSR data was unpacked from Swift binary protocol to a readable JSON file. Where possible, the OSR corrections are also provided in RTCM3 MSM5 format. Please refer to the RTCM3 standard on how to decode these messages. Alternatively you can use one of the many tools available online to convert these files. For example the open-source software RTKLIB can convert the data to RINEX. RINEX v3.03 files are also provided.

### SSR
The SSR data was unpacked from Swift binary protocol to a readable JSON file. The SSR corrections include orbits, clock and phase biases as well as precise atmospheric corrections covering a large part of California. Some notes:
* the 2020 files use a message format that is different from the 2021 files. The description of the messages is provided in the documentation in the _spec_ folder.
* the SSR data for 2020 does not contain L5 code and phase biases for GPS, only for Galileo.


## Swift Navigation Binary Protocol (SBP)
All corrections data is also provided in SBP format. SBP is a fast, simple, and minimal binary protocol for communicating with Swift devices. You can integrate the client libraries from [libsbp](https://github.com/swift-nav/libsbp) with your existing software to read the SBP data directly. The client libraries are available in a variety of languages (Python, C, Java, Rust, ...). The latest version of libsbp can be found here: [github.com/swift-nav/libsbp/releases/tag/v3.4.7](https://github.com/swift-nav/libsbp/releases/tag/v3.4.7).


## JSON format
The JSON files have been zip compressed to preserve space. They need to be extracted before use. There are many JSON loaders and parsers available online for most popular programming languages (Python, C, C++, ...). The format of the messages in the JSON files is described in the _spec_ folder.  The PDF file gives a complete description of each message. In the JSON files the messages can be identified by the `msg_type` field, which contains the decimal message type number. For example, message type number `138` for message `MSG_EPHEMERIS_GPS`. Note that the `payload` field of the message can be safely discarded. This simply contains the packed version of the message content.

If you are using Python, you can use the [libsbp](https://github.com/swift-nav/libsbp) library to load the message from the JSON files directly. The latest version of libsbp can be found here: [github.com/swift-nav/libsbp/releases/tag/v3.4.7](https://github.com/swift-nav/libsbp/releases/tag/v3.4.7).


## Drive overview
| Start | End | SSR | OSR |
| --- | --- | --- | --- |
| 5/14/2020 22:00:00 | 5/14/2020 23:00:00 | N | Y |
| 5/15/2020 00:00:00 | 5/15/2020 01:00:00 | N | Y |
| 5/15/2020 00:00:00 | 5/15/2020 02:00:00 | N | Y |
| 5/15/2020 20:00:00 | 5/15/2020 22:00:00 | N | Y |
| 5/15/2020 23:00:00 | 5/16/2020 01:00:00 | N | Y |
| 5/21/2020 18:00:00 | 5/21/2020 19:00:00 | N | Y |
| 5/21/2020 21:00:00 | 5/21/2020 22:00:00 | N | Y |
| 5/28/2020 19:00:00 | 5/28/2020 20:00:00 | N | Y |
| 5/28/2020 21:00:00 | 5/28/2020 22:00:00 | N | Y |
| 5/28/2020 21:00:00 | 5/28/2020 23:00:00 | N | Y |
| 5/29/2020 22:00:00 | 5/30/2020 00:00:00 | N | Y |
| 5/29/2020 23:00:00 | 5/30/2020 01:00:00 | N | Y |
| 6/04/2020 20:00:00 | 6/04/2020 22:00:00 | Partial (no GPS L5 code and phase biases) | Y |
| 6/04/2020 23:00:00 | 6/05/2020 00:00:00 | Partial (no GPS L5 code and phase biases) | Y |
| 6/05/2020 17:00:00 | 6/05/2020 18:00:00 | N | Y |
| 6/05/2020 17:00:00 | 6/05/2020 19:00:00 | N | Y |
| 6/05/2020 20:00:00 | 6/05/2020 21:00:00 | N | Y |
| 6/10/2020 17:00:00 | 6/10/2020 19:00:00 | Partial (no GPS L5 code and phase biases) | Y |
| 6/10/2020 20:00:00 | 6/10/2020 21:00:00 | Partial (no GPS L5 code and phase biases) | N |
| 6/11/2020 18:00:00 | 6/11/2020 19:00:00 | N | N |
| 7/08/2020 22:00:00 | 7/08/2020 23:00:00 | Partial (no GPS L5 code and phase biases) | Y |
| 7/08/2020 22:00:00 | 7/09/2020 00:00:00 | Partial (no GPS L5 code and phase biases) | Y |
| 7/08/2020 23:00:00 | 7/09/2020 01:00:00 | Partial (no GPS L5 code and phase biases) | Y |
| 7/17/2020 22:00:00 | 7/18/2020 00:00:00 | Partial (no GPS L5 code and phase biases) | Y |
| 7/17/2020 23:00:00 | 7/18/2020 00:00:00 | Partial (no GPS L5 code and phase biases) | Y |
| 8/03/2020 21:00:00 | 8/03/2020 23:00:00 | Partial (no GPS L5 code and phase biases) | N |
| 8/04/2020 00:00:00 | 8/04/2020 01:00:00 | Partial (no GPS L5 code and phase biases) | N |
| 8/06/2020 22:00:00 | 8/07/2020 00:00:00 | Partial (no GPS L5 code and phase biases) | N |
| 8/13/2020 21:00:00 | 8/13/2020 23:00:00 | Partial (no GPS L5 code and phase biases) | Y |
| 9/04/2020 17:00:00 | 9/04/2020 18:00:00 | Partial (no GPS L5 code and phase biases) | Y |
| 9/04/2020 17:00:00 | 9/04/2020 19:00:00 | Partial (no GPS L5 code and phase biases) | N |
| 1/04/2021 22:00:00 | 1/05/2021 00:00:00 | Y | Y |
| 1/05/2021 21:00:00 | 1/05/2021 22:00:00 | Y | Y |
| 1/05/2021 21:00:00 | 1/05/2021 23:00:00 | Y | Y |
| 3/10/2021 23:00:00 | 3/11/2021 00:00:00 | Y | Y |
| 3/16/2021 18:00:00 | 3/16/2021 20:00:00 | Y | Y |
| 3/16/2021 19:00:00 | 3/16/2021 20:00:00 | Y | Y |
| 3/16/2021 23:00:00 | 3/17/2021 00:00:00 | Y | Y |
| 3/25/2021 22:00:00 | 3/26/2021 00:00:00 | Y | Y |
| 4/02/2021 20:00:00 | 4/02/2021 22:00:00 | Y | Y |
| 4/08/2021 21:00:00 | 4/08/2021 22:00:00 | Y | Y |
| 4/15/2021 21:00:00 | 4/15/2021 23:00:00 | Y | Y |
| 4/21/2021 16:00:00 | 4/21/2021 19:00:00 | Y | Y |
| 4/22/2021 21:00:00 | 4/22/2021 22:00:00 | Y | Y |
| 4/22/2021 22:00:00 | 4/22/2021 23:00:00 | Y | Y |
| 4/26/2021 22:00:00 | 4/27/2021 00:00:00 | Y | Y |
| 4/26/2021 23:00:00 | 4/27/2021 01:00:00 | Y | Y |
| 4/28/2021 19:00:00 | 4/28/2021 21:00:00 | Y | Y |
| 4/28/2021 22:00:00 | 4/28/2021 23:00:00 | Y | Y |
| 4/28/2021 23:00:00 | 4/29/2021 00:00:00 | Y | Y |
| 4/29/2021 18:00:00 | 4/29/2021 20:00:00 | Y | Y |
| 4/29/2021 19:00:00 | 4/29/2021 21:00:00 | Y | Y |
| 4/29/2021 22:00:00 | 4/29/2021 23:00:00 | Y | Y |
| 4/29/2021 22:00:00 | 4/30/2021 00:00:00 | Y | Y |

Note that some overlapping or successive time intervals may be combined into a single file. Please check the timestamp of the files.


&nbsp;
&nbsp;


![Swift Navigation](https://avatars.githubusercontent.com/u/1069835?s=200&v=4)

201 Mission, Suite 2400\
San Francisco, CA 94105

Website: [swiftnav.com](https://www.swiftnav.com/)\
Twitter: [twitter.com/swiftnav](https://twitter.com/swiftnav)\
LinkedIn: [www.linkedin.com/company/swift-navigation](https://www.linkedin.com/company/swift-navigation)\
GitHub: [github.com/swift-nav](https://github.com/swift-nav)
