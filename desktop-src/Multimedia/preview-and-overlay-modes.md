---
title: Modos de vista previa y superposición
description: Modos de vista previa y superposición
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- Mensaje WM_CAP_SET_PREVIEW
- capPreview (macro)
- Mensaje WM_CAP_SET_PREVIEWRATE
- capPreviewRate (macro)
- Mensaje WM_CAP_SET_SCALE
- capPreviewScale (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4dc293587160d950856fccb15709a11e9533bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994115"
---
# <a name="preview-and-overlay-modes"></a>Modos de vista previa y superposición

Un controlador de captura puede implementar dos métodos para ver una secuencia de vídeo entrante: modo de vista previa y modo de superposición. Si un controlador de captura implementa ambos métodos, el usuario puede elegir el método que se va a usar.

El modo de vista previa transfiere fotogramas digitalizados del hardware de captura a la memoria del sistema y, a continuación, muestra los fotogramas digitalizados en la ventana de captura mediante funciones de la interfaz de dispositivo gráfico (GDI). Es posible que las aplicaciones disminuyan la velocidad de vista previa cuando la ventana primaria pierde el foco y aumentan la velocidad de vista previa cuando la ventana primaria gana el foco. Esta acción mejora la capacidad de respuesta del sistema general porque la operación de vista previa es intensiva en el procesador.

Hay tres mensajes para controlar la operación de vista previa.

-   Use el mensaje de [**\_ \_ \_ vista previa de límite de Cap de WM**](wm-cap-set-preview.md) para habilitar o deshabilitar el modo de vista previa mediante el envío de la (o la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) ) a una ventana de captura.
-   Use el [**mensaje \_ \_ \_ PREVIEWRATE del conjunto de límites de WM**](wm-cap-set-previewrate.md) (o la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) ) para establecer la velocidad a la que se muestran los fotogramas en el modo de vista previa.
-   Use el mensaje de escala del conjunto de Cap de WM (o la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) ) para habilitar o deshabilitar el escalado del vídeo de vista previa. [**\_ \_ \_**](wm-cap-set-scale.md)

Cuando se habilitan la vista previa y el escalado, el fotograma de vídeo capturado se ajusta a las dimensiones de la ventana de captura. Al habilitar el modo de vista previa se deshabilita automáticamente el modo de superposición.

El modo de superposición es una función de hardware que muestra el contenido del búfer de captura en el monitor sin usar recursos de CPU. Puede habilitar y deshabilitar el modo de superposición enviando el mensaje de [**\_ \_ \_ superposición de conjunto de Cap de WM**](wm-cap-set-overlay.md) (o la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) ) a una ventana de captura. Al habilitar el modo de superposición, se deshabilita automáticamente el modo vista previa.

También puede establecer la posición de desplazamiento del fotograma de vídeo en el área cliente de la ventana de captura para el modo de vista previa o el modo de superposición enviando el mensaje de desplazamiento del conjunto de límites de WM (o la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) ) a una ventana de captura. [**\_ \_ \_**](wm-cap-set-scroll.md)

 

 




