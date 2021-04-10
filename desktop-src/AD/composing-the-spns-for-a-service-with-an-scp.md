---
title: Creación de los SPN para un servicio con un SCP
description: En el ejemplo de código siguiente se compone un SPN para un servicio que usa un punto de conexión de servicio (SCP).
ms.assetid: cbaa11ba-d32b-46cf-86a4-9050bb1be3a6
ms.tgt_platform: multiple
keywords:
- Creación de los SPN para un servicio con un AD de SCP
- Nombre de entidad de seguridad de servicio AD, creación de SPN para un servicio con un SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a9c44bc603372af35e874acfea4c1e12a2433d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075017"
---
# <a name="composing-the-spns-for-a-service-with-an-scp"></a>Creación de los SPN para un servicio con un SCP

En el ejemplo de código siguiente se compone un SPN para un servicio que usa un punto de conexión de servicio (SCP). El SPN devuelto tiene el formato siguiente.


```C++
<service class>/<host>/<service name>
```



" &lt; clase &gt; de servicio" y " &lt; nombre de servicio &gt; " se corresponden con los parámetros *pszDNofSCP* y *pszServiceClass* . " &lt; host &gt; " tiene como valor predeterminado el nombre DNS del equipo local.


```C++
DWORD
SpnCompose(
    TCHAR ***pspn,          // Output: an array of SPNs
    unsigned long *pulSpn,  // Output: the number of SPNs returned
    TCHAR *pszDNofSCP,      // Input: DN of the service's SCP
    TCHAR* pszServiceClass) // Input: the name of the service class
{
DWORD   dwStatus;    
 
dwStatus = DsGetSpn(
    DS_SPN_SERVICE, // Type of SPN to create (enumerated type)
    pszServiceClass, // Service class - a name in this case
    pszDNofSCP, // Service name - DN of the service SCP
    0, // Default: omit port component of SPN
    0, // Number of entries in hostnames and ports arrays
    NULL, // Array of hostnames. Default is local computer
    NULL, // Array of ports. Default omits port component
    pulSpn, // Receives number of SPNs returned in array
    pspn // Receives array of SPN(s)
    );
 
return dwStatus;
}
```



 

 




