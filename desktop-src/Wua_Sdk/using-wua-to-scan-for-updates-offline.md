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
# <a name="using-wua-to-scan-for-updates-offline"></a><span data-ttu-id="279c9-104">Usar WUA para buscar actualizaciones sin conexión</span><span class="sxs-lookup"><span data-stu-id="279c9-104">Using WUA to Scan for Updates Offline</span></span>

<span data-ttu-id="279c9-105">Windows Update Agent (WUA) se puede usar para examinar equipos en busca de actualizaciones de seguridad sin necesidad de conectarse a Windows Update o a un servidor de Windows Server Update Services (WSUS), lo que permite que los equipos que no están conectados a Internet puedan examinar las actualizaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="279c9-105">Windows Update Agent (WUA) can be used to scan computers for security updates without connecting to Windows Update or to a Windows Server Update Services (WSUS) server, which enables computers that are not connected to the Internet to be scanned for security updates.</span></span>

<span data-ttu-id="279c9-106">El análisis sin conexión de las actualizaciones requiere la descarga de un archivo firmado, Wsusscn2.cab, de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="279c9-106">Offline scanning for updates requires the download of a signed file, Wsusscn2.cab, from Windows Update.</span></span>

<span data-ttu-id="279c9-107">El archivo Wsusscn2.cab es un archivo. CAB firmado por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="279c9-107">The Wsusscn2.cab file is a cabinet file that is signed by Microsoft.</span></span> <span data-ttu-id="279c9-108">Este archivo contiene información acerca de las actualizaciones relacionadas con la seguridad publicadas por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="279c9-108">This file contains info about security-related updates that are published by Microsoft.</span></span> <span data-ttu-id="279c9-109">Los equipos que no están conectados a Internet se pueden examinar para ver si estas actualizaciones relacionadas con la seguridad están presentes o son necesarias.</span><span class="sxs-lookup"><span data-stu-id="279c9-109">Computers that aren't connected to the Internet can be scanned to see whether these security-related updates are present or required.</span></span> <span data-ttu-id="279c9-110">El archivo Wsusscn2.cab no contiene las actualizaciones de seguridad por sí mismos, por lo que debe obtener e instalar las actualizaciones relacionadas con la seguridad necesarias a través de otros medios.</span><span class="sxs-lookup"><span data-stu-id="279c9-110">The Wsusscn2.cab file doesn't contain the security updates themselves so you must obtain and install any needed security-related updates through other means.</span></span> <span data-ttu-id="279c9-111">Las nuevas versiones del archivo Wsusscn2.cab se publican periódicamente a medida que se publican, quitan o revisan las actualizaciones relacionadas con la seguridad en el sitio de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="279c9-111">New versions of the Wsusscn2.cab file are released periodically as security-related updates are released, removed, or revised on the Windows Update site.</span></span> <span data-ttu-id="279c9-112">El archivo de Wsusscn2.cab más reciente está disponible para su descarga en la siguiente ubicación: [descargar Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span><span class="sxs-lookup"><span data-stu-id="279c9-112">The latest Wsusscn2.cab file is available for download at the following location: [Download Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span></span>

<span data-ttu-id="279c9-113">Después de descargar el Wsusscn2.cab más reciente, se puede proporcionar el archivo al método [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) y se puede usar la API de WUA para buscar actualizaciones de seguridad en el equipo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="279c9-113">After you download the latest Wsusscn2.cab, the file can be provided to the [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) method, and the WUA API can be used to search the offline computer for security updates.</span></span> <span data-ttu-id="279c9-114">WUA valida que el Wsusscn2.cab está firmado por un certificado válido de Microsoft antes de ejecutar un examen sin conexión.</span><span class="sxs-lookup"><span data-stu-id="279c9-114">WUA validates that the Wsusscn2.cab is signed by a valid Microsoft certificate before running an offline scan.</span></span>

> [!NOTE]
> <span data-ttu-id="279c9-115">De acuerdo con nuestra [iniciativa de desuso de SHA-1](https://aka.ms/sha1deprecation), el archivo Wsusscn2.cab ya no tiene una firma doble mediante SHA-1 y el conjunto de algoritmos hash Sha-2 (específicamente, sha-256).</span><span class="sxs-lookup"><span data-stu-id="279c9-115">In accordance with our [SHA-1 deprecation initiative](https://aka.ms/sha1deprecation), the Wsusscn2.cab file is no longer dual-signed using both SHA-1 and the SHA-2 suite of hash algorithms (specifically SHA-256).</span></span> <span data-ttu-id="279c9-116">Este archivo está firmado ahora solo con SHA-256.</span><span class="sxs-lookup"><span data-stu-id="279c9-116">This file is now signed using only SHA-256.</span></span> <span data-ttu-id="279c9-117">Los administradores que comprueban las firmas digitales en este archivo ahora deberían esperar solo firmas SHA-256.</span><span class="sxs-lookup"><span data-stu-id="279c9-117">Administrators who verify digital signatures on this file should now expect only single SHA-256 signatures.</span></span>

## <a name="example"></a><span data-ttu-id="279c9-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="279c9-118">Example</span></span>

<span data-ttu-id="279c9-119">En el ejemplo siguiente se usa el archivo Wsusscn2.cab para examinar un equipo y se muestran las actualizaciones que faltan.</span><span class="sxs-lookup"><span data-stu-id="279c9-119">The following example uses the Wsusscn2.cab file to scan a computer and displays updates that are missing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="279c9-120">Este script está pensado para demostrar el uso de las API del agente de Windows Update y proporcionar un ejemplo de cómo los desarrolladores pueden usar estas API para resolver los problemas.</span><span class="sxs-lookup"><span data-stu-id="279c9-120">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="279c9-121">Este script no está pensado como código de producción y Microsoft no admite el propio script (aunque se admiten las API del agente de Windows Update subyacentes).</span><span class="sxs-lookup"><span data-stu-id="279c9-121">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


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



 

 



