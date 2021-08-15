---
description: Windows El Agente de actualización (WUA) se puede usar para buscar actualizaciones de seguridad en los equipos sin conectarse a Windows Update o a un servidor Windows Server Update Services (WSUS), lo que permite que los equipos que no están conectados a Internet se analicen en busca de actualizaciones de seguridad. El examen sin conexión de actualizaciones requiere la descarga de un archivo firmado, Wsusscn2.cab, desde Windows Update.
ms.assetid: 452b53af-0f7b-435e-bf12-dd9d84cbd564
title: Uso de WUA para buscar actualizaciones sin conexión
ms.topic: article
ms.date: 07/23/2020
ms.openlocfilehash: 54da554eca4e2320ecb8644ffb7ae274ed929d897f6e17e28b271a682f9fdc59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410765"
---
# <a name="using-wua-to-scan-for-updates-offline"></a>Uso de WUA para buscar actualizaciones sin conexión

Windows El Agente de actualización (WUA) se puede usar para buscar actualizaciones de seguridad en los equipos sin conectarse a Windows Update o a un servidor Windows Server Update Services (WSUS), lo que permite que los equipos que no están conectados a Internet se analicen en busca de actualizaciones de seguridad.

El examen sin conexión de actualizaciones requiere la descarga de un archivo firmado, Wsusscn2.cab, desde Windows Update.

El Wsusscn2.cab archivo es un archivo de archivador firmado por Microsoft. Este archivo contiene información sobre las actualizaciones relacionadas con la seguridad publicadas por Microsoft. Los equipos que no están conectados a Internet se pueden examinar para ver si estas actualizaciones relacionadas con la seguridad están presentes o son necesarias. El Wsusscn2.cab no contiene las actualizaciones de seguridad por sí mismos, por lo que debe obtener e instalar las actualizaciones relacionadas con la seguridad necesarias a través de otros medios. Las nuevas versiones del archivo Wsusscn2.cab se lanzan periódicamente a medida que se liberan, quitan o revisan actualizaciones relacionadas con la seguridad en el Windows update. El archivo Wsusscn2.cab más reciente está disponible para su descarga en la siguiente ubicación: [Descargar Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)

Después de descargar la versión Wsusscn2.cab, el archivo se puede proporcionar al método [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) y la API de WUA se puede usar para buscar actualizaciones de seguridad en el equipo sin conexión. WUA valida que el Wsusscn2.cab está firmado por un certificado de Microsoft válido antes de ejecutar un examen sin conexión.

> [!NOTE]
> De acuerdo con nuestra iniciativa de desuso de [SHA-1,](https://aka.ms/sha1deprecation)el archivo Wsusscn2.cab ya no tiene doble firma mediante SHA-1 y el conjunto de algoritmos hash SHA-2 (específicamente SHA-256). Este archivo ahora está firmado solo con SHA-256. Los administradores que comprueban las firmas digitales en este archivo ahora solo deben esperar firmas SHA-256 únicas.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se usa el Wsusscn2.cab para examinar un equipo y se muestran las actualizaciones que faltan.

> [!IMPORTANT]
> Este script está pensado para mostrar el uso de las API del agente de actualización de Windows y proporcionar un ejemplo de cómo los desarrolladores pueden usar estas API para solucionar problemas. Este script no está pensado como código de producción y Microsoft no admite el propio script (aunque se admiten las API Windows Update Agent subyacentes).

 


```VB
Set UpdateSession = CreateObject("Microsoft.Update.Session")
Set UpdateServiceManager = CreateObject("Microsoft.Update.ServiceManager")
Set UpdateService = UpdateServiceManager.AddScanPackageService("Offline Sync Service", "c:\wsusscn2.cab", 1)
Set UpdateSearcher = UpdateSession.CreateUpdateSearcher()

WScript.Echo "Searching for updates..." & vbCRLF

UpdateSearcher.ServerSelection = 3 ' ssOthers

UpdateSearcher.ServiceID = UpdateService.ServiceID

Set SearchResult = UpdateSearcher.Search("IsInstalled=0")

Set Updates = SearchResult.Updates

If searchResult.Updates.Count = 0 Then
    WScript.Echo "There are no applicable updates."
    WScript.Quit
End If

WScript.Echo "List of applicable items on the machine when using wssuscan.cab:" & vbCRLF

For I = 0 to searchResult.Updates.Count-1
    Set update = searchResult.Updates.Item(I)
    WScript.Echo I + 1 & "> " & update.Title
Next

WScript.Quit
```



 

 



