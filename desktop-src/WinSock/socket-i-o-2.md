---
description: Mediante E/S de bloqueo, E/S sin bloqueo con notificación asincrónica de eventos de red y E/S superpuesta con indicación de finalización en Windows Sockets 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: E/S de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162491d2cd840ed15e30f4d0aa9add7040807b148d16950fcb279e0984a26b54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993405"
---
# <a name="socket-io"></a>E/S de socket

Hay tres formas principales de realizar E/S en Windows Sockets 2:

-   Bloquear E/S.
-   E/S sin bloqueo junto con la notificación asincrónica de eventos de red.
-   E/S superpuesta con indicación de finalización.

En las secciones siguientes se describe cada método. Bloquear E/S es el comportamiento predeterminado, el modo de no bloqueo se puede usar en cualquier socket que se coloque en modo de no bloqueo y la E/S superpuesta solo puede producirse en sockets creados con el atributo superpuesto. También es interesante tener en cuenta que las dos llamadas para enviar: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) y [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) y las dos llamadas para recibir: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) y [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) implementan los tres métodos de E/S. Los proveedores de servicios determinan cómo realizar la operación de E/S en función de los modos de socket, los atributos y los valores de los parámetros de entrada.

 

 
