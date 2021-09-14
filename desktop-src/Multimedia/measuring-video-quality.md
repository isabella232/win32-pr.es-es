---
title: Medición de la calidad del vídeo
description: Medición de la calidad del vídeo
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup macro
- WM_CAP_SET_SEQUENCE_SETUP mensaje
- CapCaptureSetSetup macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071760"
---
# <a name="measuring-video-quality"></a>Medición de la calidad del vídeo

Una manera de medir la calidad del vídeo es limitar el número de fotogramas capturados descartados durante la operación de captura. Una vez finalizada la captura de streaming, el valor de calidad se compara con la proporción de fotogramas eliminados con el total de fotogramas. Si el porcentaje de fotogramas eliminados es mayor que el valor del miembro **wPercentDropForError** de la estructura [**CAPTUREPARMS,**](/windows/win32/api/vfw/ns-vfw-captureparms) AVICap envía un mensaje de error a la función de devolución de llamada de error si está instalada.

Puede recuperar el límite actual de fotogramas eliminados (expresados como porcentaje) mediante el mensaje [**\_ GET SEQUENCE \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) Puede establecer un nuevo límite especificando un porcentaje como valor del miembro **wPercentDropForError** de la estructura **CAPTUREPARMS** y, a continuación, enviando la estructura actualizada a la ventana de captura mediante el mensaje [**SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) de WM CAP (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) El valor predeterminado de **wPercentDropForError** es del 10 por ciento.

 

 




