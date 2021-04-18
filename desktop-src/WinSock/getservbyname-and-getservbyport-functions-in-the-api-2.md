---
description: Las funciones getservbyname y getservbyport usan la función WSALookupServiceBegin para consultar SVCID \_ inet \_ SERVICEBYNAME como el GUID de la clase de servicio.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Funciones getservbyname y getservbyport en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715125"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a>Funciones getservbyname y getservbyport en la API

Las funciones [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) y [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) usan la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ inet \_ SERVICEBYNAME como el GUID de la clase de servicio. El miembro *lpszServiceInstanceName* de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) que se pasa a la función **WSALookupServiceBegin** hace referencia a una cadena para indicar el nombre del servicio o el puerto del servicio y, opcionalmente, el protocolo del servicio. El formato de la cadena se muestra como FTP, TCP o 21/TCP o simplemente FTP. La cadena no distingue entre mayúsculas y minúsculas. La marca de barra diagonal, si está presente, separa el identificador de protocolo de la parte anterior de la cadena. El \_32.dll Ws2 especificará LUP \_ devolverá el \_ BLOB y el proveedor de espacios de nombres colocará una estructura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) en el BLOB (mediante desplazamientos en lugar de punteros, como se describió anteriormente). Los proveedores de espacios de nombres deben cumplir también estas otras \_ \_ \* marcas de devolución de LUP.

| Marca              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_nombre devuelto de LUP \_ | Devuelve el miembro de **\_ nombre s** de la estructura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) en *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_tipo de valor devuelto LUP \_ | Devuelve el GUID canónico en *lpServiceClassId* . se entiende que un servicio identificado como FTP o 21 puede estar en otro puerto de acuerdo con las convenciones establecidas localmente. El parámetro de **\_ Puerto s** de la estructura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) debe indicar dónde se puede establecer contacto con el servicio en el entorno local. El GUID canónico devuelto cuando el \_ tipo de valor devuelto LUP \_ está establecido debe ser uno de los GUID predefinidos de SVC. h que corresponde al número de puerto indicado en la estructura **SERVENT** . |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolución de nombres independiente del Protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



