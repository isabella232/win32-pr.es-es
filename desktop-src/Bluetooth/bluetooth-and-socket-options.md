---
title: Opciones de Bluetooth y socket
description: Bluetooth para Windows admite las siguientes opciones de socket.
ms.assetid: e2e305c2-e749-4566-8e24-c07a7a29c612
keywords:
- Bluetooth y opciones de Socket Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84040a98c3dae1fec292e4f0a7086f11d1ee546c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995344"
---
# <a name="bluetooth-and-socket-options"></a>Opciones de Bluetooth y socket

Bluetooth para Windows admite las siguientes opciones de socket. Las opciones de socket se establecen y se consultan [**con las funciones de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) , respectivamente. Todas las opciones siguientes se pueden usar **con la función de la** función de la función, pero solo la opción de **\_ \_ MTU BTH** está disponible para su uso con la función **getsockopt** .

Se requiere la siguiente configuración para trabajar con opciones de Socket Bluetooth:

-   El parámetro *s* debe ser un Socket Bluetooth.
-   El parámetro *LEVEL* debe ser **sol \_ RFCOMM**.

## <a name="so_bth_authenticate"></a>\_BTH \_ Authenticate

En el caso de los sockets desconectados, el **\_ BTH \_ Authenticate** especifica que se requiere autenticación para que una operación de [**conexión**](/windows/desktop/api/winsock2/nf-winsock2-connect) o [**aceptación**](/windows/desktop/api/winsock2/nf-winsock2-accept) se complete correctamente. La configuración de esta opción de socket inicia activamente la autenticación durante el establecimiento de la conexión, si los dos dispositivos Bluetooth no se autenticaron previamente. La interfaz de usuario para el intercambio de claves de paso, si es necesario, la proporciona el sistema operativo fuera del contexto de la aplicación.

En el caso de las conexiones salientes que requieren autenticación, se produce un error en la operación de [**conexión**](/windows/desktop/api/winsock2/nf-winsock2-connect) con **WSAEACCES** si la autenticación no se realiza correctamente. En respuesta, la aplicación puede solicitar al usuario que autentique los dos dispositivos Bluetooth antes de la conexión.

