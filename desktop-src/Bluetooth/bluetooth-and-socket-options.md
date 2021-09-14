---
title: Bluetooth y opciones de socket
description: Bluetooth para Windows admite las siguientes opciones de socket.
ms.assetid: e2e305c2-e749-4566-8e24-c07a7a29c612
keywords:
- Bluetooth y opciones de socket Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84040a98c3dae1fec292e4f0a7086f11d1ee546c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172098"
---
# <a name="bluetooth-and-socket-options"></a>Bluetooth y opciones de socket

Bluetooth para Windows admite las siguientes opciones de socket. Las opciones de socket se establecen y consultan mediante las [**funciones setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) y [**getsockopt,**](/windows/desktop/api/winsock/nf-winsock-getsockopt) respectivamente. Todas las opciones siguientes se pueden usar con la función **setsockopt,** pero solo la opción **\_ so BTH \_ MTU** está disponible para su uso con la **función getsockopt.**

La siguiente configuración es necesaria para trabajar con Bluetooth de socket:

-   El *parámetro s* debe ser un Bluetooth socket.
-   El *parámetro level* debe ser SOL **\_ RFCOMM.**

## <a name="so_bth_authenticate"></a>AUTENTICACIÓN \_ DE BTH \_

En el caso de los sockets desconectados, SO [](/windows/desktop/api/winsock2/nf-winsock2-connect) **\_ BTH \_ AUTHENTICATE** especifica que se requiere autenticación para que una operación de conexión o aceptación se complete correctamente. [](/windows/desktop/api/winsock2/nf-winsock2-accept) Al establecer esta opción de socket se inicia activamente la autenticación durante el establecimiento de la conexión, si los dos dispositivos Bluetooth no se autenticaron previamente. El sistema operativo proporciona la interfaz de usuario para el intercambio de claves de paso, si es necesario, fuera del contexto de la aplicación.

En el caso de [](/windows/desktop/api/winsock2/nf-winsock2-connect) las conexiones salientes que requieren autenticación, se produce un error en la operación de conexión **con WSAEACCES** si la autenticación no se realiza correctamente. En respuesta, la aplicación puede pedir al usuario que autentique los dos dispositivos Bluetooth antes de la conexión.

