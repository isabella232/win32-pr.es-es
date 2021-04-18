---
description: La función GetHostName (usa la función WSALookupServiceBegin para consultar el \_ nombre de host de SVCID como el GUID de la clase de servicio.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Función GetHostName (en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715129"
---
# <a name="gethostname-function-in-the-api"></a>Función GetHostName (en la API

La función [**GetHostName (**](/windows/desktop/api/winsock/nf-winsock-gethostname) usa la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar el \_ nombre de host de SVCID como el GUID de la clase de servicio. Si el miembro **lpszServiceInstanceName** de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) pasada a la función **WSALookupServiceBegin** es **null** o hace referencia a una cadena **nula** (es decir, ""), el host local se va a resolver. De lo contrario, se produce una búsqueda en un nombre de host especificado. Con el fin de emular **GetHostName (** , el Ws2 \_32.dll especifica un puntero **nulo** para el miembro **lpszServiceInstanceName** y especifica LUP \_ nombre devuelto para \_ que el nombre de host se devuelva en el miembro **lpszServiceInstanceName** . Si una aplicación usa esta consulta y especifica LUP \_ Return \_ addr, la dirección del host se proporciona en una estructura de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . La \_ acción devolver \_ BLOB de LUP no está definida para esta consulta. El valor predeterminado de la información de puerto es cero, a menos que el miembro **lpszQueryString** de la estructura **WSAQUERYSET** que se pasa a la función **WSALookupServiceBegin** haga referencia a un servicio como FTP, en cuyo caso se proporciona la dirección de transporte completa del servicio indicado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolución de nombres independiente del Protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
