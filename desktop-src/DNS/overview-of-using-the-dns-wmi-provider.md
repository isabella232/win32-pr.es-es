---
title: Información general sobre el uso del proveedor WMI de DNS
description: Los siguientes pasos generales le ayudarán a empezar a crear su propio script o programa que utiliza el proveedor WMI de DNS.
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9188e14e0a0b1f73380434be0d4298b0748da12f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076006"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a><span data-ttu-id="6e1ac-103">Información general sobre el uso del proveedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="6e1ac-103">Overview of Using the DNS WMI Provider</span></span>

<span data-ttu-id="6e1ac-104">Los siguientes pasos generales le ayudarán a empezar a crear su propio script o programa que utiliza el proveedor WMI de DNS.</span><span class="sxs-lookup"><span data-stu-id="6e1ac-104">The following general steps get you started in creating your own script or program that makes use of the DNS WMI Provider.</span></span>

<span data-ttu-id="6e1ac-105">**Para crear un script o programa mediante el proveedor WMI de DNS**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-105">**To create a script or program using the DNS WMI Provider**</span></span>

1.  <span data-ttu-id="6e1ac-106">Conéctese al proveedor WMI de DNS.</span><span class="sxs-lookup"><span data-stu-id="6e1ac-106">Connect to the DNS WMI Provider.</span></span>
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > <span data-ttu-id="6e1ac-107">El espacio de nombres para el proveedor WMI de DNS siempre será " \\ microsoftdns raíz".</span><span class="sxs-lookup"><span data-stu-id="6e1ac-107">The name space for the DNS WMI Provider will always be "root\\microsoftdns".</span></span>

     

2.  <span data-ttu-id="6e1ac-108">Obtener una instancia del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="6e1ac-108">Get a DNS Server instance.</span></span>
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  <span data-ttu-id="6e1ac-109">En función de la acción de tipo que desee realizar, obtenga una zona DNS o una instancia de registro.</span><span class="sxs-lookup"><span data-stu-id="6e1ac-109">Depending on the type action you want to perform, get a DNS zone or record instance.</span></span>
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  <span data-ttu-id="6e1ac-110">Realice las acciones deseadas:</span><span class="sxs-lookup"><span data-stu-id="6e1ac-110">Perform the desired actions:</span></span>
    -   <span data-ttu-id="6e1ac-111">Ejecutar un método</span><span class="sxs-lookup"><span data-stu-id="6e1ac-111">Execute a method</span></span>
    -   <span data-ttu-id="6e1ac-112">Mostrar una propiedad</span><span class="sxs-lookup"><span data-stu-id="6e1ac-112">Display a property</span></span>
    -   <span data-ttu-id="6e1ac-113">Modificar una propiedad (debe tener acceso de lectura y escritura)</span><span class="sxs-lookup"><span data-stu-id="6e1ac-113">Modify a property (must have Read/Write access)</span></span>

 

 




