---
description: La consulta WSALookupServiceBegin usa SVCID \_ INET \_ SERVICEBYNAME como GUID de clase de servicio.
ms.assetid: 72ee4a10-2864-48e3-a72c-ae069eb5aef3
title: Getservbyname y getservbyport Functions en spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466966db2fc605b4043355746a1e606626e3d5d518452d1fab661dcfb68b3238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132168"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-spi"></a>Getservbyname y getservbyport Functions en spi

La [**consulta WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ INET \_ SERVICEBYNAME como GUID de clase de servicio. El *parámetro lpszServiceInstanceName hace* referencia a una cadena que indica el nombre del servicio o el puerto del servicio, y (opcionalmente) el protocolo de servicio. El formato de la cadena se muestra como ftp/tcp, 21/tcp o simplemente ftp. La cadena no distingue mayúsculas de minúsculas. La barra diagonal, si está presente, separa el identificador de protocolo de la parte anterior de la cadena. El32.dll Ws2 especificará LUP RETURN BLOB y el NSP colocará una estructura SERPLACE en el blob (mediante desplazamientos en lugar de punteros, como se describió \_ \_ \_ anteriormente). [](/windows/desktop/api/winsock/ns-winsock-servent) Los NSP también deben respetar estas \_ otras marcas LUP \_ \* RETURN.



| Marca              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOMBRE DEVUELTO DE LUP \_ \_ | Devuelve el **miembro de nombre \_ de** s de [**la estructura SER SERIALIZA**](/windows/desktop/api/winsock/ns-winsock-servent) en *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                            |
| TIPO DE VALOR \_ DEVUELTO DE \_ LUP | Devuelve guid canónico en *lpServiceClassId.* Se entiende que un servicio identificado como ftp o 21 puede estar en otro puerto según las convenciones establecidas localmente. El **miembro de puerto \_ s** de la [**estructura SER SERIALIZA**](/windows/desktop/api/winsock/ns-winsock-servent) debe indicar dónde se puede ponerse en contacto con el servicio en el entorno local. El GUID canónico devuelto cuando se establece LUP RETURN TYPE debe ser uno de los GUID predefinidos de svcs.h que se corresponde con el número de puerto indicado en la \_ \_ estructura **SERLEJOS.** |



 

 

 



