---
description: En la tabla siguiente se describen \_ las opciones de socket IRLMP de sol que se aplican a los sockets creados para la familia de direcciones de la Asociación de datos de infrarrojos (IrDA) \_ y el protocolo de administración de vínculos de infrarrojos (IRLMP).
ms.assetid: 0457159d-8509-435c-8f57-752530d5df65
title: Opciones de SOL_IRLMP socket (AF \_ IrDA. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090193aec00eaebd87494afefbafc7b1450fdb44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718944"
---
# <a name="sol_irlmp-socket-options"></a>Opciones de socket de SOL \_ IRLMP

En la tabla siguiente se describen las opciones de socket **\_ IRLMP de sol** que se aplican a los sockets creados para la familia de direcciones de la Asociación de datos de infrarrojos (IrDA) \_ y el protocolo de administración de vínculos de infrarrojos (IRLMP). Consulte las páginas de referencia de [**la función**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y el valor de My para obtener más información sobre cómo obtener y establecer las opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas de cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="SOL_IRLMP_Socket_Options"></span><span id="sol_irlmp_socket_options"></span><span id="SOL_IRLMP_SOCKET_OPTIONS"></span>**Opciones de socket de SOL \_ IRLMP**</dt> <dd> <dl> <dt> 

| Opción                 | Obtener | Set | Tipo Optval     | Descripción                                                            |
|------------------------|-----|-----|-----------------|------------------------------------------------------------------------|
| \_modo de detección de IRLMP \_ |     |     |                 |                                                                        |
| IRLMP \_ ENUMDEVICES     | sí |     | **DEVICELIST**  | Devuelve una lista de identificadores de dispositivo IrDA para dispositivos compatibles con IR dentro del intervalo. |
| IRLMP \_ \_ modo exclusivo |     |     | DWORD (booleano) | Establece socket para omitir el nivel TinyTP para comunicarse directamente con IrLMP. |
| consulta de IRLMP \_ IAS \_      | sí |     | **\_consulta IAS**  | Consulta IAS en un servicio y un nombre de clase determinados para sus atributos.      |
| IRLMP \_ conjunto de IAS \_        |     | sí | **conjunto de IAS \_**    | Establece un valor de atributo para un nombre de clase y un atributo determinados en IAS. |
| \_modo IRLPT de IRLMP \_     |     | sí | DWORD (booleano) | Habilita la comunicación con impresoras compatibles con IR.                        |
| parámetros de IRLMP \_      |     |     |                 |                                                                        |
| longitud de la PDU de envío de IRLMP \_ \_ \_  | sí |     | DWORD           | Recupera la longitud máxima de PDU necesaria para usar el \_ modo 9WIRE de IRLMP \_ .   |
| \_modo sostenido de IRLMP \_     |     | sí |                 |                                                                        |
| \_modo TINYTP de IRLMP \_    |     | sí |                 |                                                                        |
| \_Modo 9WIRE de IRLMP \_     | sí | sí | DWORD (booleano) | Coloca el socket IrDA en modo IrCOMM.                                 |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_IRLMP_options"></span><span id="windows_support_for_sol_irlmp_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_IRLMP_OPTIONS"></span>**Compatibilidad de Windows con \_ las opciones de sol IRLMP**</dt> <dd> <dl> <dt> 

| Opción                            | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows me, Windows 98 | Windows NT 4.0 |
|-----------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|------------------------|----------------|
| \_modo de detección de IRLMP \_<br/> |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ ENUMDEVICES<br/>     | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ \_ modo exclusivo<br/> |           |                     |               |                     |            |              |                        |                |
| consulta de IRLMP \_ IAS \_<br/>      | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ conjunto de IAS \_<br/>        | x         | x                   | x             | x                   | x          | x            | x                      |                |
| \_modo IRLPT de IRLMP \_<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |
| parámetros de IRLMP \_<br/>      |           |                     |               |                     |            |              | x                      |                |
| longitud de la PDU de envío de IRLMP \_ \_ \_<br/>  | x         | x                   | x             | x                   | x          | x            |                        |                |
| \_modo sostenido de IRLMP \_<br/>     |           |                     |               |                     |            |              |                        |                |
| \_modo TINYTP de IRLMP \_<br/>    |           |                     |               |                     |            |              | x                      |                |
| \_Modo 9WIRE de IRLMP \_<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Las opciones de socket de **sol \_ IRLMP** y las estructuras utilizadas por estas opciones de socket se definen en el archivo de encabezado de registro *\_ IrDA. h* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>AF \_ IrDA. h</dt> </dl> |



 

 




