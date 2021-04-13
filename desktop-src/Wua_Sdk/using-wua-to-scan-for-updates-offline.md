---
description: Windows Update Agent (WUA) se puede usar para examinar equipos en busca de actualizaciones de seguridad sin necesidad de conectarse a Windows Update o a un servidor de Windows Server Update Services (WSUS), lo que permite que los equipos que no están conectados a Internet puedan examinar las actualizaciones de seguridad. El análisis sin conexión de las actualizaciones requiere la descarga de un archivo firmado, Wsusscn2.cab, de Windows Update.
ms.assetid: 452b53af-0f7b-435e-bf12-dd9d84cbd564
title: Usar WUA para buscar actualizaciones sin conexión
ms.topic: article
ms.date: 07/23/2020
ms.openlocfilehash: 242ff3655f4ab469d8d768a94f8dc8e529e0da74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360143"
---
# <a name="using-wua-to-scan-for-updates-offline"></a>Usar WUA para buscar actualizaciones sin conexión

Windows Update Agent (WUA) se puede usar para examinar equipos en busca de actualizaciones de seguridad sin necesidad de conectarse a Windows Update o a un servidor de Windows Server Update Services (WSUS), lo que permite que los equipos que no están conectados a Internet puedan examinar las actualizaciones de seguridad.

El análisis sin conexión de las actualizaciones requiere la descarga de un archivo firmado, Wsusscn2.cab, de Windows Update.

El archivo Wsusscn2.cab es un archivo. CAB firmado por Microsoft. Este archivo contiene información acerca de las actualizaciones relacionadas con la seguridad publicadas por Microsoft. Los equipos que no están conectados a Internet se pueden examinar para ver si estas actualizaciones relacionadas con la seguridad están presentes o son necesarias. El archivo Wsusscn2.cab no contiene las actualizaciones de seguridad por sí mismos, por lo que debe obtener e instalar las actualizaciones relacionadas con la seguridad necesarias a través de otros medios. Las nuevas versiones del archivo Wsusscn2.cab se publican periódicamente a medida que se publican, quitan o revisan las actualizaciones relacionadas con la seguridad en el sitio de Windows Update. El archivo de Wsusscn2.cab más reciente está disponible para su descarga en la siguiente ubicación: [descargar Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)

Después de descargar el Wsusscn2.cab más reciente, se puede proporcionar el archivo al método [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) y se puede usar la API de WUA para buscar actualizaciones de seguridad en el equipo sin conexión. WUA valida que el Wsusscn2.cab está firmado por un certificado válido de Microsoft antes de ejecutar un examen sin conexión.

> [!NOTE]
> De acuerdo con nuestra [iniciativa de desuso de SHA-1](https://aka.ms/sha1deprecation), el archivo Wsusscn2.cab ya no tiene una firma doble mediante SHA-1 y el conjunto de algoritmos hash Sha-2 (específicamente, sha-256). Este archivo está firmado ahora solo con SHA-256. Los administradores que comprueban las firmas digitales en este archivo ahora deberían esperar solo firmas SHA-256.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se usa el archivo Wsusscn2.cab para examinar un equipo y se muestran las actualizaciones que faltan.

> [!IMPORTANT]
> Este script está pensado para demostrar el uso de las API del agente de Windows Update y proporcionar un ejemplo de cómo los desarrolladores pueden usar estas API para resolver los problemas. Este script no está pensado como código de producción y Microsoft no admite el propio script (aunque se admiten las API del agente de Windows Update subyacentes).

 


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



 

 



