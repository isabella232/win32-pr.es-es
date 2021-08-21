---
title: Captura de nombre de archivo
description: Captura de nombre de archivo
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE mensaje
- CapFileSetCaptureFile macro
- WM_CAP_FILE_GET_CAPTURE_FILE mensaje
- CapFileGetCaptureFile macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e48ecd727accccb868d0f78c68a833ac6ec6655bada23db8a56f2a9aeaffd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941600"
---
# <a name="capture-filename"></a>Captura de nombre de archivo

AVICap, de forma predeterminada, enruta los datos de secuencia de vídeo y audio de una ventana de captura a un archivo denominado CAPTURE.AVI en el directorio raíz de la unidad actual. Puede especificar un nombre de archivo alternativo enviando el mensaje [**WM CAP FILE SET CAPTURE \_ \_ \_ \_ \_ FILE**](wm-cap-file-set-capture-file.md) (o la macro [**capFileSetCaptureFile)**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) a una ventana de captura. Este mensaje especifica el nombre de archivo; no crea, asigna ni abre el archivo. Puede recuperar el nombre de archivo de captura actual enviando el mensaje [**\_ GET CAPTURE \_ \_ \_ \_ FILE**](wm-cap-file-get-capture-file.md) de WM CAP FILE (o la macro [**capFileGetCaptureFile)**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) a una ventana de captura.

 

 




