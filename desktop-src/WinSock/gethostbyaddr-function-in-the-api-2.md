---
description: La función gethostbyaddr usa la función WSALookupServiceBegin para consultar SVCID \_ INET HOSTNAMEBYADDR como GUID de \_ clase de servicio.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Gethostbyaddr (Función) en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac84d30ba919a4fc61456d5ca4772c12df786d89241e8249b57068b9aac3f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132328"
---
# <a name="gethostbyaddr-function-in-the-api"></a>Gethostbyaddr (Función) en la API

La [**función gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) usa la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ INET HOSTNAMEBYADDR como GUID de \_ clase de servicio. La dirección del host se proporciona como una cadena IPv4 decimnal con puntos (por ejemplo, "192.9.200.120") en el miembro *lpszServiceInstanceName* de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) pasada a la función **WSALookupServiceBegin.** El32.dll Ws2 especifica LUP RETURN BLOB y el proveedor de servicios de nombres coloca una estructura HOSTENT en el blob (mediante desplazamientos en lugar de punteros, como se ha \_ \_ descrito \_ anteriormente). [](/windows/desktop/api/winsock/ns-winsock-hostent) Los proveedores de servicios de nombres también deben respetar estas \_ otras marcas RETURN de \_ \* LUP. 

| Marca              | Descripción                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOMBRE DEVUELTO \_ DE \_ LUP | Devuelve el **miembro h \_ name** de [**la estructura HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) *en lpszServiceInstanceName*.                                                     |
| LUP \_ RETURN \_ ADDR | Devuelve información de direccionamiento de [**HOSTENT en**](/windows/desktop/api/winsock/ns-winsock-hostent) [**estructuras INFO de CSADDR; \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) la información del puerto tiene como valor predeterminado cero. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres compatible para TCP/IP en la API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolución de nombres independiente del protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
