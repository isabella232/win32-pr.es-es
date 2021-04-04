---
description: Windows Sockets 2 ofrece un conjunto expandido de operaciones que pueden producirse con coincidencias para establecer una conexión de socket. A continuación se describen los requisitos del proveedor de servicios para implementar estas características.
ms.assetid: fbc7055e-ea25-4d17-8039-f0fef300353c
title: Funcionalidad mejorada en tiempo de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33c6d7ee928fe7e97f535363e9e842285eef7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154287"
---
# <a name="enhanced-functionality-at-connect-time"></a>Funcionalidad mejorada en tiempo de conexión

Windows Sockets 2 ofrece un conjunto expandido de operaciones que pueden producirse con coincidencias para establecer una conexión de socket. A continuación se describen los requisitos del proveedor de servicios para implementar estas características.

## <a name="conditional-acceptance"></a>Aceptación condicional

Tal y como se ha descrito anteriormente, [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) invoca una función de condición proporcionada por el cliente que usa los parámetros de entrada para proporcionar información sobre la solicitud de conexión pendiente. El cliente puede usar esta información para aceptar o rechazar una solicitud de conexión en función de la información del llamador, como el identificador del autor de la llamada, QoS, etc. Si la función Condition devuelve CF \_ Accept, se crea un nuevo socket con las mismas propiedades que el socket de escucha y se devuelve un identificador al nuevo socket. Si la función Condition devuelve \_ el rechazo CF, se debe rechazar la solicitud de conexión. Si la función Condition devuelve el \_ aplazamiento CF, la decisión de aceptación y rechazo no se puede realizar inmediatamente, y el proveedor de servicios debe dejar la solicitud de conexión en la cola de trabajos pendientes. El cliente debe llamar de nuevo a **WSPAccept** , cuando esté listo para tomar una decisión y organizar la función de condición para que devuelva el rechazo de CF \_ o de CF \_ . Mientras que una solicitud de conexión diferida se encuentra en la parte superior de la cola de trabajos pendientes, el proveedor de servicios no emite ninguna indicación adicional para las solicitudes de conexión pendientes.

## <a name="exchanging-user-data-at-connect-time"></a>Intercambio de datos de usuario en tiempo de conexión

Algunos protocolos permiten que se intercambie una pequeña cantidad de datos de usuario en el momento de la conexión. Si dichos datos se han recibido desde el host de conexión, se colocan en un búfer del proveedor de servicios y se proporciona un puntero a este búfer junto con un valor de longitud al cliente de Winsock SPI a través de los parámetros de entrada de la función de condición [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) . Si el cliente de Winsock SPI tiene datos de respuesta para volver al host de conexión, puede copiarlos en un búfer proporcionado por el proveedor de servicios. Un puntero a este búfer y un entero que indica que el tamaño de búfer también se proporciona como parámetros de entrada de la función de condición (si es compatible con el protocolo).

## <a name="establishing-socket-groups"></a>Establecimiento de grupos de sockets

Todo el uso de grupos de sockets está reservado.

 

 



