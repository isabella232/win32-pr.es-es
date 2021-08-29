---
title: Comprobación de la compatibilidad con la unidad
description: En el ejemplo siguiente se examinan las características del dispositivo de disco que son independientes de los medios insertados en el dispositivo.
ms.assetid: 2d7e5ff9-7f1b-4bc1-bbc8-5e7eab45cdb0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a584640cba7b67632924e40b4b8e816be7b4625c9a07a520e0d590e03264e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758813"
---
# <a name="checking-drive-support"></a>Comprobación de la compatibilidad con la unidad

En el ejemplo siguiente se examinan las características del dispositivo de disco que son independientes de los medios insertados en el dispositivo. En concreto, recupera listas de características admitidas, perfiles admitidos y páginas de modo admitido, así como la configuración y el perfil de características actuales.


```VB
' This script examines the burn device characteristics such as 
' product ID, product revision level, feature set, and profiles. 

' Copyright (C) Microsoft Corp. 2006

Option Explicit

' Constants
const IMAPI_FEATURE_PAGE_TYPE_DVD_DASH_WRITE = 47

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system

    ' Create a DiscMaster2 object to connect to CD/DVD drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(Index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' *** - Formatting to display recorder info
    WScript.Echo "--------------------------------------------------"
    Wscript.Echo " ActiveRecorderId: " & recorder.ActiveDiscRecorder
    Wscript.Echo "        Vendor Id: " & recorder.VendorId
    Wscript.Echo "       Product Id: " & recorder.ProductId
    Wscript.Echo " Product Revision: " & recorder.ProductRevision
    Wscript.Echo "       VolumeName: " & recorder.VolumeName
    Wscript.Echo "   Can Load Media: " & recorder.DeviceCanLoadMedia
    Wscript.Echo "    Device Number: " & recorder.LegacyDeviceNumber

    Dim mountPoint
    For Each mountPoint In recorder.VolumePathNames
        WScript.Echo "      Mount Point: " & mountPoint
    Next

    WScript.Echo "Supported Features"  'in _IMAPI_FEATURE_PAGE_TYPE 
    Dim supportedFeature
    For Each supportedFeature  in recorder.SupportedFeaturePages
        if supportedFeature = _
            IMAPI_FEATURE_PAGE_TYPE_DVD_DASH_WRITE then
                WScript.Echo "    Feature: " & supportedFeature & _
                    "  Drive supports DVD-RW."
        else
                     WScript.Echo "    Feature: " & supportedFeature
        end if
    Next
    
    WScript.Echo "Current Features"    'in _IMAPI_FEATURE_PAGE_TYPE
    Dim currentFeature
    For Each currentFeature  in recorder.CurrentFeaturePages
        WScript.Echo "    Feature: " & currentFeature
    Next
    
    WScript.Echo "Supported Profiles"  'in _IMAPI_PROFILE_TYPE
    Dim supportedProfile
    For Each supportedProfile  in recorder.SupportedProfiles
        WScript.Echo "    Profile: " & supportedProfile
    Next

    WScript.Echo "Current Profiles"    'in _IMAPI_PROFILE_TYPE
    Dim currentProfile
    For Each currentProfile    in recorder.CurrentProfiles
        WScript.Echo "    Profile: " & currentProfile
    Next
    
    WScript.Echo "Supported Mode Pages"  'in  _IMAPI_MODE_PAGE_TYPE
    Dim supportedModePage       
    For Each supportedModePage in recorder.SupportedModePages
        WScript.Echo "    Mode Page: " & supportedModePage
    Next

    WScript.Echo
    WScript.Echo "----- Finished content -----"
    Main = 0
End Function
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de IMAPI](using-imapi.md)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[**TIPO DE \_ PÁGINA DE \_ CARACTERÍSTICAS \_ IMAPI**](/windows/desktop/api/imapi2/ne-imapi2-imapi_feature_page_type)
</dt> <dt>

[**TIPO DE PÁGINA \_ MODO \_ \_ IMAPI**](/windows/desktop/api/imapi2/ne-imapi2-imapi_mode_page_type)
</dt> <dt>

[**TIPO DE PERFIL \_ \_ IMAPI**](/windows/desktop/api/imapi2/ne-imapi2-imapi_profile_type)
</dt> </dl>

 

 




