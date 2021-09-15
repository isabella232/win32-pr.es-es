---
description: La función gethostname usa la función WSALookupServiceBegin para consultar SVCID HOSTNAME como GUID \_ de clase de servicio.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Gethostname (Función) en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566848"
---
# <a name="gethostname-function-in-the-api"></a>Gethostname (Función) en la API

La [**función gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) usa la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID HOSTNAME como GUID \_ de clase de servicio. Si el **miembro lpszServiceInstanceName** de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) pasado a la función **WSALookupServiceBegin** es **NULL** o hace referencia a una **cadena NULL** (es decir, . ""), el host local se va a resolver. De lo contrario, se produce una búsqueda en un nombre de host especificado. Para emular **gethostname,** el32.dll de Ws2 especifica un puntero NULL para el miembro \_ **lpszServiceInstanceName** y especifica LUP RETURN NAME para que el nombre de host se devuelva en el miembro  \_ \_ **lpszServiceInstanceName.** Si una aplicación usa esta consulta y especifica LUP RETURN ADDR, la dirección host se proporciona en una estructura \_ \_ INFO de [**CSADDR. \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) La acción LUP \_ RETURN BLOB no está definida para esta \_ consulta. El valor predeterminado de la información de puerto es cero a menos que el miembro **lpszQueryString** de la estructura **WSAQUERYSET** pasado a la función **WSALookupServiceBegin** haga referencia a un servicio como FTP, en cuyo caso se proporciona la dirección de transporte completa del servicio indicado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres compatible para TCP/IP en la API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolución de nombres independiente del protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
