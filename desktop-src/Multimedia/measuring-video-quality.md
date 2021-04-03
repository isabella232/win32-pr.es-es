---
title: Medición de la calidad del vídeo
description: Medición de la calidad del vídeo
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075648"
---
# <a name="measuring-video-quality"></a>Medición de la calidad del vídeo

Una manera de medir la calidad del vídeo es limitar el número de fotogramas capturados quitados durante la operación de captura. Una vez finalizada la captura de streaming, el valor de calidad se compara con la relación de fotogramas quitados con el total de fotogramas. Si el porcentaje de fotogramas quitados es mayor que el valor del miembro **wPercentDropForError** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) , AVICap envía un mensaje de error a la función de devolución de llamada de error si está instalada.

Puede recuperar el límite actual de fotogramas quitados (expresado como un porcentaje) mediante el mensaje de configuración de la secuencia de obtención de Cap de WM (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). [**\_ \_ \_ \_**](wm-cap-get-sequence-setup.md) Puede establecer un límite nuevo especificando un porcentaje como el valor del miembro **wPercentDropForError** de la estructura **CAPTUREPARMS** y, a continuación, enviando la estructura actualizada a la ventana de captura mediante el mensaje de configuración de la [**\_ \_ \_ secuencia \_ de límite de Cap de WM**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). El valor predeterminado de **wPercentDropForError** es 10 por ciento.

 

 




