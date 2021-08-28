---
title: Información general sobre el uso del proveedor WMI de DNS
description: Los pasos generales siguientes le indican cómo crear su propio script o programa que usa el proveedor WMI de DNS.
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9eaa50e4ed1a237ed5b42abd4375ab301a2106498e929e42993cd634ca9ba18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077045"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a>Información general sobre el uso del proveedor WMI de DNS

Los pasos generales siguientes le indican cómo crear su propio script o programa que usa el proveedor WMI de DNS.

**Para crear un script o programa mediante el proveedor WMI de DNS**

1.  Conectar al proveedor WMI de DNS.
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > El espacio de nombres del proveedor WMI de DNS siempre será \\ "root microsoftdns".

     

2.  Obtenga una instancia del servidor DNS.
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  En función de la acción de tipo que quiera realizar, obtenga una zona DNS o una instancia de registro.
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  Realice las acciones deseadas:
    -   Ejecución de un método
    -   Mostrar una propiedad
    -   Modificar una propiedad (debe tener acceso de lectura y escritura)

 

 




