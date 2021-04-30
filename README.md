# GNSS correction data for the Google Smartphone Decimeter Challenge (SDC)

This repo contains the GNSS correction data for Google's 2021 Smartphone Decimeter Challenge (SDC). The data in this repo is provided by Swift Navigation as is and without support.

The repo contains SSR and OSR correction data. OSR correction data is provided as Swift's protocol messages in JSON format and, where possible, in RTCM3 MSM5. The SSR data is provided as Swift's protocol messages in JSON format. The description of the JSON format is provided in the _spec_ folder. In the _spec_ folder there is a PDF document with a description of all messages. There are also YAML files with the message definition for those who want to automate the loading or conversion of the data.

Note that not all drives of the Google Smartphone Decimeter Challenge have both SSR and OSR. An overview is provided below.


## Folder structure
* _osr_: JSON and RTCM3 MSM5 files containing the OSR data.
* _ssr_: JSON files containing the SSR messages.
* _spec_: description of all messages in PDF and YAML format.


## Drive overview
* 5/14/2020 22:00:00 - 5/14/2020 23:00:00: SSR: N, OSR: Y
* 5/15/2020 0:00:00 - 5/15/2020 1:00:00: SSR: N, OSR: Y
* 5/15/2020 0:00:00 - 5/15/2020 2:00:00: SSR: N, OSR: Y
* 5/15/2020 20:00:00 - 5/15/2020 22:00:00: SSR: N, OSR: Y
* 5/15/2020 23:00:00 - 5/16/2020 1:00:00: SSR: N, OSR: Y
* 5/21/2020 18:00:00 - 5/21/2020 19:00:00: SSR: N, OSR: Y
* 5/21/2020 21:00:00 - 5/21/2020 22:00:00: SSR: N, OSR: Y
* 5/28/2020 19:00:00 - 5/28/2020 20:00:00: SSR: N, OSR: Y
* 5/28/2020 21:00:00 - 5/28/2020 22:00:00: SSR: N, OSR: Y
* 5/28/2020 21:00:00 - 5/28/2020 23:00:00: SSR: N, OSR: Y
* 5/29/2020 22:00:00 - 5/30/2020 0:00:00: SSR: N, OSR: Y
* 5/29/2020 23:00:00 - 5/30/2020 1:00:00: SSR: N, OSR: Y
* 6/4/2020 20:00:00 - 6/4/2020 22:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: Y
* 6/4/2020 23:00:00 - 6/5/2020 0:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: Y
* 6/5/2020 17:00:00 - 6/5/2020 18:00:00: SSR: N, OSR: Y
* 6/5/2020 17:00:00 - 6/5/2020 19:00:00: SSR: N, OSR: Y
* 6/5/2020 20:00:00 - 6/5/2020 21:00:00: SSR: N, OSR: Y
* 6/10/2020 17:00:00 - 6/10/2020 19:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: Y
* 6/10/2020 20:00:00 - 6/10/2020 21:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: N
* 6/11/2020 18:00:00 - 6/11/2020 19:00:00: SSR: N, OSR: N
* 7/8/2020 22:00:00 - 7/8/2020 23:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: Y
* 7/8/2020 22:00:00 - 7/9/2020 0:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: Y
* 7/8/2020 23:00:00 - 7/9/2020 1:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: Y
* 7/17/2020 22:00:00 - 7/18/2020 0:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: Y
* 7/17/2020 23:00:00 - 7/18/2020 0:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: Y
* 8/3/2020 21:00:00 - 8/3/2020 23:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: N
* 8/4/2020 0:00:00 - 8/4/2020 1:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: N
* 8/6/2020 22:00:00 - 8/7/2020 0:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: N
* 8/13/2020 21:00:00 - 8/13/2020 23:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: Y
* 9/4/2020 17:00:00 - 9/4/2020 18:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: Y
* 9/4/2020 17:00:00 - 9/4/2020 19:00:00: SSR: Partial (no GPS L5 code and phase biases), OSR: N
* 1/4/2021 22:00:00 - 1/5/2021 0:00:00: SSR: Y, OSR: Y (RTCM3 coming soon)
* 1/5/2021 21:00:00 - 1/5/2021 22:00:00: SSR: Y, OSR: Y (RTCM3 coming soon)
* 1/5/2021 21:00:00 - 1/5/2021 23:00:00: SSR: Y, OSR: Y (RTCM3 coming soon)
* 3/10/2021 23:00:00 - 3/11/2021 0:00:00: SSR: Y, OSR: Y (RTCM3 coming soon)
* 3/16/2021 23:00:00 - 3/17/2021 0:00:00: SSR: Y, OSR: Y (RTCM3 coming soon)
* 4/2/2021 20:00:00 - 4/2/2021 22:00:00: SSR: Y, OSR: Y (RTCM3 coming soon)
* 4/8/2021 21:00:00 - 4/8/2021 22:00:00: SSR: Y, OSR: Y (RTCM3 coming soon)
* 4/15/2021 21:00:00 - 4/15/2021 23:00:00: SSR: Y, OSR: Y (RTCM3 coming soon)
* 4/21/2021 16:00:00 - 4/21/2021 19:00:00: SSR: Y, OSR: Y (RTCM3 coming soon)


## Corrections

### OSR
The OSR data was unpacked from Swift binary protocol to a readable JSON file. Where possible, the OSR corrections are also provided in RTCM3 MSM5 format. Please refer to the RTCM3 standard on how to decode these messages. Alternatively you can use one of the many tools available online to convert these files. For example the open source software RTKLIB can convert the data to RINEX. Note that RTCM3 files are not yet available for more recent files (from 2021).

### SSR
The SSR data was unpacked from Swift binary protocol to a readable JSON file. The SSR corrections include orbits, clock and phase biases as well as precise atmospheric corrections covering a large part of California. Some notes:
* the 2020 files use a different file format that is different from the 2021 files. The description of the messages is provided in the documentation in the _spec_ folder.
* the SSR data for 2020 does not contain L5 code and phase biases for GPS, only for Galileo.


## JSON format
The JSON files have been tar compressed to preserve space. They need to be extracted before use. There are many JSON loaders and parsers available online for most popular programming languages (Python, C, C++, ...). The format of the messages in the JSON files is described in the _spec_ folder.  The PDF file gives a complete description of each message. In the JSON files the messages can be identified by the `msg_type` field, which contains the decimal message type number. For example, message type number `138` for message `MSG_EPHEMERIS_GPS`. Note that the `payload` field of the message can be safely discarded. This simply contains the packed version of the message content.


&nbsp;
&nbsp;


![Swift Navigation](https://avatars.githubusercontent.com/u/1069835?s=200&v=4)

201 Mission, Suite 2400\
San Francisco, CA 94105

Website: [swiftnav.com](https://www.swiftnav.com/)\
Twitter: [twitter.com/swiftnav](https://twitter.com/swiftnav)\
LinkedIn: [www.linkedin.com/company/swift-navigation](https://www.linkedin.com/company/swift-navigation)\
GitHub: [github.com/swift-nav](https://github.com/swift-nav)
