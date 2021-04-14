---
description: La consulta WSALookupServiceBegin usa SVCID \_ inet \_ HOSTNAMEBYADDR como el GUID de la clase de servicio.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Función gethostbyaddr en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541587"
---
# <a name="gethostbyaddr-function-in-the-spi"></a>Función gethostbyaddr en el SPI

La consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ inet \_ HOSTNAMEBYADDR como el GUID de la clase de servicio. La dirección de host se proporciona en *lpszServiceInstanceName* como una cadena de dirección IPv4 decimal con puntos (por ejemplo, 192.9.200.120). El *\_32.dllWS2* especifica LUP \_ devolverá el \_ BLOB y el NSP coloca una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en el BLOB (mediante desplazamientos en lugar de punteros, como se describió anteriormente). Los NSP deben respetar también estas \_ otras \_ \* marcas de devolución de LUP.



| Marca              | Descripción                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_nombre devuelto de LUP \_ | Devuelve el miembro de **\_ nombre h** de la estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en *lpszServiceInstanceName*.                                                     |
| LUP \_ devolver \_ dirección | Devuelve la información de dirección de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en las estructuras de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . el valor predeterminado de la información de puerto es cero. |



 

 

 