Para las conexiones entrantes, la conexión se rechaza si no se puede establecer la autenticación y devuelve un error **WSAEHOSTDOWN.** Para obtener más información sobre la autenticación Bluetooth dispositivos, vea [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Para la opción de socket **SO \_ BTH \_ AUTHENTICATE,** *optval* es un puntero a ULONG bAuthenticate y debe ser **TRUE**; *optlen* es equivalente a "sizeof(ULONG)".

**Windows XP con SP2: SO \_ BTH \_ AUTHENTICATE inicia** la autenticación para los sockets conectados y fuerza la autenticación tras la conexión para los sockets no conectados. Para las conexiones entrantes, la conexión se rechaza si no se puede realizar la autenticación.

## <a name="so_bth_encrypt"></a>SO \_ BTH \_ ENCRYPT

En los sockets no conectados, la opción de socket **\_ SO BTH \_ ENCRYPT** aplica el cifrado para establecer una conexión. El cifrado solo está disponible para las conexiones autenticadas. En el caso de las conexiones entrantes, se rechaza automáticamente una conexión para la que no se puede establecer el cifrado y se devuelve **WSAEHOSTDOWN** como error. Para las conexiones salientes, [**se**](/windows/desktop/api/winsock2/nf-winsock2-connect) produce un error en la **función de conexión con WSAEACCES si** no se puede establecer el cifrado. En respuesta, la aplicación puede pedir al usuario que autentique los dos dispositivos Bluetooth antes de la conexión. Para obtener más información sobre la autenticación Bluetooth dispositivos, vea [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Para la opción de socket SO \_ BTH \_ ENCRYPT, *optval* es un puntero a ULONG **bEncrypt** y debe ser **TRUE**; *optlen* es equivalente a sizeof(ULONG).

**Windows XP con SP2:** Para un socket que está conectado y autenticado, **SO \_ BTH \_ ENCRYPT inicia** el cifrado.

## <a name="so_bth_mtu"></a>SO \_ BTH \_ MTU

La **opción de socket de \_ \_ MTU so BTH** es una opción avanzada que se usa principalmente para la validación. La **opción \_ SO BTH \_ MTU** obtiene o establece la MTU de RFCOMM predeterminada (unidad de transmisión máxima) para la negociación de la conexión en un valor diferente del valor predeterminado del protocolo RFCOMM.

Dado que la MTU de RFCOMM se ve afectada por la MTU L2CAP subyacente y los valores mínimos y máximos de protocolo y aplicación, el valor predeterminado de **\_ \_ MTU** de SO BTH es solo un punto de partida para la negociación con el par remoto y es probable que la MTU negociada final varíe del valor predeterminado. Establecer el **valor \_ de \_ MTU de SO BTH** puede afectar negativamente al rendimiento y, como tal, cualquier modificación debe realizarse con conocimiento del protocolo Bluetooth subyacente.

La **opción de socket so \_ BTH \_ MTU** se puede realizar en sockets conectados, pero no tiene ningún efecto si la negociación ya se ha completado. Establecerlo en el socket de escucha (servidor) no tiene ningún efecto.

La cantidad de datos que una aplicación puede enviar o recibir en una sola llamada de socket no se ve afectada por la MTU; La MTU solo afecta a la forma en que el proveedor Windows sockets subyacente segmenta los paquetes para el transporte. Tanto la MTU propuesta como la MTU negociada en última instancia deben estar entre **\_ \_ MTU MIN** de RFCOMM y **\_ \_ MTU MAX de RFCOMM,** tal como se define en el archivo de encabezado Ws2bth.h.

Para la opción de socket **\_ so BTH \_ MTU,** *optval* es un puntero a ULONG mtu; *optlen* es equivalente a "sizeof(ULONG)".

## <a name="so_bth_mtu_max"></a>SO \_ BTH \_ MTU \_ MAX

La **opción de socket SO \_ BTH \_ MTU \_ MAX** es una opción avanzada que se usa principalmente para la validación. La opción de socket **SO \_ BTH \_ MTU \_ MAX** establece la MTU máxima de RFCOMM (unidad de transmisión máxima) para la negociación de la conexión. Las conexiones con una MTU de RFCOMM igual o mayor que este valor producirán un error durante el proceso [**de**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**aceptación de**](/windows/desktop/api/winsock2/nf-winsock2-accept) la conexión. Aunque se permite establecer esta opción de socket para un socket conectado, no tiene ningún efecto si se ha completado la negociación. Al establecer esta opción de socket en un socket de escucha, se propaga el valor de todas las conexiones entrantes. El valor de MTU MAX debe estar entre **\_ \_ MTU MIN** de RFCOMM y **\_ \_ MTU** MAX de RFCOMM, tal y como se define en el archivo de encabezado Ws2bth.h.

Para la opción de socket **\_ SO BTH \_ MTU \_ MAX,** *optval* es un puntero a ULONG max \_ mtu; *optlen* es equivalente a "sizeof(ULONG)".

## <a name="so_bth_mtu_min"></a>ASÍ \_ QUE BTH \_ MTU \_ MIN

La **opción de socket SO \_ BTH \_ MTU \_ MIN** es una opción avanzada que se usa principalmente para la validación. La opción de socket MIN de **\_ \_ MTU \_ de SO BTH** establece la MTU mínima de RFCOMM (unidad de transmisión máxima) para la negociación de la conexión. Las conexiones con una MTU RFCOMM menor que este valor producirán un error durante el [**proceso de**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**aceptación de**](/windows/desktop/api/winsock2/nf-winsock2-accept) la conexión. Aunque se permite establecer esta opción de socket para un socket conectado, no tiene ningún efecto si se ha completado la negociación. Al establecer esta opción de socket en un socket de escucha, se propaga el valor de todas las conexiones entrantes.

Solo un socket de escucha puede revisar la MTU hacia abajo, por lo tanto, si el valor propuesto por el socket de conexión es menor que el valor establecido para **SO \_ BTH \_ MTU \_ MIN** en el socket de escucha, se rechaza la conexión. La MTU mínima debe estar entre **\_ \_ MTU MIN** de RFCOMM y **\_ \_ MTU** MAX de RFCOMM, tal como se define en el archivo de encabezado Ws2bth.h.

Para la opción de \_ socket SO BTH \_ MTU \_ MIN, *optval* es un puntero a ULONG min \_ mtu; *optlen* es equivalente a "sizeof(ULONG)".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)
</dt> <dt>

[**Conectar**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**Aceptar**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 