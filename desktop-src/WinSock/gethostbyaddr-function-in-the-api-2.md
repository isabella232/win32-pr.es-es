---
description: La función gethostbyaddr usa la función WSALookupServiceBegin para consultar SVCID \_ inet \_ HOSTNAMEBYADDR como el GUID de la clase de servicio.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Función gethostbyaddr en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715131"
---
# <a name="gethostbyaddr-function-in-the-api"></a>Función gethostbyaddr en la API

La función [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) usa la función [**WSALOOKUPSERVICEBEGIN**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ inet \_ HOSTNAMEBYADDR como el GUID de la clase de servicio. La dirección del host se proporciona como una cadena IPv4 decimnal con puntos (por ejemplo, "192.9.200.120") en el miembro *lpszServiceInstanceName* de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) pasada a la función **WSALookupServiceBegin** . El \_32.dll Ws2 especifica LUP \_ devolverá el \_ BLOB y el proveedor de servicios de nombres coloca una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en el BLOB (mediante desplazamientos en lugar de punteros, como se describió anteriormente). Los proveedores de servicios de nombres deben cumplir \_ también estas otras \_ \* marcas de devolución de LUP. 

| Marca              | Descripción                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_nombre devuelto de LUP \_ | Devuelve el miembro de **\_ nombre h** de la estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en *lpszServiceInstanceName*.                                                     |
| LUP \_ devolver \_ dirección | Devuelve la información de dirección de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en las estructuras de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . el valor predeterminado de la información de puerto es cero. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolución de nombres independiente del Protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
