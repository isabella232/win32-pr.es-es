---
description: Función gethostbyname en el SPI de Winsock.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: Función gethostbyname en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715130"
---
# <a name="gethostbyname-function-in-the-spi"></a>Función gethostbyname en el SPI

La consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ inet \_ HOSTADDRBYNAME como el GUID de la clase de servicio. El nombre de host se proporciona en *lpszServiceInstanceName*. El *\_32.dllWS2* especifica LUP \_ devolverá el \_ BLOB y el NSP coloca una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en el BLOB (mediante desplazamientos en lugar de punteros, como se describió anteriormente). Los NSP deben respetar también estas \_ otras \_ \* marcas de devolución de LUP.



| Marca              | Descripción                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_nombre devuelto de LUP \_ | Devuelve el miembro de **\_ nombre h** de la estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en *lpszServiceInstanceName*.                                                                                                                                                            |
| LUP \_ devolver \_ dirección | Devuelve la información de dirección de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en las estructuras de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . el valor predeterminado de la información de puerto es cero. Tenga en cuenta que esta rutina no resuelve los nombres de host que se componen de una cadena de dirección IPv4 decimal con puntos. |



 

 

 
