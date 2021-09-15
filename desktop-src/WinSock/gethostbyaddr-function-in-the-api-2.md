---
description: La función gethostbyaddr usa la función WSALookupServiceBegin para consultar SVCID \_ INET HOSTNAMEBYADDR como GUID de \_ clase de servicio.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Gethostbyaddr (Función) en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566853"
---
# <a name="gethostbyaddr-function-in-the-api"></a>Gethostbyaddr (Función) en la API

La [**función gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) usa la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ INET HOSTNAMEBYADDR como GUID de \_ clase de servicio. La dirección del host se proporciona como una cadena IPv4 decimnal con puntos (por ejemplo, "192.9.200.120") en el miembro *lpszServiceInstanceName* de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) pasada a la función **WSALookupServiceBegin.** El Ws232.dll especifica LUP RETURN BLOB y el proveedor de servicios de nombres coloca una estructura HOSTENT en el blob (mediante desplazamientos en lugar de punteros, como se describió \_ \_ \_ anteriormente). [](/windows/desktop/api/winsock/ns-winsock-hostent) Los proveedores de servicios de nombres también deben respetar estas \_ otras marcas LUP \_ \* RETURN. 

| Marca              | Descripción                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOMBRE DEVUELTO DE LUP \_ \_ | Devuelve el **miembro \_ h name** de la estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) *en lpszServiceInstanceName*.                                                     |
| LUP \_ RETURN \_ ADDR | Devuelve información de direccionamiento de [**HOSTENT en**](/windows/desktop/api/winsock/ns-winsock-hostent) [**estructuras INFO de CSADDR, \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) la información del puerto tiene como valor predeterminado cero. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres compatible para TCP/IP en la API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolución de nombres independientes del protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
