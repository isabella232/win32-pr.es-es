---
description: El destino predeterminado se puede cambiar simplemente llamando a WSPConnect de nuevo, incluso si el socket ya está conectado. Los datagramas en cola para la recepción se descartan si la nueva dirección es diferente de la dirección especificada en un WSPConnect anterior.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Volver a conectarse y desconectarse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4c50872b6690c42d97c3696bcfcb2586b9b5b510c17aafc5dcc159b17ed56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121365"
---
# <a name="reconnecting-and-disconnecting"></a>Volver a conectarse y desconectarse

El destino predeterminado se puede cambiar simplemente llamando a [**WSPConnect de**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) nuevo, incluso si el socket ya está conectado. Los datagramas en cola para la recepción se descartan si la nueva dirección es diferente de la dirección especificada en un **WSPConnect anterior.**

Si la dirección proporcionada para el socket es de ceros, el socket se desconectará( la dirección remota predeterminada será indeterminada, por lo que las llamadas [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) y [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) devolverán el código de error WSAENOTCONN, aunque todavía se pueden usar [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) y [**WSPRecvFrom.**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))

 

 
