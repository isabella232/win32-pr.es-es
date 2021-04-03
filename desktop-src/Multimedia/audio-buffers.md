---
title: Búferes de audio
description: Búferes de audio
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774713"
---
# <a name="audio-buffers"></a>Búferes de audio

Puede controlar la parte de audio de una operación de captura de tres maneras:

-   Incluir o excluir audio de la operación de captura.
-   Solicitar un número específico de búferes de audio.
-   Solicite que los búferes de audio tengan un tamaño específico.

Puede recuperar la configuración de los búferes de audio mediante el mensaje de configuración de la [**\_ secuencia de \_ \_ salida \_ de Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). El miembro **fCaptureAudio** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) especifica si el audio se incluye o se excluye de la operación de captura. El número solicitado actual de búferes de audio se almacena en el miembro **wNumAudioRequested** y el tamaño actual del búfer de audio se almacena en el miembro **dwAudioBufferSize** . Puede especificar si desea incluir la captura de audio, especificar el tamaño y el número de búferes de audio mediante la actualización de estos miembros y enviar la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje de configuración de la [](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) secuencia del conjunto de Cap de WM (o la macro capCaptureSetSetup). [**\_ \_ \_ \_**](wm-cap-set-sequence-setup.md)

De forma predeterminada, el audio se incluye en la operación de captura y se asignan cuatro búferes de audio. El valor predeterminado de **fCaptureAudio** es **true**. El tamaño de búfer predeterminado (el valor de **dwAudioBufferSize**) puede contener 0,5 segundos de datos de audio o 10 000, lo que sea mayor.

 

 




