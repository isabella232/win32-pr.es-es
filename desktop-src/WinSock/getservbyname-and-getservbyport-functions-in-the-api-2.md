---
description: Las funciones getservbyname y getservbyport usan la función WSALookupServiceBegin para consultar SVCID \_ INET SERVICEBYNAME como GUID de clase \_ de servicio.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Getservbyname y getservbyport Functions en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566845"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a>Getservbyname y getservbyport Functions en la API

Las [**funciones getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) y [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) usan la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ INET SERVICEBYNAME como GUID de clase \_ de servicio. El *miembro lpszServiceInstanceName* de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) que se pasa a la función **WSALookupServiceBegin** hace referencia a una cadena para indicar el nombre del servicio o el puerto del servicio y (opcionalmente) el protocolo de servicio. El formato de la cadena se muestra como FTP, TCP, 21/TCP o simplemente FTP. La cadena no distingue mayúsculas de minúsculas. La barra diagonal, si está presente, separa el identificador de protocolo de la parte anterior de la cadena. El32.dll Ws2 especificará LUP RETURN BLOB y el proveedor de espacios de nombres colocará una estructura SERPLACE en el blob (mediante desplazamientos en lugar de punteros, como se describió \_ \_ \_ anteriormente). [](/windows/desktop/api/winsock/ns-winsock-servent) Los proveedores de espacios de nombres también deben respetar estas \_ otras marcas LUP \_ \* RETURN.

| Marca              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOMBRE DEVUELTO DE LUP \_ \_ | Devuelve el **miembro de nombre \_ de** s de [**la estructura SER SERIALIZA**](/windows/desktop/api/winsock/ns-winsock-servent) en *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                               |
| TIPO DE VALOR \_ DEVUELTO DE \_ LUP | Devuelve guid canónico *en lpServiceClassId.* Se entiende que un servicio identificado como FTP o 21 puede estar en otro puerto según las convenciones establecidas localmente. El **parámetro de puerto \_ s** de la [**estructura SER SERIALIZA**](/windows/desktop/api/winsock/ns-winsock-servent) debe indicar dónde se puede ponerse en contacto con el servicio en el entorno local. El GUID canónico devuelto cuando se establece LUP RETURN TYPE debe ser uno de los GUID predefinidos de Svcs.h que se corresponde con el número de puerto indicado en la \_ \_ estructura **SERLEJOS.** |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres compatible para TCP/IP en la API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolución de nombres independientes del protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



