---
description: NSPGetServiceClassInfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Funciones auxiliares en SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705613"
---
# <a name="helper-functions-in-the-spi"></a>Funciones auxiliares en SPI

-   [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

La función [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) recupera la información de esquema de clase de servicio que un proveedor de espacios de nombres ha conservado. También lo usa el archivo DLL de Windows Sockets 2 en su implementación de [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).

Las siguientes macros se definen en el archivo de encabezado *Svcguid. h* y pueden ayudar en la asignación entre las clases de servicio conocidas y los espacios de nombres.

| Un nombre de macro                                                                              | Descripción                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_TCP SVCID (puerto)**<br/> **SVCID \_ UDP (puerto)**<br/>                         | Dado un puerto TCP o UDP para el protocolo de Internet, devuelve el GUID.                                                                               |
| **ES \_ SVCID \_ TCP (GUID)**<br/> **ES \_ SVCID \_ UDP (GUID)**<br/>                 | Devuelve **true** si el GUID para TCP o UDP está dentro del intervalo permitido.                                                                         |
| **Puerto \_ de \_ SVCID \_ TCP (GUID)**<br/> **Puerto \_ de \_ SVCID \_ UDP (GUID)**<br/> | Devuelve el puerto TCP o UDP asociado al GUID.                                                                                              |
| **SVCID \_ NetWare (SAPID)**<br/>                                                    | Dado el identificador de protocolo de anuncio de servicio (SAP), devuelve el GUID. Esta macro se usa con el espacio de nombres de SAP en un entorno de NetWare. |
| **SAPID \_ de \_ SVCID \_ NetWare (GUID)**<br/>                                        | Devuelve el identificador de NetWare SAP asociado al GUID. Esta macro se usa con el espacio de nombres de SAP en un entorno de NetWare.               |
| **ES \_ SVCID \_ NetWare (GUID)**<br/>                                                 | Devuelve **true** si el GUID para NetWare está dentro del intervalo permitido. Esta macro se usa con el espacio de nombres de SAP en un entorno de NetWare.    |



 

> [!Note]  
> El archivo de encabezado *Svcguid. h* no se incluye automáticamente en el archivo de encabezado *WinSock2. h* .

 

 

 




