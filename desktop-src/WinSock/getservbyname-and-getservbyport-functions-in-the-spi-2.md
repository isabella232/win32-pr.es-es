---
description: La consulta WSALookupServiceBegin usa SVCID \_ inet \_ SERVICEBYNAME como el GUID de la clase de servicio.
ms.assetid: 72ee4a10-2864-48e3-a72c-ae069eb5aef3
title: Funciones getservbyname y getservbyport en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd910dc7ab478c262bd5ca6c480dc3ec58e1b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154281"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-spi"></a>Funciones getservbyname y getservbyport en el SPI

La consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ inet \_ SERVICEBYNAME como el GUID de la clase de servicio. El parámetro *lpszServiceInstanceName* hace referencia a una cadena que indica el nombre del servicio o el puerto del servicio y, opcionalmente, el protocolo del servicio. El formato de la cadena se ilustra como FTP/TCP o 21/TCP o simplemente FTP. La cadena no distingue entre mayúsculas y minúsculas. La marca de barra diagonal, si está presente, separa el identificador de protocolo de la parte anterior de la cadena. El \_32.dll Ws2 especificará LUP \_ devolverá el \_ BLOB y el NSP colocará una estructura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) en el BLOB (mediante desplazamientos en lugar de punteros, como se describió anteriormente). Los NSP deben respetar también estas \_ otras \_ \* marcas de devolución de LUP.



| Marca              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_nombre devuelto de LUP \_ | Devuelve el miembro de **\_ nombre s** de la estructura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) en *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_tipo de valor devuelto LUP \_ | Devuelve el GUID canónico en *lpServiceClassId* . se entiende que un servicio identificado como FTP o 21 puede estar en otro puerto de acuerdo con las convenciones establecidas localmente. El miembro del **\_ Puerto s** de la estructura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) debe indicar dónde se puede establecer contacto con el servicio en el entorno local. El GUID canónico devuelto cuando el \_ tipo de valor devuelto LUP \_ está establecido debe ser uno de los GUID predefinidos de SVC. h que corresponde al número de puerto indicado en la estructura **SERVENT** . |



 

 

 



