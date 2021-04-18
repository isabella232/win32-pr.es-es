---
description: En la tabla siguiente se describen \_ las opciones de socket de AppleTalk de sol que se aplican a los sockets creados para la familia de direcciones de AppleTalk (AF \_ AppleTalk).
ms.assetid: 1a6b18e3-1fea-4ba2-8076-c38e7f679e9e
title: Opciones de SOL_APPLETALK socket (Atalkwsh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SOL_APPLETALK
- Windows
api_type:
- HeaderDef
api_location:
- Atalkwsh.h
ms.openlocfilehash: 146cfa02706cc9a2669cf21ba6d9eac0ac74ee4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718960"
---
# <a name="sol_appletalk-socket-options"></a>Opciones de socket de APPLETALK de SOL \_

En la tabla siguiente se describen las opciones de socket de **\_ AppleTalk de sol** que se aplican a los sockets creados para la familia de direcciones de AppleTalk (AF \_ AppleTalk). Consulte las páginas de referencia de [**la función**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y el valor de My para obtener más información sobre cómo obtener y establecer las opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas de cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="SOL_APPLETALK_Socket_Options"></span><span id="sol_appletalk_socket_options"></span><span id="SOL_APPLETALK_SOCKET_OPTIONS"></span>**Opciones de socket de APPLETALK de SOL \_**</dt> <dd> <dl> <dt> 

| Opción                          | Obtener | Set | Tipo Optval                          | Descripción                                                                                                                                                                                          |
|---------------------------------|-----|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_confirmar \_ nombre               | sí |     | **\_tupla NBP de WSH \_**                  | Confirma que un nombre AppleTalk determinado está enlazado a la dirección especificada.                                                                                                                                  |
| \_nombre de anulación del registro \_            |     | sí | **\_nombre de registro de WSH \_**              | Anula el registro del nombre de la red.                                                                                                                                                               |
| \_GETLOCALZONES               | sí |     | **\_zonas de búsqueda de WSH \_**               | Devuelve una lista de nombres de zona conocidos para el nombre de adaptador especificado.                                                                                                                                        |
| \_GETMYZONE                   | sí |     | Juegos \[\]                            | Devuelve la zona predeterminada en la red.                                                                                                                                                             |
| \_GETNETINFO                  | sí |     | **\_consulta WSH \_ NETDEF \_ en el \_ adaptador** | Devuelve los valores de inicialización de la red, así como la zona predeterminada. El parámetro *optlen* debe tener al menos un byte mayor que el tamaño de la **búsqueda de WSH \_ NETDEF en la estructura \_ \_ del \_ adaptador** .  |
| \_GETZONELIST                 | sí |     | **\_zonas de búsqueda de WSH \_**               | Devuelve los nombres de zona de la lista de zonas de Internet. El parámetro *optlen* debe tener al menos un byte mayor que el tamaño de la estructura de las **\_ \_ zonas de búsqueda de WSH** .                                       |
| Buscar en la \_ \_ zona              | sí |     |                                      | Igual que \_ GETMYZONE                                                                                                                                                                                |
| \_nombre de búsqueda \_                | sí |     | **\_nombre de búsqueda de WSH \_**                | Busca un nombre de NBP especificado y devuelve las tuplas coincidentes de la información de nombre y NBP. El parámetro *optlen* debe tener al menos un byte mayor que el tamaño de la estructura de nombre de búsqueda de WSH \_ \_ . |
| \_busque \_ NETDEF en \_ el \_ adaptador | sí |     | **\_consulta WSH \_ NETDEF \_ en el \_ adaptador** | Igual que \_ GETNETINFO.                                                                                                                                                                              |
| \_zonas de búsqueda \_               | sí |     | **\_zonas de búsqueda de WSH \_**               | Igual que \_ GETZONELIST.                                                                                                                                                                             |
| \_ \_ zonas de búsqueda \_ en el \_ adaptador  | sí |     | **\_zonas de búsqueda de WSH \_**               | Igual que \_ GETLOCALZONES.                                                                                                                                                                           |
| por tanto, \_ PAP \_ obtiene el \_ Estado del servidor \_    | sí |     | **Estado del servidor de WSH \_ PAP \_ Get \_ \_**    | Devuelve el estado de PAP de un servidor determinado.                                                                                                                                                           |
| \_lectura de PAP \_ Prime \_            |     | sí | Juegos \[\]                            | Esta llamada Prime una lectura en una conexión PAP para que el remitente pueda comenzar a enviar los datos.                                                                                                                 |
| \_configurar el \_ \_ Estado del servidor de PAP \_    |     | sí | Juegos \[\]                            | Establece el estado que se enviará si otro cliente solicita el estado.                                                                                                                                     |
| \_nombre de registro \_              |     | sí | **\_nombre de registro de WSH \_**              | Registra el nombre especificado en la red AppleTalk.                                                                                                                                                    |
| \_quitar \_ nombre                |     | sí | **\_nombre de registro de WSH \_**              | Igual que para \_ cancelar el registro de \_ nombre                                                                                                                                                                         |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_APPLETALK_options"></span><span id="windows_support_for_sol_appletalk_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_APPLETALK_OPTIONS"></span>**Compatibilidad con Windows para \_ las opciones de sol APPLETALK**</dt> <dd> <dl> <dt> 

| Opción                          | Windows Vista y versiones posteriores | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/me |
|---------------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| \_confirmar \_ nombre               |                         | x                   | x          | x            | x           |               |
| \_nombre de anulación del registro \_            |                         | x                   | x          | x            | x           |               |
| \_GETLOCALZONES               |                         | x                   | x          | x            | x           |               |
| \_GETMYZONE                   |                         | x                   | x          | x            | x           |               |
| \_GETNETINFO                  |                         | x                   | x          | x            | x           |               |
| \_GETZONELIST                 |                         | x                   | x          | x            | x           |               |
| Buscar en la \_ \_ zona              |                         | x                   | x          | x            | x           |               |
| \_nombre de búsqueda \_                |                         | x                   | x          | x            | x           |               |
| \_busque \_ NETDEF en \_ el \_ adaptador |                         | x                   | x          | x            | x           |               |
| \_zonas de búsqueda \_               |                         | x                   | x          | x            | x           |               |
| \_ \_ zonas de búsqueda \_ en el \_ adaptador  |                         | x                   | x          | x            | x           |               |
| por tanto, \_ PAP \_ obtiene el \_ Estado del servidor \_    |                         | x                   | x          | x            | x           |               |
| \_lectura de PAP \_ Prime \_            |                         | x                   | x          | x            | x           |               |
| \_configurar el \_ \_ Estado del servidor de PAP \_    |                         | x                   | x          | x            | x           |               |
| \_nombre de registro \_              |                         | x                   | x          | x            | x           |               |
| \_quitar \_ nombre                |                         | x                   | x          | x            | x           |               |



 

Las opciones de la versión **sol de \_ APPLETALK** solo se admiten en las versiones de servidor de Windows 2000 y Windows NT 4,0.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Las opciones de sockets de **\_ Apple de sol** y las estructuras utilizadas por estas opciones de socket se definen en el archivo de encabezado *Atalkwsh. h* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Atalkwsh. h</dt> </dl> |



 

 




