---
title: Captura manual de fotogramas
description: Captura manual de fotogramas
ms.assetid: 7c5576ff-2694-4f44-a386-03bbc6f9c2ed
keywords:
- WM_CAP_SINGLE_FRAME_OPEN mensaje
- WM_CAP_SINGLE_FRAME mensaje
- WM_CAP_SINGLE_FRAME_CLOSE mensaje
- capCaptureSingleFrameOpen macro
- CapCaptureSingleFrame (macro)
- CapCaptureSingleFrameClose macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9024f8759697248b1aadf2f46f902c4bf706c9d10417281d9b5c4f61fc1e94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138860"
---
# <a name="manual-frame-capture"></a>Captura manual de fotogramas

Si desea especificar individualmente los fotogramas que se capturan en una secuencia de vídeo, puede controlar la secuencia mediante los mensajes [**WM CAP SINGLE FRAME \_ \_ \_ \_ OPEN**](wm-cap-single-frame-open.md), [**WM CAP SINGLE \_ \_ \_ FRAME**](wm-cap-single-frame.md)y [**WM CAP SINGLE FRAME \_ \_ \_ \_ CLOSE**](wm-cap-single-frame-close.md) (o las macros [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame y**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) [**capCaptureSingleFrameClose).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) Normalmente, estos mensajes se usan para crear animaciones anexando fotogramas individuales al archivo de captura. WM \_ CAP SINGLE FRAME OPEN abre un archivo para una operación de captura controlada \_ \_ \_ manualmente. WM \_ CAP SINGLE FRAME captura un fotograma individual y lo anexa al archivo de \_ \_ captura. WM \_ CAP SINGLE FRAME CLOSE cierra el archivo que se usa para la captura manual de \_ \_ \_ fotogramas.

> [!Note]  
> Este método de captura no admite la captura de audio simultánea con la captura de vídeo.

 

 

 




