---
title: Granularidad de fragmentos de audio y vídeo
description: Granularidad de fragmentos de audio y vídeo
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- Archivos AVI, granularidad de fragmentos
- Clase AVICap, fragmentos de relleno
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994343"
---
# <a name="video-and-audio-chunk-granularity"></a>Granularidad de fragmentos de audio y vídeo

La granularidad de los fragmentos es un tamaño de bloque lógico para un archivo AVI que se usa para escribir y recuperar fragmentos de datos de audio y vídeo. Al escribir fragmentos de audio y vídeo en el disco, AVICap agrega fragmentos de relleno (fragmentos "no DESEAdos" de RIFF), según sea necesario, para rellenar cada bloque lógico de datos.

Puede recuperar la configuración de granularidad de fragmentos actual mediante el mensaje de configuración de la [**\_ secuencia de \_ \_ salida \_ de Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). La granularidad del fragmento actual se almacena en el miembro **wChunkGranularity** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Puede especificar una nueva granularidad de fragmentos como el valor de **wChunkGranularity** y, a continuación, enviar la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje de configuración de la secuencia de [](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) definición de Cap de WM (o la macro capCaptureSetSetup). [**\_ \_ \_ \_**](wm-cap-set-sequence-setup.md) También puede especificar cero para este miembro para establecer la granularidad del fragmento en el tamaño de sector del disco.

 

 




