---
title: Nombre de archivo de captura
description: Nombre de archivo de captura
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- Mensaje WM_CAP_FILE_SET_CAPTURE_FILE
- capFileSetCaptureFile (macro)
- Mensaje WM_CAP_FILE_GET_CAPTURE_FILE
- capFileGetCaptureFile (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4856649906e09f212d2f8992c9d4fb9b8f4c37d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676159"
---
# <a name="capture-filename"></a>Nombre de archivo de captura

De forma predeterminada, AVICap enruta los datos de vídeo y de secuencia de audio desde una ventana de captura a un archivo denominado CAPTURE.AVI en el directorio raíz de la unidad actual. Puede especificar un nombre de archivo alternativo mediante el envío del mensaje de archivo de límite de WM (o la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) a una ventana de captura [**\_ \_ \_ \_ \_**](wm-cap-file-set-capture-file.md) . Este mensaje especifica el nombre de archivo; no crea, asigna ni abre el archivo. Puede recuperar el nombre de archivo de captura actual mediante el envío del mensaje de archivo [**Cap de WM \_ \_ \_ Get \_ Capture \_ File**](wm-cap-file-get-capture-file.md) (o la macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ) a una ventana de captura.

 

 




