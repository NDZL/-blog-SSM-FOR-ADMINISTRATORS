Title: "Unlocking Efficiency: Driving Zebra Secure Storage Manager Adoption in Staging Operations with Android 13" 

 

In the fast-paced world of enterprise technology, staying ahead of the curve is essential. Zebra Technologies is leading the charge with its innovative approach to storage solutions, particularly through the adoption of Secure Storage Manager (SSM) in Staging Operations with the latest Android 13. In this guide, we'll delve into the key aspects of this technology and how it benefits developers, staging designers, and businesses alike. 


## Understanding Secure Storage Manager (SSM) 

Secure Storage Manager (SSM) is a powerful tool designed by Zebra Technologies to address and overcome storage-related concerns. In essence, SSM provides a secure channel for transmitting data between applications, ensuring confidentiality through features like optional pre-encryption and auto-decryption. This shared resource manages multiple connections and pieces of data, making it a versatile solution for both developers and staging designers. 

### Benefits for Developers 

Developers can leverage SSM to enhance their applications with features like: 

- Differentiation for data types (files and key/value pairs) 

- Optional pre-encryption support and auto-decryption for secure data transmission 

- Notifications for real-time updates on new data availability 

- Persistence across OS Enterprise Reset for saving data for future instances 

 
### Empowering Staging Designers 

Even non-developers can start using SSM in staging workflows, thanks to its user-friendly configuration. The guide provides step-by-step instructions on configuring various Zebra tools like Datawedge, Enterprise Browser, Device Diagnostic Tool, Application Manager, and Enterprise Keyboard to seamlessly integrate with SSM. 


## Configuring Zebra Tools for SSM Adoption 

 

The guide outlines the detailed process of configuring different Zebra tools for SSM adoption in Staging Operations: 

---

1. **Datawedge Configuration:** Setting up profiles for Datawedge to deploy files for applications using SSM. 

Main reference https://techdocs.zebra.com/datawedge/13-0/guide/programmers-guides/ssm/#deployviastagenow-1

In StageNow add a FileMgr block and select File Action «Deploy file for an application» 

In «Target Application File Definition» enter DW packagename and the path ```com.symbol.datawedge/config/datawedge.db```

change the db filename according to your case, e.g. “dwprofile_SpatialCompute.db”

In «Source Access Method» choose «File on a Remote Server» (This means either on your Staging machine or on the Internet)

![image](https://github.com/NDZL/-blog-SSM-FOR-ADMINISTRATORS/assets/11386676/7dc3d936-bd11-4512-85bd-7cf071fc60f2)

Then put it at work creating the staging 2D-barcode and validating the output

![image](https://github.com/NDZL/-blog-SSM-FOR-ADMINISTRATORS/assets/11386676/d4323d86-2020-4c8e-89b4-69a1ab99f3a3)

---

2. **Enterprise Browser Configuration:** Deploying files for Enterprise Browser applications using SSM. 

Main reference https://techdocs.zebra.com/enterprise-browser/3-6/guide/about/ 

In StageNow add a FileMgr block and select File Action «Deploy file for an application» 

In «Target Application File Definition» enter EB package name and the path ```com.zebra.mdna.enterprisebrowser/Config.xml```

In this case, the configuration file name must not be changed

In «Source Access Method» choose «File on a Remote Server»

![image](https://github.com/NDZL/-blog-SSM-FOR-ADMINISTRATORS/assets/11386676/78b50526-65b1-4fbb-962d-39f00a1bc39d)

Configured EB at work

![image](https://github.com/NDZL/-blog-SSM-FOR-ADMINISTRATORS/assets/11386676/104f71ba-113d-415f-a708-9e3fe2c87cd4)

--- 

3. **Device Diagnostic Tool Configuration:** Configuring the Device Diagnostic Tool for secure deployment using SSM. 

Main reference https://techdocs.zebra.com/ddt/2-9/guide/configuration/#securedeployment

Get it from here https://www.zebra.com/us/en/support-downloads/software/utilities/device-diagnostic-tool.html

In StageNow add a FileMgr block and select File Action «Deploy file for an application»

In «Target Application File Definition» enter DDT package name and the path ```com.zebra.mdna.selfdiagnostics/configuration.xml```

In this case, the configuration file name must not be changed

In «Source Access Method» choose «File on a Remote Server»

An example of configuration

![image](https://github.com/NDZL/-blog-SSM-FOR-ADMINISTRATORS/assets/11386676/5d7b9fbd-537c-43f5-95a8-89bf719c5906)

---

4. **App Installation using SSM:** Installing applications in a two-step profile setup, utilizing SSM for seamless deployment. 

Main reference https://techdocs.zebra.com/stagenow/5-10/ssmusage/#installappsusingssm 

1. - FILE MANAGER SET UP
In StageNow add a FileMgr block and select File Action «Deploy file for an application»

In «Target Application File Definition» enter the AppMgr package name and the path of the app to be stored in SSM
```com.zebra.devicemanager/non_persist_apk/ion-ang-cap-printer-v1.0.apk```

Change the apk name according to your case. Check doc for persisting the app

In «Source Access Method» choose «File on a Remote Server»

In the example the asset (APK) will be sourced from the Internet!  

![image](https://github.com/NDZL/-blog-SSM-FOR-ADMINISTRATORS/assets/11386676/0f346a8a-c512-4aff-977d-46a92c4f85f8)


2. - APP MANAGER SET UP
In StageNow add an AppMgr block and select Application Action «Install» 
In «File name and path» enter the same package name and the path you entered in the previous step
```com.zebra.devicemanager/non_persist_apk/ion-ang-cap-printer-v1.0.apk```

APPLY THE PROFILE
Downloading assets from the Internet (https://...) works fine on Android 13 BSPs – Not tested on Android 11.

Shoot the 2D barcode and see your APK downloaded and installed

![image](https://github.com/NDZL/-blog-SSM-FOR-ADMINISTRATORS/assets/11386676/8d9fb32a-f98b-4e03-90d1-6f7404c84311)


---

5. **Enterprise Keyboard Configuration:** Deploying files for Enterprise Keyboard applications using SSM, with a step-by-step guide. 

 

Each section provides main references, step-by-step instructions, and practical tips to ensure a smooth transition to SSM adoption in staging workflows. 

 

## Conclusion 

As the digital landscape continues to evolve, Zebra Technologies remains at the forefront, driving innovation in storage solutions with Android 13. Whether you're a developer seeking enhanced security features or a staging designer streamlining workflows, the adoption of Secure Storage Manager and associated tools promises increased efficiency and functionality. Embrace the future of enterprise technology with Zebra Technologies. 
