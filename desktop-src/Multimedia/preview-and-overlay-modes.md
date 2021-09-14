---
title: Modos de vista previa y superposición
description: Modos de vista previa y superposición
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- WM_CAP_SET_PREVIEW mensaje
- capPreview macro
- WM_CAP_SET_PREVIEWRATE mensaje
- capPreviewRate (macro)
- WM_CAP_SET_SCALE mensaje
- CapPreviewScale macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4dc293587160d950856fccb15709a11e9533bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169561"
---
# <a name="preview-and-overlay-modes"></a>Modos de vista previa y superposición

Un controlador de captura puede implementar dos métodos para ver una secuencia de vídeo entrante: modo de vista previa y modo de superposición. Si un controlador de captura implementa ambos métodos, el usuario puede elegir qué método usar.

El modo de vista previa transfiere los fotogramas digitalizados del hardware de captura a la memoria del sistema y, a continuación, muestra los fotogramas digitalizados en la ventana de captura mediante funciones de interfaz de dispositivo gráfico (GDI). Las aplicaciones pueden reducir la tasa de vista previa cuando la ventana primaria pierde el foco y aumentar la tasa de vista previa cuando la ventana primaria obtiene el foco. Esta acción mejora la capacidad de respuesta general del sistema porque la operación de versión preliminar consume muchos procesadores.

Hay tres mensajes para controlar la operación de vista previa.

-   Use el [**mensaje WM CAP SET \_ \_ \_ PREVIEW**](wm-cap-set-preview.md) para habilitar o deshabilitar el modo de vista previa mediante el envío de (o la macro [**capPreview)**](/windows/desktop/api/Vfw/nf-vfw-cappreview) a una ventana de captura.
-   Use el [**mensaje WM CAP SET \_ \_ \_ PREVIEWRATE**](wm-cap-set-previewrate.md) (o la macro [**capPreviewRate)**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) para establecer la velocidad a la que se muestran los fotogramas en modo de vista previa.
-   Use el [**mensaje WM CAP SET \_ \_ \_ SCALE**](wm-cap-set-scale.md) (o la macro [**capPreviewScale)**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) para habilitar o deshabilitar el escalado del vídeo de vista previa.

Cuando la vista previa y el escalado están habilitados, el fotograma de vídeo capturado se extiende a las dimensiones de la ventana de captura. Habilitar el modo de vista previa deshabilita automáticamente el modo de superposición.

El modo de superposición es una función de hardware que muestra el contenido del búfer de captura en el monitor sin usar recursos de CPU. Puede habilitar y deshabilitar el modo de superposición enviando el mensaje OVERLAY de [**WM \_ CAP \_ SET \_**](wm-cap-set-overlay.md) (o la macro [**capOverlay)**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) a una ventana de captura. Al habilitar el modo de superposición, se deshabilita automáticamente el modo de vista previa.

También puede establecer la posición de desplazamiento del fotograma de vídeo dentro del área de cliente de la ventana de captura para el modo de vista previa o el modo de superposición mediante el envío del mensaje SCROLL de [**WM \_ CAP \_ SET \_**](wm-cap-set-scroll.md) (o la macro [**capSetScrollPos)**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) a una ventana de captura.

 

 




