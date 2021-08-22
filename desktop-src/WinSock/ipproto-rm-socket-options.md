---
description: En la tabla siguiente se describen las opciones de socket IPPROTO RM que se aplican a los sockets creados para la familia de direcciones IPv4 (AF INET) con el parámetro de protocolo para la función de socket especificada como multidifusión confiable \_ \_ (IPPROTO \_ RM).
ms.assetid: cb99960e-428b-4ef1-a6a5-e4bdb497c771
title: IPPROTO_RM sockets (Wsrm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1710b1135d2c645f5ff55de12b2feb2d62cfbe2b257e3f28367a66a81d5171
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051493"
---
# <a name="ipproto_rm-socket-options"></a>Opciones de socket de IPPROTO \_ RM

En la tabla siguiente se describen las opciones de socket **IPPROTO \_ RM** que se aplican a los sockets creados para la familia de direcciones IPv4 (AF INET) con el parámetro de protocolo para la función de socket especificada como multidifusión confiable \_ (IPPROTO  [](/windows/desktop/api/Winsock2/nf-winsock2-socket) \_ RM). Consulte las [**páginas de referencia de función getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obtener más información sobre cómo obtener y establecer las opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas para cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

**Windows XP:** No se admite la programación de multidifusión confiable (PGM).

Algunas opciones de socket requieren más explicación de la que pueden transmitir estas tablas. estas opciones contienen vínculos a páginas adicionales.

<dl> <dt><span id="IPPROTO_RM__Socket_Options"></span><span id="ipproto_rm__socket_options"></span><span id="IPPROTO_RM__SOCKET_OPTIONS"></span>**Opciones de socket de IPPROTO \_ RM**</dt> <dd> <dl> <dt> 

| Opción                              | Obtener | Set | Tipo optval                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------|-----|-----|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RM \_ ADD \_ RECEIVE \_ IF                |     | Sí | ULONG                                            | Solo receptor. Agrega una interfaz en la que se va a escuchar (el valor predeterminado es la primera interfaz local enumerada). El parámetro optval especifica la interfaz de red en orden de bytes de red que se debe agregar. El valor especificado reemplaza la interfaz predeterminada en la primera llamada para un socket determinado y agrega otras interfaces en llamadas posteriores. Para obtener el comportamiento INADDR \_ ANY, cada interfaz de red debe agregarse por separado. |
| RM \_ DEL \_ RECEIVE \_ IF                |     | Sí | ULONG                                            | Solo receptor. Quita una interfaz agregada mediante RM \_ ADD \_ RECEIVE \_ IF. El parámetro optval especifica la interfaz de red en orden de bytes de red que se debe eliminar.                                                                                                                                                                                                                                                            |
| RM \_ FLUSHCACHE                      |     | sí | N/D                                              | Sin implementar.                                                                                                                                                                                                                                                                                                                                                                                                       |
| RM \_ HIGH \_ SPEED \_ INTRANET \_ OPT      | Sí | Sí | ULONG                                            | Solo receptor. Especifica si se usa una conexión LAN de ancho de banda alto (100 Mbps+).                                                                                                                                                                                                                                                                                                                                   |
| RM \_ LATEJOIN                        | Sí | Sí | ULONG                                            | Solo remitente. Porcentaje de tamaño de ventana que pueden solicitar los receptores de unión tardía tras la aceptación de la sesión. El valor máximo es 75 % (el valor predeterminado es cero). Deshabilite esta configuración llamando de nuevo a con el valor establecido en cero.                                                                                                                                                                                                |
| TAMAÑO DE \_ VENTANA \_ VELOCIDAD DE \_ RM              | Sí | Sí | [**VENTANA \_ DE ENVÍO DE \_ RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window)       | Solo remitente. Establece el límite de velocidad de transmisión, el tiempo de avance de la ventana y el tamaño de la ventana.                                                                                                                                                                                                                                                                                                                                   |
| ESTADÍSTICAS \_ DEL \_ RECEPTOR DE RM            | Sí |     | [**ESTADÍSTICAS \_ DEL RECEPTOR \_ DE RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_receiver_stats) | Solo receptor. Recupera las estadísticas de la sesión receptora.                                                                                                                                                                                                                                                                                                                                                         |
| VELOCIDAD \_ DE \_ ADV DE VENTANA DE ENVÍO DE \_ \_ RM         | Sí | Sí | ULONG                                            | Solo remitente. Especifica la tasa de avance incremental para la ventana de envío perimetral final (el valor predeterminado es el 15 %). El valor máximo es del 50 %.                                                                                                                                                                                                                                                                                          |
| ESTADÍSTICAS \_ DE \_ REMITENTE DE RM              | Sí |     | [**ESTADÍSTICAS \_ DE REMITENTE \_ DE RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_sender_stats)     | Solo remitente. Recupera las estadísticas de la sesión de envío.                                                                                                                                                                                                                                                                                                                                                             |
| MÉTODO RM \_ SENDER \_ WINDOW \_ \_ ADVANCE | Sí | Sí | ULONG                                            | Solo remitente. El parámetro optval especifica el método usado al avanzar la ventana de envío del borde final. El parámetro optval solo puede ser E \_ WINDOW ADVANCE BY TIME \_ \_ \_ (valor predeterminado). Tenga en cuenta que no \_ se admite E WINDOW USE AS DATA \_ \_ \_ \_ CACHE.                                                                                                                                                                     |
| RM \_ SET \_ MCAST \_ TTL                 |     | Sí | ULONG                                            | Solo remitente. Establece el valor de período de vida máximo (TTL) para los paquetes de multidifusión. El valor máximo y predeterminado es 255.                                                                                                                                                                                                                                                                                                      |
| RM \_ SET \_ MESSAGE \_ BOUNDARY          |     | Sí | ULONG                                            | Solo remitente. Especifica el tamaño del siguiente mensaje que se va a enviar, en bytes. Solo significativo para los sockets de modo de mensaje (SOCK \_ RDM). Se puede establecer mientras la sesión está en curso.                                                                                                                                                                                                                                                |
| RM \_ SET \_ SEND \_ IF                   | Sí | Sí | ULONG                                            | Solo remitente. Establece la dirección IP de la interfaz de envío en orden de bytes de red.                                                                                                                                                                                                                                                                                                                                              |
| RM \_ USE \_ FEC                        | Sí | Sí | [**RM \_ FEC \_ INFO**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info)             | Solo remitente. Notifica al remitente que aplique técnicas de corrección de errores de reenvío para enviar datos de reparación. FEC tiene tres modos: solo paquetes de paridad pro-activo, solo paquetes de paridad OnDemand o ambos. Consulte [**Rm \_ FEC INFO structure \_ (Estructura de RM FEC INFO)**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info) para obtener más información.                                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_IPPROTO_RM_options"></span><span id="windows_support_for_ipproto_rm_options"></span><span id="WINDOWS_SUPPORT_FOR_IPPROTO_RM_OPTIONS"></span>**Windows Compatibilidad con las opciones de IPPROTO \_ RM**</dt> <dd> <dl> <dt> 

| Opción                              | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-------------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|-------------|---------------|
| RM \_ ADD \_ RECEIVE \_ IF                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ DEL \_ RECEIVE \_ IF                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ FLUSHCACHE                      | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ HIGH \_ SPEED \_ INTRANET \_ OPT      | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ LATEJOIN                        | x         | x                   | x             | x                   | x          |              |             |               |
| TAMAÑO DE \_ VENTANA DE VELOCIDAD DE \_ \_ RM              | x         | x                   | x             | x                   | x          |              |             |               |
| ESTADÍSTICAS \_ DEL \_ RECEPTOR DE RM            | x         | x                   | x             | x                   | x          |              |             |               |
| VELOCIDAD \_ DE \_ ADV DE LA VENTANA DE ENVÍO \_ DE \_ RM         | x         | x                   | x             | x                   | x          |              |             |               |
| ESTADÍSTICAS \_ DEL \_ REMITENTE DE RM              | x         | x                   | x             | x                   | x          |              |             |               |
| MÉTODO RM \_ SENDER \_ WINDOW \_ \_ ADVANCE | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SET \_ MCAST \_ TTL                 | x         | x                   | x             | x                   | x          |              |             |               |
| LÍMITE DE MENSAJES DE RM \_ SET \_ \_          | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SET \_ SEND \_ IF                   | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ USE \_ FEC                        | x         | x                   | x             | x                   | x          |              |             |               |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Las **opciones de socket \_ IPPROTO RM** y las estructuras usadas por estas opciones de socket se definen en el archivo de encabezado *Wsrm.h.*

La **constante IPPROTO \_ RM** o **IPPROTO \_ PGM** se puede usar para especificar el parámetro *protocol* en la función [**de socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) para usar las opciones de socket rm. En el Kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la constante **\_ IPPROTO PGM** se define en el archivo de encabezado *Ws2def.h* en el mismo valor que la constante **IPPROTO \_ RM** definida en el archivo de encabezado *Wsrm.h.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wsrm.h</dt> </dl> |



 

 




