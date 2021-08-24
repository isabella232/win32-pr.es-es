---
description: En la tabla siguiente se describen las opciones de socket IRLMP de SOL que se aplican a los sockets creados para la familia de direcciones de Protocolo de asociación de datos por infrarrojos (IrDA) (IrDA) (AF IRDA) y el Protocolo de administración de \_ vínculos \_ InfraRed (IRLMP).
ms.assetid: 0457159d-8509-435c-8f57-752530d5df65
title: SOL_IRLMP sockets (Af \_ irda.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2be68bc658cd7d55ff72a77b6ec87568c37d6d786d0a5e654e9276378b837c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860735"
---
# <a name="sol_irlmp-socket-options"></a>Opciones \_ de socket IRLMP de SOL

En la tabla siguiente se describen las opciones de socket **\_ IRLMP** de SOL que se aplican a los sockets creados para la familia de direcciones de Protocolo de asociación de datos por infrarrojos (IrDA) (IrDA) (AF IRDA) y el Protocolo de administración de vínculos \_ InfraRed (IRLMP). Consulte las [**páginas de referencia de función getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obtener más información sobre cómo obtener y establecer las opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas para cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

<dl> <dt><span id="SOL_IRLMP_Socket_Options"></span><span id="sol_irlmp_socket_options"></span><span id="SOL_IRLMP_SOCKET_OPTIONS"></span>**Opciones \_ de socket IRLMP de SOL**</dt> <dd> <dl> <dt> 

| Opción                 | Obtener | Set | Tipo optval     | Descripción                                                            |
|------------------------|-----|-----|-----------------|------------------------------------------------------------------------|
| MODO DE DETECCIÓN \_ DE IRLMP \_ |     |     |                 |                                                                        |
| IRLMP \_ ENUMDEVICES     | Sí |     | **DEVICELIST**  | Devuelve una lista de los IDs de dispositivo IrDA para dispositivos compatibles con IR dentro del intervalo. |
| MODO EXCLUSIVO \_ DE IRLMP \_ |     |     | DWORD (booleano) | Establece socket para omitir la capa tinyTP para comunicarse directamente con IrLMP. |
| IRLMP \_ IAS \_ QUERY      | Sí |     | **CONSULTA \_ de IAS**  | Consulta IAS en un servicio y un nombre de clase determinados para sus atributos.      |
| IRLMP \_ IAS \_ SET        |     | Sí | **IAS \_ SET**    | Establece un valor de atributo para un nombre de clase y un atributo determinados en IAS. |
| MODO \_ IRLMP \_ IRLPT     |     | Sí | DWORD (booleano) | Permite la comunicación con impresoras compatibles con IR.                        |
| PARÁMETROS \_ IRLMP      |     |     |                 |                                                                        |
| IRLMP \_ SEND \_ PDU \_ LEN  | Sí |     | DWORD           | Recupera la longitud máxima de PDU necesaria para usar IRLMP \_ 9WIRE \_ MODE.   |
| MODO IRLMP \_ SHARP \_     |     | Sí |                 |                                                                        |
| MODO \_ IRLMP \_ TINYTP    |     | Sí |                 |                                                                        |
| MODO IRLMP \_ 9WIRE \_     | Sí | Sí | DWORD (booleano) | Coloca el socket irDA en modo IrCOMM.                                 |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_IRLMP_options"></span><span id="windows_support_for_sol_irlmp_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_IRLMP_OPTIONS"></span>**Windows Compatibilidad con las opciones \_ de IRLMP de SOL**</dt> <dd> <dl> <dt> 

| Opción                            | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows Me, Windows 98 | Windows NT 4.0 |
|-----------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|------------------------|----------------|
| MODO DE DETECCIÓN \_ DE IRLMP \_<br/> |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ ENUMDEVICES<br/>     | x         | x                   | x             | x                   | x          | x            | x                      |                |
| MODO EXCLUSIVO \_ DE IRLMP \_<br/> |           |                     |               |                     |            |              |                        |                |
| IRLMP \_ IAS \_ QUERY<br/>      | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ IAS \_ SET<br/>        | x         | x                   | x             | x                   | x          | x            | x                      |                |
| MODO \_ IRLMP \_ IRLPT<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |
| PARÁMETROS \_ IRLMP<br/>      |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ SEND \_ PDU \_ LEN<br/>  | x         | x                   | x             | x                   | x          | x            |                        |                |
| MODO IRLMP \_ SHARP \_<br/>     |           |                     |               |                     |            |              |                        |                |
| MODO \_ IRLMP \_ TINYTP<br/>    |           |                     |               |                     |            |              | x                      |                |
| MODO IRLMP \_ 9WIRE \_<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Las **opciones de socket \_ IRLMP** de SOL y las estructuras usadas por estas opciones de socket se definen en el *archivo de encabezado \_ irda.h de Af.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Af \_ irda.h</dt> </dl> |



 

 




