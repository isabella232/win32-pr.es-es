---
description: En las tablas siguientes \_ se describen las opciones de socket de NSPROTO IPX que se aplican a los sockets creados para la familia de direcciones IPX/SPX (AF \_ IPX). Consulte las páginas de referencia de la función getsockopt y el valor de My para obtener más información sobre cómo obtener y establecer las opciones de socket.
ms.assetid: 0d5c8299-14d7-41e5-8ff6-f57a732acb26
title: Opciones de NSPROTO_IPX socket (Wsnwlink. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e1fabed1963c3549d2d5a34fb432cac795e07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650087"
---
# <a name="nsproto_ipx-socket-options"></a>NSPROTO \_ Opciones de socket IPX

En las tablas siguientes se describen las opciones de socket de **NSPROTO \_ IPX** que se aplican a los sockets creados para la familia de direcciones IPX/SPX (AF \_ IPX). Consulte las páginas de referencia de [**la función**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y el valor de My para obtener más información sobre cómo obtener y establecer las opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas de cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="NSPROTO_IPX_Socket_Options"></span><span id="nsproto_ipx_socket_options"></span><span id="NSPROTO_IPX_SOCKET_OPTIONS"></span>**NSPROTO \_ Opciones de socket IPX**</dt> <dd> <dl> <dt> 

| Opción                      | Obtener | Set | Tipo Optval                  | Descripción                                                                                                                                                                                                                                                                     |
|-----------------------------|-----|-----|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Dirección IPX                | sí |     | **\_datos de dirección IPX \_**       | Devuelve información acerca del adaptador específico en el que está habilitado IPX.                                                                                                                                                                                                          |
| \_notificación de dirección IPX \_        | sí |     | **\_datos de dirección IPX \_**       | Notifica de forma asincrónica cuando cambia el estado de un adaptador de IPX.                                                                                                                                                                                                              |
| \_DSTYPE IPX                 | sí | sí | DWORD                        | Obtiene o establece el valor del campo datastream en el encabezado SPX con el que se van a enviar paquetes.                                                                                                                                                                                          |
| \_dirección extendida de IPX \_      |     | sí | DWORD (booleano)              | Habilita la opción Extended Addressing en los paquetes IPX.                                                                                                                                                                                                                          |
| \_FILTERPTYPE IPX            | sí | sí | DWORD                        | Obtiene o establece el tipo de paquete del filtro de recepción de IPX actual. Solo se devolverán los paquetes IPX con un tipo de paquete igual al valor especificado en el parámetro optval. Los paquetes con un tipo de paquete que no coincide se descartan. Esto solo es aplicable a un socket de datagramas. |
| \_GETNETINFO IPX             | sí |     | **\_datos de NETNUM IPX \_**        | Devuelve información relacionada con un número de red IPX específico. El miembro netnum de la estructura de **\_ \_ datos netnum de IPX** debe establecerse en el número de red IPX que se va a devolver.                                                                                                     |
| \_NORIP GETNETINFO \_ IPX      | sí |     | **\_datos de NETNUM IPX \_**        | Devuelve información relacionada con un número de red IPX específico sin enviar una solicitud RIP. El miembro netnum de la estructura de **\_ \_ datos netnum de IPX** debe establecerse en el número de red IPX que se va a devolver.                                                                       |
| \_IMMEDIATESPXACK IPX        |     | sí | DWORD (booleano)              | Si se establece en **true**, no retrasar el envío de confirmaciones en una conexión de SPX.                                                                                                                                                                                                             |
| \_número máximo de \_ adaptadores \_ de IPX      | sí |     | DWORD                        | Devuelve el número de adaptadores habilitados para IPX.                                                                                                                                                                                                                             |
| tamaño máximo de IPX \_                | sí |     | DWORD                        | Devuelve el tamaño máximo del datagrama IPX en bytes que se puede enviar.                                                                                                                                                                                                                |
| \_PTYPE IPX                  | sí | sí | DWORD                        | Obtiene o establece el tipo de paquete. El valor especificado en el parámetro optval se establecerá como el tipo de paquete en cada paquete IPX enviado desde este socket.                                                                                                                             |
| \_difusión de recepción de IPX \_     |     | sí | DWORD (booleano)              | Si se establece en **true**, recibir paquetes IPX de difusión.                                                                                                                                                                                                                              |
| \_RECVHDR IPX                |     | sí | DWORD (booleano)              | Si se establece en **true**, se reciben encabezados de protocolo IPX con datos.                                                                                                                                                                                                                     |
| \_RERIPNETNUMBER IPX         | sí |     | **\_datos de NETNUM IPX \_**        | Devuelve información relacionada con un número de red IPX especificado mediante una nueva solicitud RIP. El miembro netnum de la estructura de **\_ \_ datos netnum de IPX** debe establecerse en el número de red IPX que se va a devolver.                                                                            |
| \_SPXGETCONNECTIONSTATUS IPX | sí |     | **\_datos de SPXCONNSTATUS IPX \_** | Devuelve información relacionada con las estadísticas conectadas del socket SPX.                                                                                                                                                                                                                |
| \_STOPFILTERPTYPE IPX        |     | sí | DWORD                        | Quita el filtro y detiene el filtrado en el tipo de paquete especificado en el parámetro optval.                                                                                                                                                                                        |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_NSPROTO_IPX_options"></span><span id="windows_support_for_nsproto_ipx_options"></span><span id="WINDOWS_SUPPORT_FOR_NSPROTO_IPX_OPTIONS"></span>**Compatibilidad de Windows con \_ las opciones de NSPROTO IPX**</dt> <dd> <dl> <dt> 

| Opción                      | Windows Vista y versiones posteriores | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/me |
|-----------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| \_Dirección IPX                |                         | x                   | x          | x            | x           | x             |
| \_notificación de dirección IPX \_        |                         | x                   | x          | x            | x           | x             |
| \_DSTYPE IPX                 |                         | x                   | x          | x            | x           | x             |
| \_dirección extendida de IPX \_      |                         | x                   | x          | x            | x           | x             |
| \_FILTERPTYPE IPX            |                         | x                   | x          | x            | x           | x             |
| \_GETNETINFO IPX             |                         | x                   | x          | x            | x           | x             |
| \_NORIP GETNETINFO \_ IPX      |                         | x                   | x          | x            | x           | x             |
| \_IMMEDIATESPXACK IPX        |                         | x                   | x          | x            | x           | x             |
| \_número máximo de \_ adaptadores \_ de IPX      |                         | x                   | x          | x            | x           | x             |
| tamaño máximo de IPX \_                |                         | x                   | x          | x            | x           | x             |
| \_PTYPE IPX                  |                         | x                   | x          | x            | x           | x             |
| \_difusión de recepción de IPX \_     |                         | x                   | x          | x            | x           | x             |
| \_RECVHDR IPX                |                         | x                   | x          | x            | x           | x             |
| \_RERIPNETNUMBER IPX         |                         | x                   | x          | x            | x           | x             |
| \_SPXGETCONNECTIONSTATUS IPX |                         | x                   | x          | x            | x           | x             |
| \_STOPFILTERPTYPE IPX        |                         | x                   | x          | x            | x           | x             |



 


</dt> </dl> </dd> </dl>

Las siguientes opciones de socket **\_ IPX de NSPROTO** se definieron en Windows sockets 2 Protocol-Specific el anexo, pero el protocolo IPX/SPX de Windows no las implementa.

*nivel* **=** de **NSPROTO \_ IPX**



| Opción           | Tipo | Valor predeterminado                         | Significado                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| suma de comprobación de IPX \_    | Bool | apagado                             | Cuando se establece, IPX realiza una suma de comprobación en los paquetes salientes y comprueba la suma de comprobación de los paquetes entrantes.                                                          |
| \_TXPKTSIZE IPX   | int  | Tamaño del medio en un máximo de 1466 | Establece el tamaño máximo del datagrama de envío. Este tamaño no incluye el encabezado IPX ni los encabezados de medios que se puedan usar también. Puede aumentarse hasta el tamaño del medio.    |
| \_RXPKTSIZE IPX   | int  | Tamaño del medio en un máximo de 1466 | Establece el tamaño máximo del datagrama de recepción. Este tamaño no incluye el encabezado IPX ni los encabezados de medios que se puedan usar también. Puede aumentarse hasta el tamaño del medio. |
| \_TXMEDIASIZE IPX | int  | Panel principal                   | Devuelve el tamaño del medio de envío que establece un límite superior para el tamaño del datagrama.                                                                                       |
| \_RXMEDIASIZE IPX | int  | Panel principal                   | Devuelve el tamaño del medio de recepción que establece un límite superior para el tamaño del datagrama.                                                                                    |
| IPX \_ principal     | Bool | Principal                         | Restringe el tráfico a la placa de red principal.                                                                                                               |



 

Las siguientes opciones de socket **NSPROTO \_ SPX** se definieron en Windows sockets 2 Protocol-Specific Annex, pero el protocolo IPX/SPX de Windows no las implementa en Windows.

*nivel* **=** de **NSPROTO \_ SPX**



| Opción           | Tipo | Valor predeterminado                         | Significado                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_suma de comprobación SPX    | Bool | apagado                             | Cuando se establece, IPX realiza una suma de comprobación en los paquetes salientes y comprueba la suma de comprobación de los paquetes entrantes. No se admite en todas las plataformas.                          |
| \_TXPKTSIZE SPX   | int  | Tamaño del medio en un máximo de 1466 | Establece el tamaño máximo del datagrama de envío. Este tamaño no incluye el encabezado SPX ni los encabezados de medios que se puedan usar también. Puede aumentarse hasta el tamaño del medio.    |
| \_RXPKTSIZE SPX   | int  | Tamaño del medio en un máximo de 1466 | Establece el tamaño máximo del datagrama de recepción. Este tamaño no incluye el encabezado SPX ni los encabezados de medios que se puedan usar también. Puede aumentarse hasta el tamaño del medio. |
| \_TXMEDIASIZE SPX | int  | Panel principal                   | Devuelve el tamaño del medio de envío menos los encabezados SPX y medio. Esto establece un límite superior para el tamaño de paquete de segmentación de mensajes.                                       |
| \_RXMEDIASIZE SPX | int  | Panel principal                   | Devuelve el tamaño de los medios de recepción menos los encabezados SPX y multimedia. Esto establece un límite superior para el tamaño de paquete de recepción.                                                 |
| \_RAWSPX SPX      | Bool | apagado                             | Cuando se establece, el encabezado del protocolo IPX/SPX se pasa con los datos.                                                                                                |



 

## <a name="remarks"></a>Observaciones

Las opciones de socket **\_ IPX NSPROTO** y las estructuras utilizadas por estas opciones de socket se definen en el archivo de encabezado *Wsnwlink. h* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wsnwlink. h</dt> </dl> |



 

 




