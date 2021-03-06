---
title: RemoteWipe DDF file
description: RemoteWipe DDF file
ms.assetid: 10ec4fb7-f911-4d0c-9a8f-e96bf5faea0c
ms.author: maricia
ms.topic: article
ms.prod: w10
ms.technology: windows
author: nickbrower
ms.date: 12/05/2017
---

# RemoteWipe DDF file


This topic shows the OMA DM device description framework (DDF) for the **RemoteWipe** configuration service provider. DDF files are used only with OMA DM provisioning XML.

Looking for the DDF XML files? See [CSP DDF files download](configuration-service-provider-reference.md#csp-ddf-files-download).

The XML below is the DDF for Windows 10, version 1709.

``` syntax
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE MgmtTree PUBLIC " -//OMA//DTD-DM-DDF 1.2//EN"
    "http://www.openmobilealliance.org/tech/DTD/DM_DDF-V1_2.dtd"
    [<?oma-dm-ddf-ver supported-versions="1.2"?>]>
<MgmtTree xmlns:MSFT="http://schemas.microsoft.com/MobileDevice/DM">
    <VerDTD>1.2</VerDTD>
    <Node>
        <NodeName>RemoteWipe</NodeName>
        <Path>./Vendor/MSFT</Path>
        <DFProperties>
            <AccessType>
                <Get />
            </AccessType>
            <DFFormat>
                <node />
            </DFFormat>
            <Occurrence>
                <One />
            </Occurrence>
            <Scope>
                <Permanent />
            </Scope>
            <DFType>
                <DDFName></DDFName>
            </DFType>
            <Description>The root node for remote wipe function.</Description>
        </DFProperties>
        <Node>
            <NodeName>doWipe</NodeName>
            <DFProperties>
                <AccessType>
                    <Exec />
                </AccessType>
                <DFFormat>
                    <chr />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
                <Description>Exec on this node will perform a remote wipe on the device. The return status code shows whether the device accepted the Exec command.</Description>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>doWipePersistProvisionedData</NodeName>
            <DFProperties>
                <AccessType>
                    <Exec />
                </AccessType>
                <DFFormat>
                    <chr />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
                <Description>Exec on this node will back up provisioning data to a persistent location and perform a remote wipe on the device. The information that was backed up will be restored and applied to the device when it resumes. The return status code shows whether the device accepted the Exec command.</Description>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>doWipeProtected</NodeName>
            <DFProperties>
                <AccessType>
                    <Exec />
                </AccessType>
                <DFFormat>
                    <chr />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
                <Description>Exec on this node will perform a remote wipe on the device and fully clean the internal drive. In some device configurations, this command may leave the device unable to boot. The return status code shows whether the device accepted the Exec command.</Description>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>doWipePersistUserData</NodeName>
            <DFProperties>
              <AccessType>
                  <Exec />
              </AccessType>
              <DFFormat>
                  <chr />
              </DFFormat>
              <Occurrence>
                  <One />
              </Occurrence>
              <Scope>
                  <Permanent />
              </Scope>
              <DFType>
                  <MIME>text/plain</MIME>
              </DFType>
              <Description>Exec on this node will perform a remote reset on the device and persist user accounts and data. The return status code shows whether the device accepted the Exec command.</Description>
            </DFProperties>
        </Node>
    </Node>
</MgmtTree>
```

## Related topics


[RemoteWipe configuration service provider](remotewipe-csp.md)

 

 






