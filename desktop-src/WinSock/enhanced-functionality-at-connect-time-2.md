---
description: Windows Sockets 2 ofrece un conjunto expandido de operaciones que pueden producirse coincidentemente con el establecimiento de una conexión de socket. A continuación se describen los requisitos del proveedor de servicios para implementar estas características.
ms.assetid: fbc7055e-ea25-4d17-8039-f0fef300353c
title: Funcionalidad mejorada en Conectar tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70be979fc807a2de25d44eb90e9d344124963d12d42863447d335b4b7e4937f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132658"
---
# <a name="enhanced-functionality-at-connect-time"></a>Funcionalidad mejorada en Conectar tiempo

Windows Sockets 2 ofrece un conjunto expandido de operaciones que pueden producirse coincidentemente con el establecimiento de una conexión de socket. A continuación se describen los requisitos del proveedor de servicios para implementar estas características.

## <a name="conditional-acceptance"></a>Aceptación condicional

Como se ha descrito anteriormente, [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) invoca una función de condición proporcionada por el cliente que usa parámetros de entrada para proporcionar información sobre la solicitud de conexión pendiente. El cliente puede usar esta información para aceptar o rechazar una solicitud de conexión en función de la información del autor de la llamada, como el identificador del autor de la llamada, QoS, etc. Si la función de condición devuelve CF ACCEPT, se crea un nuevo socket con las mismas propiedades que el socket de escucha y se devuelve un identificador \_ para el nuevo socket. Si la función de condición devuelve CF REJECT, se debe rechazar \_ la solicitud de conexión. Si la función de condición devuelve CF DEFER, la decisión de aceptación o rechazo no se puede tomar inmediatamente y el proveedor de servicios debe dejar la solicitud de conexión en la cola \_ de trabajos pendientes. El cliente debe llamar de nuevo a **WSPAccept,** cuando esté listo para tomar una decisión, y organizar para que la función de condición devuelva CF ACCEPT o \_ CF \_ REJECT. Aunque una solicitud de conexión diferida se encuentra en la parte superior de la cola de trabajos pendientes, el proveedor de servicios no emite ninguna indicación adicional para las solicitudes de conexión pendientes.

## <a name="exchanging-user-data-at-connect-time"></a>Intercambio de datos de usuario a Conectar tiempo

Algunos protocolos permiten intercambiar una pequeña cantidad de datos de usuario en el momento de la conexión. Si estos datos se han recibido del host de conexión, se colocan en un búfer del proveedor de servicios y se proporciona un puntero a este búfer junto con un valor de longitud al cliente SPI de Winsock a través de parámetros de entrada a la función de condición [**WSPAccept.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) Si el cliente SPI de Winsock tiene datos de respuesta para volver al host de conexión, puede copiarlo en un búfer proporcionado por el proveedor de servicios. También se proporciona un puntero a este búfer y un entero que indica el tamaño del búfer como parámetros de entrada de función de condición (si el protocolo lo admite).

## <a name="establishing-socket-groups"></a>Establecer grupos de sockets

Todo el uso de grupos de sockets está reservado.

 

 



