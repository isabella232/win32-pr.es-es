---
description: Si un socket está en modo de no bloqueo, cualquier operación de e/s debe completarse inmediatamente o devolver el código de error WSAEWOULDBLOCK, lo que indica que la operación no se puede finalizar de inmediato.
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: Entrada/salida de no bloqueo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541531"
---
# <a name="nonblocking-inputoutput"></a>Entrada/salida de no bloqueo

Si un socket está en modo de no bloqueo, cualquier operación de e/s debe completarse inmediatamente o devolver el código de error WSAEWOULDBLOCK, lo que indica que la operación no se puede finalizar de inmediato. En el último caso, se necesita un mecanismo para detectar cuándo es adecuado volver a intentar la operación con la expectativa de que la operación se realizará correctamente. Se ha definido un conjunto de eventos de red para este fin. Estos eventos se pueden sondear o esperar mediante [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), o bien se pueden registrar para la entrega asincrónica llamando a [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) o [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). Consulte [notificación de eventos de red](notification-of-network-events-2.md) para obtener más información.

 

 
