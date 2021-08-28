---
title: Granularidad de fragmentos de audio y vídeo
description: Granularidad de fragmentos de audio y vídeo
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- Archivos AVI, granularidad de fragmentos
- Clase AVICap, fragmentos de relleno
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup macro
- WM_CAP_SET_SEQUENCE_SETUP mensaje
- CapCaptureSetSetup macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e8e03eb774e4173b86812c7cc4e9fb35d0ab2557d1ab9022bce3848ec7d13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892245"
---
# <a name="video-and-audio-chunk-granularity"></a>Granularidad de fragmentos de audio y vídeo

La granularidad del fragmento es un tamaño de bloque lógico para un archivo AVI que se usa para escribir y recuperar fragmentos de datos de audio y vídeo. Al escribir fragmentos de audio y vídeo en el disco, AVICap agrega fragmentos de relleno (fragmentos "JUNK" de RIFF) según sea necesario para rellenar cada bloque lógico de datos.

Puede recuperar la configuración de granularidad del fragmento actual mediante el mensaje [**\_ GET SEQUENCE \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) La granularidad del fragmento actual se almacena en el **miembro wChunkGranularity** de la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) Puede especificar una nueva granularidad de fragmentos como el valor de **wChunkGranularity** y, a continuación, enviar la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje [**SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) de WM CAP (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) También puede especificar cero para este miembro para establecer la granularidad del fragmento en el tamaño de sector del disco.

 

 




