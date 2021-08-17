---
description: Las rutinas WSPSend, WSPSendTo, WSPRecv y WSPRecvFrom toman una matriz de búferes de cliente como parámetros de entrada y, por tanto, se pueden usar para la E/S de dispersión/recopilación (o vectores).
ms.assetid: ecd3d2f1-74b1-42f7-8402-3170112e3aca
title: Compatibilidad con la entrada y salida de dispersión/recopilación en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b136898c1163ab298d8a177238f11239262b04306662b3f11b75bfb847f335d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740002"
---
# <a name="support-for-scattergather-inputoutput-in-the-spi"></a>Compatibilidad con la entrada y salida de dispersión/recopilación en el SPI

Las rutinas [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)), [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)), [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))y [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) toman una matriz de búferes de cliente como parámetros de entrada y, por tanto, se pueden usar para la E/S de dispersión/recopilación (o vectores). Esto puede ser muy útil en instancias en las que las partes de cada mensaje que se transmiten constan de uno o varios componentes de encabezado de longitud fija además de un cuerpo del mensaje. Estos componentes de encabezado no deben concatenarse en un solo búfer contiguo antes de enviarlos. Del mismo modo, al recibir, los componentes de encabezado se pueden dividir automáticamente en búferes independientes, dejando el cuerpo del mensaje puro.

El uso de listas de búferes en lugar de un solo búfer no cambia los límites que se aplican a las operaciones de recepción. En el caso de los protocolos orientados a mensajes, una operación de recepción se completa cada vez que se recibe un único mensaje, independientemente de cuántos o pocos de los búferes proporcionados se hayan usado. Del mismo modo para los protocolos orientados a secuencias, una recepción se completa cuando llega una cantidad no especificada de bytes a través de la red, no necesariamente cuando todos los búferes proporcionados están llenos.

 

 
