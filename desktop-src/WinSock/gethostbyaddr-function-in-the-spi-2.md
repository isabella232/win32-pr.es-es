---
description: La consulta WSALookupServiceBegin usa SVCID \_ INET \_ HOSTNAMEBYADDR como GUID de clase de servicio.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Gethostbyaddr (Función) en spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e343bcd66b7b1482f14a07239ae73710fd789486633219952696406dd8f1bd3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132318"
---
# <a name="gethostbyaddr-function-in-the-spi"></a>Gethostbyaddr (Función) en spi

La [**consulta WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ INET \_ HOSTNAMEBYADDR como GUID de clase de servicio. La dirección del host se proporciona en *lpszServiceInstanceName* como una cadena de dirección IPv4 con puntos decimales (por ejemplo, 192.9.200.120). El *32.dllWs2 \_ especifica* LUP RETURN BLOB y el NSP coloca una estructura HOSTENT en el blob (mediante desplazamientos en lugar de \_ \_ punteros, [](/windows/desktop/api/winsock/ns-winsock-hostent) como se describió anteriormente). Los NSP también deben respetar estas \_ otras marcas LUP \_ \* RETURN.



| Marca              | Descripción                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOMBRE DEVUELTO DE LUP \_ \_ | Devuelve el **miembro \_ h name** de la estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) *en lpszServiceInstanceName*.                                                     |
| LUP \_ RETURN \_ ADDR | Devuelve información de direccionamiento de [**HOSTENT en**](/windows/desktop/api/winsock/ns-winsock-hostent) [**estructuras INFO de CSADDR; \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) la información de puerto tiene como valor predeterminado cero. |



 

 

 
