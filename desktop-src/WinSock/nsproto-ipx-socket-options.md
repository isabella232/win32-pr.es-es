---
description: En las tablas siguientes se describen las opciones de socket IPX de NSPROTO que se aplican a los sockets creados para la familia de direcciones \_ IPX/SPX (AF \_ IPX). Consulte las páginas de referencia de las funciones getsockopt y setsockopt para obtener más información sobre cómo obtener y establecer opciones de socket.
ms.assetid: 0d5c8299-14d7-41e5-8ff6-f57a732acb26
title: NSPROTO_IPX sockets (Wsnwlink.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e1fabed1963c3549d2d5a34fb432cac795e07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063974"
---
# <a name="nsproto_ipx-socket-options"></a>Opciones de socket IPX de NSPROTO \_

En las tablas siguientes se describen las opciones de socket **\_ IPX de NSPROTO** que se aplican a los sockets creados para la familia de direcciones IPX/SPX (AF \_ IPX). Consulte las páginas de referencia de las funciones [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obtener más información sobre cómo obtener y establecer opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas para cada protocolo instalado, use la función [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

<dl> <dt><span id="NSPROTO_IPX_Socket_Options"></span><span id="nsproto_ipx_socket_options"></span><span id="NSPROTO_IPX_SOCKET_OPTIONS"></span>**Opciones de socket IPX de NSPROTO \_**</dt> <dd> <dl> <dt> 

| Opción                      | Obtener | Set | Tipo optval                  | Descripción                                                                                                                                                                                                                                                                     |
|-----------------------------|-----|-----|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DIRECCIÓN \_ IPX                | sí |     | **DATOS DE DIRECCIONES IPX \_ \_**       | Devuelve información sobre el adaptador específico en el que está habilitado IPX.                                                                                                                                                                                                          |
| NOTIFICACIÓN DE \_ DIRECCIÓN IPX \_        | sí |     | **DATOS DE DIRECCIONES IPX \_ \_**       | Notifica de forma asincrónica cuando cambia el estado de un adaptador IPX.                                                                                                                                                                                                              |
| IPX \_ DSTYPE                 | sí | sí | DWORD                        | Obtiene o establece el valor del campo de flujo de datos en el encabezado SPX con el que se envían paquetes.                                                                                                                                                                                          |
| DIRECCIÓN EXTENDIDA DE IPX \_ \_      |     | sí | DWORD (booleano)              | Habilita la opción de direccionamiento extendido en paquetes IPX.                                                                                                                                                                                                                          |
| IPX \_ FILTERPTYPE            | sí | sí | DWORD                        | Obtiene o establece el tipo de paquete de filtro de recepción IPX actual. Solo se devolverán los paquetes IPX con un tipo de paquete igual al valor especificado en el parámetro optval. Se descartan los paquetes con un tipo de paquete que no coincide. Esto solo es aplicable a un socket de datagrama. |
| IPX \_ GETNETINFO             | sí |     | **IPX \_ NETNUM \_ DATA**        | Devuelve información relacionada con un número de red IPX específico. El miembro netnum de la estructura **IPX \_ NETNUM \_ DATA** debe establecerse en el número de red IPX que se va a devolver.                                                                                                     |
| IPX \_ GETNETINFO \_ NORIP      | sí |     | **IPX \_ NETNUM \_ DATA**        | Devuelve información relacionada con un número de red IPX específico sin enviar una solicitud RIP. El miembro netnum de la estructura **IPX \_ NETNUM \_ DATA** debe establecerse en el número de red IPX que se va a devolver.                                                                       |
| IPX \_ IMMEDIATESPXACK        |     | sí | DWORD (booleano)              | Si se establece **en TRUE,** no retrase el envío de ACKs en una conexión SPX.                                                                                                                                                                                                             |
| NÚMERO DE ADAPTADOR DE IPX \_ MAX \_ \_      | sí |     | DWORD                        | Devuelve el número de adaptadores habilitados para IPX presentes.                                                                                                                                                                                                                             |
| MAXSIZE de IPX \_                | sí |     | DWORD                        | Devuelve el tamaño máximo del datagrama IPX en bytes que se pueden enviar.                                                                                                                                                                                                                |
| IPX \_ PTYPE                  | sí | sí | DWORD                        | Obtiene o establece el tipo de paquete. El valor especificado en el parámetro optval se establecerá como el tipo de paquete en cada paquete IPX enviado desde este socket.                                                                                                                             |
| DIFUSIÓN DE RECEPCIÓN DE IPX \_ \_     |     | sí | DWORD (booleano)              | Si se establece en **TRUE,** reciba paquetes IPX de difusión.                                                                                                                                                                                                                              |
| IPX \_ RECVHDR                |     | sí | DWORD (booleano)              | Si se establece en **TRUE,** reciba encabezados de protocolo IPX con datos.                                                                                                                                                                                                                     |
| IPX \_ RERIPNETNUMBER         | sí |     | **IPX \_ NETNUM \_ DATA**        | Devuelve información sobre un número de red IPX especificado mediante una nueva solicitud RIP. El miembro netnum de la estructura **IPX \_ NETNUM \_ DATA** debe establecerse en el número de red IPX que se va a devolver.                                                                            |
| IPX \_ SPXGETCONNECTIONSTATUS | sí |     | **DATOS \_ DE IPX SPXCONNSTATUS \_** | Devuelve información relacionada con las estadísticas de sockets SPX conectados.                                                                                                                                                                                                                |
| IPX \_ STOPFILTERPTYPE        |     | sí | DWORD                        | Quita el filtro y deja de filtrar por el tipo de paquete especificado en el parámetro optval.                                                                                                                                                                                        |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_NSPROTO_IPX_options"></span><span id="windows_support_for_nsproto_ipx_options"></span><span id="WINDOWS_SUPPORT_FOR_NSPROTO_IPX_OPTIONS"></span>**Windows Compatibilidad con opciones de IPX de NSPROTO \_**</dt> <dd> <dl> <dt> 

| Opción                      | Windows Vista y versiones posteriores | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-----------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| DIRECCIÓN \_ IPX                |                         | x                   | x          | x            | x           | x             |
| NOTIFICACIÓN DE DIRECCIÓN IPX \_ \_        |                         | x                   | x          | x            | x           | x             |
| IPX \_ DSTYPE                 |                         | x                   | x          | x            | x           | x             |
| DIRECCIÓN EXTENDIDA DE IPX \_ \_      |                         | x                   | x          | x            | x           | x             |
| IPX \_ FILTERPTYPE            |                         | x                   | x          | x            | x           | x             |
| IPX \_ GETNETINFO             |                         | x                   | x          | x            | x           | x             |
| IPX \_ GETNETINFO \_ NORIP      |                         | x                   | x          | x            | x           | x             |
| IPX \_ IMMEDIATESPXACK        |                         | x                   | x          | x            | x           | x             |
| NÚMERO DE ADAPTADOR DE IPX \_ MAX \_ \_      |                         | x                   | x          | x            | x           | x             |
| MAXSIZE de IPX \_                |                         | x                   | x          | x            | x           | x             |
| IPX \_ PTYPE                  |                         | x                   | x          | x            | x           | x             |
| DIFUSIÓN DE RECEPCIÓN DE IPX \_ \_     |                         | x                   | x          | x            | x           | x             |
| IPX \_ RECVHDR                |                         | x                   | x          | x            | x           | x             |
| IPX \_ RERIPNETNUMBER         |                         | x                   | x          | x            | x           | x             |
| IPX \_ SPXGETCONNECTIONSTATUS |                         | x                   | x          | x            | x           | x             |
| IPX \_ STOPFILTERPTYPE        |                         | x                   | x          | x            | x           | x             |



 


</dt> </dl> </dd> </dl>

Las siguientes opciones de socket **\_ IPX de NSPROTO** se definieron en Windows Sockets 2 Protocol-Specific Anexo, pero no se implementan mediante el protocolo IPX/SPX de Windows.

*level* **=** **NSPROTO \_ IPX**



| Opción           | Tipo | Valor predeterminado                         | Significado                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SUMA DE COMPROBACIÓN DE IPX \_    | Bool | apagado                             | Cuando se establece, IPX realiza una suma de comprobación en los paquetes salientes y comprueba la suma de comprobación de los paquetes entrantes.                                                          |
| IPX \_ TXPKTSIZE   | int  | Tamaño del medio hasta un máximo de 1466 | Establece el tamaño máximo del datagrama de envío. Este tamaño no incluye el encabezado IPX ni ningún encabezado multimedia que también se pueda usar. Se puede aumentar al tamaño del medio.    |
| IPX \_ RXPKTSIZE   | int  | Tamaño del medio hasta un máximo de 1466 | Establece el tamaño máximo del datagrama de recepción. Este tamaño no incluye el encabezado IPX ni ningún encabezado multimedia que también se pueda usar. Se puede aumentar al tamaño del medio. |
| IPX \_ TXMEDIASIZE | int  | Placa principal                   | Devuelve el tamaño del medio de envío que establece un límite superior para el tamaño del datagrama.                                                                                       |
| IPX \_ RXMEDIASIZE | int  | Placa principal                   | Devuelve el tamaño del medio de recepción que establece un límite superior para el tamaño del datagrama.                                                                                    |
| IPX \_ PRIMARY     | Bool | Principal                         | Restringe el tráfico a la placa de red principal.                                                                                                               |



 

Las siguientes opciones de socket **\_ de SPX de NSPROTO** se definieron en el anexo de Windows Sockets 2 Protocol-Specific, pero no se implementan en Windows mediante el protocolo WINDOWS IPX/SPX.

*level* **=** **NSPROTO \_ SPX**



| Opción           | Tipo | Valor predeterminado                         | Significado                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SUMA DE COMPROBACIÓN DE SPX \_    | Bool | apagado                             | Cuando se establece, IPX realiza una suma de comprobación en los paquetes salientes y comprueba la suma de comprobación de los paquetes entrantes. No se admite en todas las plataformas.                          |
| SPX \_ TXPKTSIZE   | int  | Tamaño del medio hasta un máximo de 1466 | Establece el tamaño máximo del datagrama de envío. Este tamaño no incluye el encabezado SPX ni ningún encabezado multimedia que también se pueda usar. Se puede aumentar al tamaño del medio.    |
| SPX \_ RXPKTSIZE   | int  | Tamaño del medio hasta un máximo de 1466 | Establece el tamaño máximo del datagrama de recepción. Este tamaño no incluye el encabezado SPX ni ningún encabezado multimedia que también se pueda usar. Se puede aumentar al tamaño del medio. |
| SPX \_ TXMEDIASIZE | int  | Placa principal                   | Devuelve el tamaño del medio de envío menos SPX y encabezados multimedia. Esto establece un límite superior para el tamaño del paquete de segmentación de mensajes.                                       |
| SPX \_ RXMEDIASIZE | int  | Placa principal                   | Devuelve el tamaño del medio de recepción menos spx y encabezados multimedia. Esto establece un límite superior para el tamaño del paquete de recepción.                                                 |
| SPX \_ RAWSPX      | Bool | apagado                             | Cuando se establece, el encabezado de protocolo IPX/SPX se pasa con los datos.                                                                                                |



 

## <a name="remarks"></a>Observaciones

Las opciones de socket **\_ IPX de NSPROTO** y las estructuras usadas por estas opciones de socket se definen en el archivo de encabezado *Wsnwlink.h.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wsnwlink.h</dt> </dl> |



 

 




