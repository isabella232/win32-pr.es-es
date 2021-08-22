---
description: Las funciones getservbyname y getservbyport usan la función WSALookupServiceBegin para consultar SVCID \_ INET SERVICEBYNAME como GUID de clase \_ de servicio.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: getservbyname y getservbyport Functions en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e5d7cc9b1811eef98cc6d337abc3230ea46bd537a19969a4b412473e671b39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132218"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a>getservbyname y getservbyport Functions en la API

Las [**funciones getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) y [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) usan la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ INET SERVICEBYNAME como GUID de clase \_ de servicio. El *miembro lpszServiceInstanceName* de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) pasado a la función **WSALookupServiceBegin** hace referencia a una cadena para indicar el nombre del servicio o el puerto del servicio, y (opcionalmente) el protocolo de servicio. El formato de la cadena se muestra como FTP, TCP, 21/TCP o simplemente FTP. La cadena no distingue mayúsculas de minúsculas. La marca de barra diagonal, si está presente, separa el identificador de protocolo de la parte anterior de la cadena. El32.dll Ws2 especificará LUP RETURN BLOB y el proveedor de espacios de nombres colocará una estructura SERPLACE en el blob (mediante desplazamientos en lugar de punteros, como se ha \_ \_ descrito \_ anteriormente). [](/windows/desktop/api/winsock/ns-winsock-servent) Los proveedores de espacios de nombres también deben respetar estas \_ otras marcas RETURN de \_ \* LUP.

| Marca              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOMBRE DEVUELTO \_ DE \_ LUP | Devuelve el **miembro de nombre \_ de** la [**estructura SER SERIALIZA**](/windows/desktop/api/winsock/ns-winsock-servent) en *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                               |
| TIPO DE VALOR \_ DEVUELTO DE \_ LUP | Devuelve guid canónico en *lpServiceClassId.* Se entiende que un servicio identificado como FTP o 21 puede estar en otro puerto según las convenciones establecidas localmente. El **parámetro de puerto \_ s** de la [**estructura SER SERIALIZA**](/windows/desktop/api/winsock/ns-winsock-servent) debe indicar dónde se puede ponerse en contacto con el servicio en el entorno local. El GUID canónico devuelto cuando se establece LUP RETURN TYPE debe ser uno de los GUID predefinidos de \_ Svcs.h que corresponde al número de puerto indicado en la \_ **estructura SER GUID.** |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres compatible para TCP/IP en la API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolución de nombres independiente del protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



