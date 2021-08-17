---
description: En la tabla siguiente se describen las opciones de socket DE APPLETALK de SOL que se aplican a los sockets creados para la familia de \_ direcciones de AppleTalk (AF \_ APPLETALK).
ms.assetid: 1a6b18e3-1fea-4ba2-8076-c38e7f679e9e
title: SOL_APPLETALK sockets (Atalkwsh.h)
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
ms.openlocfilehash: 5ea45b4007a3bd36d2cfbceda5b7ec4f2cff20d9bb2387fb2d184710a8a4492c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740012"
---
# <a name="sol_appletalk-socket-options"></a>Opciones \_ de socket de APPLETALK de SOL

En la tabla siguiente se describen las opciones de socket DE **\_ APPLETALK** de SOL que se aplican a los sockets creados para la familia de direcciones de AppleTalk (AF \_ APPLETALK). Consulte las [**páginas de referencia de función getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obtener más información sobre cómo obtener y establecer las opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas para cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

<dl> <dt><span id="SOL_APPLETALK_Socket_Options"></span><span id="sol_appletalk_socket_options"></span><span id="SOL_APPLETALK_SOCKET_OPTIONS"></span>**Opciones \_ de socket de APPLETALK de SOL**</dt> <dd> <dl> <dt> 

| Opción                          | Obtener | Set | Tipo optval                          | Descripción                                                                                                                                                                                          |
|---------------------------------|-----|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASÍ QUE \_ CONFIRME \_ EL NOMBRE.               | Sí |     | **WSH \_ NBP \_ TUPLE**                  | Confirma que un nombre de AppleTalk determinado está enlazado a la dirección dada.                                                                                                                                  |
| POR \_ LO TANTO, ANULAR EL \_ REGISTRO DEL NOMBRE            |     | Sí | **WSH \_ REGISTER \_ NAME**              | Anula el registro del nombre de la red.                                                                                                                                                               |
| SO \_ GETLOCALZONES               | Sí |     | **ZONAS DE \_ BÚSQUEDA DE \_ WSH**               | Devuelve una lista de nombres de zona conocidos por el nombre del adaptador especificado.                                                                                                                                        |
| ASÍ \_ QUE GETMYZONE                   | Sí |     | Char \[\]                            | Devuelve la zona predeterminada de la red.                                                                                                                                                             |
| ASÍ \_ QUE GETNETINFO                  | Sí |     | **WSH \_ LOOKUP \_ NETDEF \_ ON \_ ADAPTER** | Devuelve los valores de eded de la red, así como la zona predeterminada. El *parámetro optlen* debe ser al menos un byte mayor que el tamaño de la estructura **WSH LOOKUP \_ \_ NETDEF ON \_ \_ ADAPTER.**  |
| ASÍ \_ QUE GETZONELIST                 | Sí |     | **ZONAS DE \_ BÚSQUEDA DE \_ WSH**               | Devuelve los nombres de zona de la lista de zonas de Internet. El *parámetro optlen* debe ser al menos un byte mayor que el tamaño de la estructura **DE ZONAS DE BÚSQUEDA \_ \_ de WSH.**                                       |
| BÚSQUEDA \_ DE \_ MYZONE              | Sí |     |                                      | Igual que SO \_ GETMYZONE                                                                                                                                                                                |
| ASÍ QUE \_ LOOKUP \_ NAME                | Sí |     | **WSH \_ LOOKUP \_ NAME**                | Busca un nombre NBP especificado y devuelve las tuplas correspondientes de nombre e información de NBP. El *parámetro optlen* debe ser al menos un byte mayor que el tamaño de la estructura WSH \_ LOOKUP \_ NAME. |
| BÚSQUEDA \_ DE \_ NETDEF EN EL \_ \_ ADAPTADOR | Sí |     | **WSH \_ LOOKUP \_ NETDEF \_ ON \_ ADAPTER** | Igual que SO \_ GETNETINFO.                                                                                                                                                                              |
| ZONAS \_ DE \_ BÚSQUEDA               | Sí |     | **ZONAS DE \_ BÚSQUEDA DE \_ WSH**               | Igual que SO \_ GETZONELIST.                                                                                                                                                                             |
| ASÍ QUE \_ LOOKUP \_ ZONES ON \_ \_ ADAPTER  | Sí |     | **ZONAS DE \_ BÚSQUEDA DE \_ WSH**               | Igual que SO \_ GETLOCALZONES.                                                                                                                                                                           |
| ASÍ QUE \_ PAP OBTIENE EL ESTADO DEL \_ \_ \_ SERVIDOR    | Sí |     | **WSH \_ PAP \_ GET \_ SERVER \_ STATUS**    | Devuelve el estado de PAP de un servidor determinado.                                                                                                                                                           |
| ASÍ \_ QUE PAP PRIME \_ \_ READ            |     | Sí | Char \[\]                            | Esta llamada establece una lectura en una conexión PAP para que el remitente pueda empezar a enviar los datos.                                                                                                                 |
| ASÍ QUE \_ PAP ESTABLECE EL ESTADO DEL \_ \_ \_ SERVIDOR    |     | Sí | Char \[\]                            | Establece el estado que se va a enviar si otro cliente solicita el estado.                                                                                                                                     |
| ASÍ QUE \_ REGISTRAR \_ NOMBRE              |     | Sí | **WSH \_ REGISTER \_ NAME**              | Registra el nombre especificado en la red de AppleTalk.                                                                                                                                                    |
| ASÍ \_ QUE QUITE EL \_ NOMBRE.                |     | Sí | **WSH \_ REGISTER \_ NAME**              | Igual que SO \_ DEREGISTER \_ NAME                                                                                                                                                                         |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_APPLETALK_options"></span><span id="windows_support_for_sol_appletalk_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_APPLETALK_OPTIONS"></span>**Windows Compatibilidad con las \_ opciones de APPLETALK de SOL**</dt> <dd> <dl> <dt> 

| Opción                          | Windows Vista y versiones posteriores | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|---------------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| ASÍ QUE \_ CONFIRME \_ EL NOMBRE.               |                         | x                   | x          | x            | x           |               |
| POR \_ LO TANTO, ANULAR EL \_ REGISTRO DEL NOMBRE            |                         | x                   | x          | x            | x           |               |
| SO \_ GETLOCALZONES               |                         | x                   | x          | x            | x           |               |
| ASÍ \_ QUE GETMYZONE                   |                         | x                   | x          | x            | x           |               |
| ASÍ \_ QUE GETNETINFO                  |                         | x                   | x          | x            | x           |               |
| ASÍ \_ QUE GETZONELIST                 |                         | x                   | x          | x            | x           |               |
| BÚSQUEDA \_ DE \_ MYZONE              |                         | x                   | x          | x            | x           |               |
| ASÍ QUE \_ LOOKUP \_ NAME                |                         | x                   | x          | x            | x           |               |
| BÚSQUEDA \_ DE \_ NETDEF EN EL \_ \_ ADAPTADOR |                         | x                   | x          | x            | x           |               |
| ZONAS \_ DE \_ BÚSQUEDA               |                         | x                   | x          | x            | x           |               |
| ASÍ QUE \_ LOOKUP \_ ZONES ON \_ \_ ADAPTER  |                         | x                   | x          | x            | x           |               |
| ASÍ QUE \_ PAP OBTIENE EL ESTADO DEL \_ \_ \_ SERVIDOR    |                         | x                   | x          | x            | x           |               |
| ASÍ \_ QUE PAP PRIME \_ \_ READ            |                         | x                   | x          | x            | x           |               |
| ASÍ QUE \_ PAP ESTABLECE EL ESTADO DEL \_ \_ \_ SERVIDOR    |                         | x                   | x          | x            | x           |               |
| ASÍ QUE \_ REGISTRAR \_ NOMBRE              |                         | x                   | x          | x            | x           |               |
| ASÍ \_ QUE QUITE EL \_ NOMBRE.                |                         | x                   | x          | x            | x           |               |



 

Las **opciones DE SOL \_ APPLETALK** solo se admiten en las versiones de servidor de Windows 2000 y Windows NT 4.0.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Las opciones de socket DE **\_ SOL APPLETALK** y las estructuras usadas por estas opciones de socket se definen en el archivo de encabezado *Atalkwsh.h.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Atalkwsh.h</dt> </dl> |



 

 




