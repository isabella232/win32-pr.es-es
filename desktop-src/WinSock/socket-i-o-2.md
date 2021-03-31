---
description: Mediante la e/s de bloqueo, la e/s de no bloqueo con notificación asincrónica de eventos de red y la e/s superpuestas con indicación de finalización en Windows Sockets 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: E/s de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efcd325a0a379671dd39709f37e2c6d2133ca27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154246"
---
# <a name="socket-io"></a>E/s de socket

Existen tres formas principales de realizar operaciones de e/s en Windows Sockets 2:

-   E/s de bloqueo.
-   E/s de no bloqueo junto con notificación asincrónica de eventos de red.
-   E/s superpuestas con indicación de finalización.

En las secciones siguientes se describe cada método. El bloqueo de e/s es el comportamiento predeterminado, el modo de no bloqueo se puede usar en cualquier socket que se encuentre en modo de no bloqueo, y la e/s superpuesta solo puede producirse en sockets creados con el atributo superpuesto. También es interesante tener en cuenta que las dos llamadas para enviar: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) y [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) y las dos llamadas para recibir: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) y [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) implementan los tres métodos de e/s. Los proveedores de servicios determinan cómo realizar la operación de e/s en función de los modos de socket, atributos y valores de parámetros de entrada.

 

 