En el caso de las conexiones entrantes, se rechaza la conexión si no se puede establecer la autenticación y se devuelve un error **WSAEHOSTDOWN** . Para obtener más información acerca de la autenticación de dispositivos Bluetooth, consulte [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

En el caso de la opción de socket **\_ BTH \_ Authenticate** , *OPTVAL* es un puntero a ulong bAuthenticate y debe ser **true**. *optlen* es equivalente a "SIZEOF (ulong)".

**Windows XP con SP2: \_ BTH \_ Authenticate** inicia la autenticación para los sockets conectados y fuerza la autenticación al conectarse a los sockets no conectados. En el caso de las conexiones entrantes, se rechaza la conexión si no se puede realizar la autenticación.

## <a name="so_bth_encrypt"></a>\_BTH \_ cifrar

En los sockets no conectados, la **opción \_ para \_ cifrar** el socket de BTH aplica el cifrado para establecer una conexión. El cifrado solo está disponible para las conexiones autenticadas. En el caso de las conexiones entrantes, se rechaza automáticamente una conexión para la que no se puede establecer el cifrado y se devuelve **WSAEHOSTDOWN** como el error. En el caso de las conexiones salientes, se produce un error en la función [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) con **WSAEACCES** si no se puede establecer el cifrado. En respuesta, la aplicación puede solicitar al usuario que autentique los dos dispositivos Bluetooth antes de la conexión. Para obtener más información acerca de la autenticación de dispositivos Bluetooth, consulte [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Para la \_ opción de BTH \_ cifrar socket, *optval* es un puntero a ulong **bEncrypt** y debe ser **true**. *optlen* es equivalente a SIZEOF (ulong).

**Windows XP con SP2:** Para un socket que está conectado y autenticado, **por lo que \_ BTH \_ Encrypt** inicia el cifrado.

## <a name="so_bth_mtu"></a>SO \_ BTH \_ MTU

La opción de socket de **\_ \_ MTU de BTH** es una opción avanzada que se usa principalmente para la validación. La opción **so \_ BTH \_ MTU** obtiene o establece la MTU de RFCOMM predeterminada (unidad de transmisión máxima) para la negociación de la conexión a un valor distinto del valor predeterminado del protocolo RFCOMM.

Dado que la MTU de RFCOMM se ve afectada por la MTU de L2CAP subyacente y los valores mínimos y máximos del protocolo y la aplicación, el valor predeterminado para la **\_ \_ MTU de BTH** es solo un punto de partida para la negociación con el elemento remoto del mismo nivel, y es probable que la MTU negociada final varíe del valor predeterminado. Establecer el valor de **\_ \_ MTU de SO BTH** puede afectar negativamente al rendimiento y, como tal, se debe realizar cualquier modificación con conocimiento del protocolo Bluetooth subyacente.

La opción de socket **\_ \_ MTU de BTH** se puede realizar en sockets conectados, pero no tiene ningún efecto si la negociación ya se ha completado. Su configuración en el socket de escucha (servidor) no tiene ningún efecto.

La cantidad de datos que una aplicación puede enviar o recibir en una sola llamada de Socket no se ve afectada por la MTU; La MTU solo afecta al modo en que el proveedor de servicios de Windows Sockets subyacente segmenta los paquetes para el transporte. Tanto la MTU propuesta como la MTU que se negocia en última instancia deben estar entre la MTU **mínima de RFCOMM \_ \_** y la MTU **máxima de RFCOMM \_ \_**, tal como se define en el archivo de encabezado Ws2bth. h.

Para la opción de socket de **\_ \_ MTU de BTH** , *optval* es un puntero a la MTU de ulong; *optlen* es equivalente a "SIZEOF (ulong)".

## <a name="so_bth_mtu_max"></a>SO \_ BTH \_ MTU \_ máx.

La opción de socket **\_ BTH \_ MTU \_ Max** es una opción avanzada que se usa principalmente para la validación. La opción de socket **\_ BTH \_ MTU \_ Max** establece la MTU máxima (unidad de transmisión máxima) de RFCOMM para la negociación de la conexión. Las conexiones con una MTU de RFCOMM igual o mayor que este valor producen un error durante el proceso de aceptación de [**conexión**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [](/windows/desktop/api/winsock2/nf-winsock2-accept) . Aunque se permite establecer esta opción de socket para un socket conectado, no tiene ningún efecto si se ha completado la negociación. Al establecer esta opción de socket en un socket de escucha, se propaga el valor de todas las conexiones entrantes. El valor de MTU máximo debe estar entre la MTU **mínima de RFCOMM \_ \_** y la **\_ \_ MTU máxima de RFCOMM**, tal como se define en el archivo de encabezado Ws2bth. h.

En el caso de la opción de socket **\_ BTH \_ MTU \_ Max** , *optval* es un puntero a la MTU Max Max \_ ; *optlen* es equivalente a "SIZEOF (ulong)".

## <a name="so_bth_mtu_min"></a>SO \_ BTH \_ MTU \_ min

La opción de socket **\_ min de \_ MTU \_ de BTH** es una opción avanzada que se usa principalmente para la validación. La opción de socket **\_ min de \_ MTU \_ de BTH** establece la MTU mínima de RFCOMM (unidad de transmisión máxima) para la negociación de la conexión. Las conexiones con una MTU de RFCOMM menor que este valor producen un error durante el proceso de aceptación de [**conexión**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [](/windows/desktop/api/winsock2/nf-winsock2-accept) . Aunque se permite establecer esta opción de socket para un socket conectado, no tiene ningún efecto si se ha completado la negociación. Al establecer esta opción de socket en un socket de escucha, se propaga el valor de todas las conexiones entrantes.

Solo un socket de escucha puede revisar la MTU hacia abajo, por lo que si el valor propuesto por el socket que se conecta es menor que el valor establecido para, por **lo que \_ BTH \_ MTU \_ min** en el socket de escucha, se rechaza la conexión. La MTU mínima debe estar entre la MTU mínima de **RFCOMM \_ \_** y la **\_ \_ MTU máxima de RFCOMM**, tal como se define en el archivo de encabezado Ws2bth. h.

En la \_ opción de BTH \_ MTU \_ min socket, *optval* es un puntero a ulong min \_ MTU; *optlen* es equivalente a "SIZEOF (ulong)".

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

[**conéctelo**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**acept**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 