---
title: Capturar sin usar Disk Storage
description: Capturar sin usar Disk Storage
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- Mensaje WM_CAP_SEQUENCE_NOFILE
- capCaptureSequenceNoFile (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651294"
---
# <a name="capture-without-using-disk-storage"></a>Capturar sin usar Disk Storage

Puede usar los servicios de captura sin escribir los datos en un archivo de disco mediante el mensaje [**\_ \_ \_ nofile Sequence**](wm-cap-sequence-nofile.md) de la secuencia de Cap de WM (o la macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) ). Este mensaje solo es útil junto con las funciones de devolución de llamada que permiten que la aplicación use los datos de vídeo y audio directamente. Por ejemplo, las aplicaciones de videoconferencia podrían usar este mensaje para obtener fotogramas de vídeo en streaming. Las funciones de devolución de llamada transferirían las imágenes capturadas al equipo remoto.

 

 




