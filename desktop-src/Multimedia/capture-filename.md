---
title: Capture Filename
description: Capture Filename
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE mensaje
- CapFileSetCaptureFile macro
- WM_CAP_FILE_GET_CAPTURE_FILE mensaje
- CapFileGetCaptureFile macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4856649906e09f212d2f8992c9d4fb9b8f4c37d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062922"
---
# <a name="capture-filename"></a>Capture Filename

AVICap, de forma predeterminada, enruta los datos de secuencia de audio y vídeo desde una ventana de captura a un archivo denominado CAPTURE.AVI en el directorio raíz de la unidad actual. Puede especificar un nombre de archivo alternativo enviando el mensaje [**WM CAP FILE SET CAPTURE \_ \_ \_ \_ \_ FILE**](wm-cap-file-set-capture-file.md) (o la macro [**capFileSetCaptureFile)**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) a una ventana de captura. Este mensaje especifica el nombre de archivo; no crea, asigna ni abre el archivo. Puede recuperar el nombre de archivo de captura actual enviando el mensaje [**\_ GET CAPTURE \_ \_ \_ \_ FILE**](wm-cap-file-get-capture-file.md) de WM CAP FILE (o la macro [**capFileGetCaptureFile)**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) a una ventana de captura.

 

 




