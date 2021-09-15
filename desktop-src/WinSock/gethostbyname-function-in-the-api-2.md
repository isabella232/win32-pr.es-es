---
description: Función Gethostbyname en winsock API.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: Gethostbyname (Función) en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3881897a0c971c48ca9a02e6205ec1cae0476f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566849"
---
# <a name="gethostbyname-function-in-the-api"></a>Gethostbyname (Función) en la API

La [**función gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) usa la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ INET HOSTADDRBYNAME como GUID de \_ clase de servicio. El nombre de host se proporciona en el miembro **lpszServiceInstanceName** de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) pasada a la **función WSALookupServiceBegin.** El32.dll Ws2 especifica LUP RETURN BLOB y el proveedor de servicios de nombres coloca una estructura HOSTENT en el blob (mediante desplazamientos en lugar de punteros, como se ha \_ \_ descrito \_ anteriormente). [](/windows/desktop/api/winsock/ns-winsock-hostent) Los proveedores de servicios de nombres también deben respetar estas \_ otras marcas RETURN de \_ \* LUP.

| Marca              | Descripción                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOMBRE DEVUELTO \_ DE \_ LUP | Devuelve el **miembro h \_ name** de la [**estructura HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) *en lpszServiceInstanceName*.                                                                                                                                           |
| LUP \_ RETURN \_ ADDR | Devuelve información de direccionamiento de [**HOSTENT en**](/windows/desktop/api/winsock/ns-winsock-hostent) [**estructuras INFO de CSADDR; \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) la información del puerto tiene como valor predeterminado cero. Tenga en cuenta que esta rutina no resuelve los nombres de host que constan de una dirección IPv4 con puntos. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres compatible para TCP/IP en la API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolución de nombres independiente del protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
