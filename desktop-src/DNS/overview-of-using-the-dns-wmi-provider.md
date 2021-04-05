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
# <a name="overview-of-using-the-dns-wmi-provider"></a>Información general sobre el uso del proveedor WMI de DNS

Los siguientes pasos generales le ayudarán a empezar a crear su propio script o programa que utiliza el proveedor WMI de DNS.

**Para crear un script o programa mediante el proveedor WMI de DNS**

1.  Conéctese al proveedor WMI de DNS.
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > El espacio de nombres para el proveedor WMI de DNS siempre será " \\ microsoftdns raíz".

     

2.  Obtener una instancia del servidor DNS.
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  En función de la acción de tipo que desee realizar, obtenga una zona DNS o una instancia de registro.
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  Realice las acciones deseadas:
    -   Ejecutar un método
    -   Mostrar una propiedad
    -   Modificar una propiedad (debe tener acceso de lectura y escritura)

 

 




