---
description: En la tabla siguiente se describen \_ las opciones de socket de RM de IPPROTO que se aplican a los sockets creados para la familia de direcciones IPv4 (AF \_ inet) con el parámetro Protocol a la función socket especificada como multidifusión confiable (IPPROTO \_ RM).
ms.assetid: cb99960e-428b-4ef1-a6a5-e4bdb497c771
title: Opciones de IPPROTO_RM socket (WSRM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2144efec9b0a92c1da3f612e707bcb44366a38c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708776"
---
# <a name="ipproto_rm-socket-options"></a>Opciones de socket de RM de IPPROTO \_

En la tabla siguiente se describen las opciones de socket de **\_ RM de IPPROTO** que se aplican a los sockets creados para la familia de direcciones IPv4 (AF \_ inet) con el parámetro *Protocol* a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) especificada como multidifusión confiable (IPPROTO \_ RM). Consulte las páginas de referencia de [**la función**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y el valor de My para obtener más información sobre cómo obtener y establecer las opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas de cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

**Windows XP:** No se admite la programación multidifusión confiable (PGM).

Algunas opciones de socket requieren más explicación de lo que pueden transmitir estas tablas; Estas opciones contienen vínculos a páginas adicionales.

<dl> <dt><span id="IPPROTO_RM__Socket_Options"></span><span id="ipproto_rm__socket_options"></span><span id="IPPROTO_RM__SOCKET_OPTIONS"></span>**Opciones de socket de RM de IPPROTO \_**</dt> <dd> <dl> <dt> 

| Opción                              | Obtener | Set | Tipo Optval                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------|-----|-----|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Agregar recepción de RM \_ \_ si                |     | sí | ULONG                                            | Solo receptor. Agrega una interfaz en la que se va a escuchar (el valor predeterminado es la primera interfaz local enumerada). El parámetro optval especifica la interfaz de red en el orden de bytes de red que se va a agregar. El valor especificado reemplaza la interfaz predeterminada en la primera llamada para un socket determinado y agrega otras interfaces en las llamadas subsiguientes. Para obtener el comportamiento de la indirección \_ , cada interfaz de red se debe agregar por separado. |
| RM \_ del \_ receptor \_ si                |     | sí | ULONG                                            | Solo receptor. Quita una interfaz agregada mediante la adición de la recepción de RM \_ \_ \_ si. El parámetro optval especifica la interfaz de red en el orden de bytes de red que se va a eliminar.                                                                                                                                                                                                                                                            |
| RM \_ FLUSHCACHE                      |     | sí | N/D                                              | Sin implementar.                                                                                                                                                                                                                                                                                                                                                                                                       |
| RM de \_ alta velocidad de la \_ \_ intranet \_ OPC      | sí | sí | ULONG                                            | Solo receptor. Especifica si se usa una conexión LAN de ancho de banda alto (100 Mbps +).                                                                                                                                                                                                                                                                                                                                   |
| RM \_ LATEJOIN                        | sí | sí | ULONG                                            | Solo remitente. Porcentaje de tamaño de ventana que se permite solicitar a los receptores que se unen en tiempo de ejecución al aceptar la sesión. El valor máximo es 75% (el valor predeterminado es cero). Deshabilite esta configuración mediante una llamada de nuevo con el valor establecido en cero.                                                                                                                                                                                                |
| tamaño de la ventana de tasa de RM \_ \_ \_              | sí | sí | [**\_ventana de envío de RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window)       | Solo remitente. Establece el límite de velocidad de transmisión, el tiempo de avance de la ventana y el tamaño de la ventana.                                                                                                                                                                                                                                                                                                                                   |
| \_estadísticas del receptor de RM \_            | sí |     | [**\_estadísticas del receptor de RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_receiver_stats) | Solo receptor. Recupera estadísticas de la sesión receptora.                                                                                                                                                                                                                                                                                                                                                         |
| tasa de ADV. de \_ ventana de envío de RM \_ \_ \_         | sí | sí | ULONG                                            | Solo remitente. Especifica la tasa de avance incremental para la ventana de envío perimetral final (el valor predeterminado es 15%). El valor máximo es 50%.                                                                                                                                                                                                                                                                                          |
| Estadísticas del remitente de RM \_ \_              | sí |     | [**Estadísticas del remitente de RM \_ \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_sender_stats)     | Solo remitente. Recupera estadísticas de la sesión de envío.                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ \_ método avanzado de la ventana del remitente de RM \_ | sí | sí | ULONG                                            | Solo remitente. El parámetro optval especifica el método que se usa al avanzar la ventana de envío del borde final. El parámetro optval solo puede ser la \_ ventana E \_ avanzar \_ por \_ tiempo (el valor predeterminado). Tenga en cuenta \_ que \_ \_ no se admite la utilización de la ventana en la \_ \_ memoria caché de datos.                                                                                                                                                                     |
| RM \_ set \_ MCAST \_ TTL                 |     | sí | ULONG                                            | Solo remitente. Establece el valor de período de vida máximo (TTL) para los paquetes de multidifusión. El valor máximo y el predeterminado es 255.                                                                                                                                                                                                                                                                                                      |
| \_límite de \_ mensajes de conjunto de RM \_          |     | sí | ULONG                                            | Solo remitente. Especifica el tamaño del siguiente mensaje que se va a enviar, en bytes. Solo significativo para Sockets de modo de mensaje (SOCK \_ RDM). Se puede establecer mientras la sesión está en curso.                                                                                                                                                                                                                                                |
| RM \_ establecer \_ envío \_ si                   | sí | sí | ULONG                                            | Solo remitente. Establece la dirección IP de la interfaz de envío en el orden de bytes de la red.                                                                                                                                                                                                                                                                                                                                              |
| RM \_ usar \_ FEC                        | sí | sí | [**\_información de FEC de RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info)             | Solo remitente. Notifica al remitente que aplique técnicas de corrección de errores de reenvío para enviar datos de reparación. FEC tiene tres modos: paquetes de paridad Pro-Active solo, paquetes de paridad OnDemand solamente o ambos. Para obtener más información, consulte la estructura de [**\_ \_ información de FEC de RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info) .                                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_IPPROTO_RM_options"></span><span id="windows_support_for_ipproto_rm_options"></span><span id="WINDOWS_SUPPORT_FOR_IPPROTO_RM_OPTIONS"></span>**Compatibilidad de Windows con \_ las opciones de IPPROTO RM**</dt> <dd> <dl> <dt> 

| Opción                              | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/me |
|-------------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|-------------|---------------|
| \_Agregar recepción de RM \_ \_ si                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ del \_ receptor \_ si                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ FLUSHCACHE                      | x         | x                   | x             | x                   | x          |              |             |               |
| RM de \_ alta velocidad de la \_ \_ intranet \_ OPC      | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ LATEJOIN                        | x         | x                   | x             | x                   | x          |              |             |               |
| tamaño de la ventana de tasa de RM \_ \_ \_              | x         | x                   | x             | x                   | x          |              |             |               |
| \_estadísticas del receptor de RM \_            | x         | x                   | x             | x                   | x          |              |             |               |
| tasa de ADV. de \_ ventana de envío de RM \_ \_ \_         | x         | x                   | x             | x                   | x          |              |             |               |
| Estadísticas del remitente de RM \_ \_              | x         | x                   | x             | x                   | x          |              |             |               |
| \_ \_ \_ método avanzado de la ventana del remitente de RM \_ | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ set \_ MCAST \_ TTL                 | x         | x                   | x             | x                   | x          |              |             |               |
| \_límite de \_ mensajes de conjunto de RM \_          | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ establecer \_ envío \_ si                   | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ usar \_ FEC                        | x         | x                   | x             | x                   | x          |              |             |               |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Las opciones de socket de **\_ RM de IPPROTO** y las estructuras utilizadas por estas opciones de socket se definen en el archivo de encabezado *WSRM. h* .

La **IPPROTO \_ RM** o la **constante \_ PGM de IPPROTO** se pueden usar para especificar el parámetro de *Protocolo* en la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) para usar las opciones de socket de RM. En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la constante **IPPROTO \_ PGM** se define en el archivo de encabezado *Ws2def. h* en el mismo valor que la constante **IPPROTO \_ RM** definida en el archivo de encabezado *WSRM. h* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WSRM. h</dt> </dl> |



 

 




