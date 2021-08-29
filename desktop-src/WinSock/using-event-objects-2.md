---
description: Windows Los objetos de evento sockets son construcciones simples que se pueden crear y cerrar, establecer y borrar, esperar y sondear.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: Usar objetos de evento (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d500656279d328046e2792b47a296bc2347e3478e36c7d81a5e781023887dc51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121165"
---
# <a name="using-event-objects-windows-sockets-2"></a>Usar objetos de evento (Windows Sockets 2)

Windows Los objetos de evento sockets son construcciones simples que se pueden crear y cerrar, establecer y borrar, esperar y sondear. El modelo aceptado es para que los clientes creen un objeto de evento y proporcionen el identificador como parámetro (o como componente de una estructura de parámetros) en funciones como [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) y [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). Cuando se ha producido la condición designada, el proveedor de servicios usa el identificador para establecer el objeto de evento llamando a [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent). Mientras tanto, el cliente SPI de Winsock puede bloquear y esperar o sondear hasta que se establezca (se señale) el objeto de evento. Posteriormente, el cliente puede borrar o restablecer el objeto de evento y usarlo de nuevo.

 

 
