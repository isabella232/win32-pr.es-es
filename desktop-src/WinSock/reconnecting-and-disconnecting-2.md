---
description: El destino predeterminado se puede cambiar simplemente llamando a WSPConnect, incluso si el socket ya está conectado. Los datagramas en cola para la recepción se descartan si la nueva dirección es diferente de la especificada en un WSPConnect anterior.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Volver a conectar y desconectar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7babefe03be44f942ee60a840aa210ee3c0e25da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908687"
---
# <a name="reconnecting-and-disconnecting"></a>Volver a conectar y desconectar

El destino predeterminado se puede cambiar simplemente llamando a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , incluso si el socket ya está conectado. Los datagramas en cola para la recepción se descartan si la nueva dirección es diferente de la especificada en un **WSPConnect** anterior.

Si la dirección proporcionada para el socket es cero, el socket se desconectará; la dirección remota predeterminada será indeterminada, por lo que las llamadas a [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) y [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) devolverán el código de error WSAENOTCONN, aunque es posible que se sigan usando [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) y [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) .

 

 
