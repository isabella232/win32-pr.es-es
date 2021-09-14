---
title: Búferes de audio
description: Búferes de audio
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup macro
- WM_CAP_SET_SEQUENCE_SETUP mensaje
- CapCaptureSetSetup macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062994"
---
# <a name="audio-buffers"></a>Búferes de audio

Puede controlar la parte de audio de una operación de captura de tres maneras:

-   Incluya o excluya el audio de la operación de captura.
-   Solicite un número específico de búferes de audio.
-   Solicite que los búferes de audio sean de un tamaño específico.

Puede recuperar la configuración de los búferes de audio mediante el mensaje [**\_ GET SEQUENCE \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) El **miembro fCaptureAudio** de la [**estructura CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) especifica si el audio se incluye o se excluye de la operación de captura. El número actual solicitado de búferes de audio se almacena en el miembro **wNumAudioRequested** y el tamaño actual del búfer de audio se almacena en el **miembro dwAudioBufferSize.** Puede especificar si desea incluir la captura de audio, especificar el tamaño y el número de búferes de audio actualizando estos miembros y enviar la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje [**SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) de WM CAP (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)

De forma predeterminada, el audio se incluye en la operación de captura y se asignan cuatro búferes de audio. El valor predeterminado de **fCaptureAudio** es **TRUE.** El tamaño de búfer predeterminado (el valor **de dwAudioBufferSize)** puede contener 0,5 segundos de datos de audio o 10 000, lo que sea mayor.

 

 




