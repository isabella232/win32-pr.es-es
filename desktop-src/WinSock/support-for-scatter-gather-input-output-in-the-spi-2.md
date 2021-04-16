---
description: Las rutinas WSPSend, WSPSendTo, WSPRecv y WSPRecvFrom toman una matriz de búferes de cliente como parámetros de entrada y, por lo tanto, se pueden usar para la e/s de dispersión y recopilación (o vector).
ms.assetid: ecd3d2f1-74b1-42f7-8402-3170112e3aca
title: Compatibilidad con la entrada/salida de dispersión y recopilación en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3f32e016c5c2e9f990c334716d4177d477c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715854"
---
# <a name="support-for-scattergather-inputoutput-in-the-spi"></a>Compatibilidad con la entrada/salida de dispersión y recopilación en el SPI

Las rutinas [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)), [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)), [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))y [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) toman una matriz de búferes de cliente como parámetros de entrada y, por lo tanto, se pueden usar para la e/s de dispersión y recopilación (o vector). Esto puede ser muy útil en las instancias en las que partes de cada mensaje que se transmiten constan de uno o varios componentes de encabezado de longitud fija además de un cuerpo de mensaje. Estos componentes de encabezado no se deben concatenar en un solo búfer contiguo antes del envío. Del mismo modo, al recibir, los componentes del encabezado se pueden dividir automáticamente en búferes independientes, lo que permite que el cuerpo del mensaje sea puro.

El uso de listas de búferes en lugar de un único búfer no cambia los límites que se aplican a las operaciones de recepción. En el caso de los protocolos orientados a mensajes, se completa una operación de recepción cada vez que se recibe un solo mensaje, independientemente de cuántos de los búferes proporcionados se hayan usado. Del mismo modo que para los protocolos orientados a flujos, se completa una recepción cuando una cantidad de bytes no especificada llega a través de la red, no necesariamente cuando todos los búferes proporcionados están llenos.

 

 
