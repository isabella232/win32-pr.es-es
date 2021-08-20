---
description: NSPGetServiceClassInfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Funciones auxiliares en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0073eeb9310764ff100431da6491cedd322fa3c803f7465875980956d6059c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112160"
---
# <a name="helper-functions-in-the-spi"></a>Funciones auxiliares en el SPI

-   [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

La [**función NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) recupera información de esquema de clase de servicio que un proveedor de espacios de nombres ha conservado. También lo usa el archivo DLL Windows Sockets 2 en su implementación de [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).

Las macros siguientes se definen en el archivo de *encabezado Svcguid.h* y pueden ayudar a la asignación entre clases de servicio conocidas y estos espacios de nombres.

| Un nombre de macro                                                                              | Descripción                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **SVCID \_ TCP(Puerto)**<br/> **SVCID \_ UDP(Port)**<br/>                         | Dado un puerto TCP o UDP para el protocolo de Internet, devuelve el GUID.                                                                               |
| **IS \_ SVCID \_ TCP(GUID)**<br/> **IS \_ SVCID \_ UDP(GUID)**<br/>                 | Devuelve **TRUE** si el GUID de TCP o UDP está dentro del intervalo permitido.                                                                         |
| **PUERTO \_ DE \_ SVCID \_ TCP(GUID)**<br/> **PUERTO \_ DE \_ SVCID \_ UDP(GUID)**<br/> | Devuelve el puerto TCP o UDP asociado al GUID.                                                                                              |
| **SVCID \_ NETWARE(SAPID)**<br/>                                                    | Dado el identificador de Service Advertising Protocol (SAP), devuelve el GUID. Esta macro se usa con el espacio de nombres de SAP dentro de un entorno de NetWare. |
| **SAPID \_ DE \_ SVCID \_ NETWARE(GUID)**<br/>                                        | Devuelve el identificador sap de NetWare asociado al GUID. Esta macro se usa con el espacio de nombres de SAP dentro de un entorno de NetWare.               |
| **IS \_ SVCID \_ NETWARE(GUID)**<br/>                                                 | Devuelve **TRUE** si el GUID de NetWare está dentro del intervalo permitido. Esta macro se usa con el espacio de nombres de SAP dentro de un entorno de NetWare.    |



 

> [!Note]  
> El *archivo de encabezado Winsock2.h* no incluye automáticamente el archivo de encabezado *Svcguid.h.*

 

 

 




