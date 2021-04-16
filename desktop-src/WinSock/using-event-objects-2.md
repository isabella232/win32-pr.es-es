---
description: Los objetos de evento de Windows Sockets son construcciones simples que se pueden crear y cerrar, establecer y borrar, esperar y sondear.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: Usar objetos de eventos (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26a9b70ff49bf7d46f2907c04fd8911d55dd623
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705588"
---
# <a name="using-event-objects-windows-sockets-2"></a>Usar objetos de eventos (Windows Sockets 2)

Los objetos de evento de Windows Sockets son construcciones simples que se pueden crear y cerrar, establecer y borrar, esperar y sondear. El modelo aceptado es para que los clientes creen un objeto de evento y suministren el identificador como un parámetro (o como un componente de una estructura de parámetros) en funciones como [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) y [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). Cuando se ha producido la condición nombrada, el proveedor de servicios utiliza el identificador para establecer el objeto de evento mediante una llamada a [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent). Mientras tanto, el cliente de Winsock SPI puede bloquear y esperar o sondear hasta que el objeto de evento se establezca (señalado). Después, el cliente puede borrar o restablecer el objeto de evento y volver a usarlo.

 

 
