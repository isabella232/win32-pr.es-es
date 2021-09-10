---
title: Capturar sin usar disk Storage
description: Capturar sin usar disk Storage
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- WM_CAP_SEQUENCE_NOFILE mensaje
- CapCaptureSequenceNoFile macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372062"
---
# <a name="capture-without-using-disk-storage"></a>Capturar sin usar disk Storage

Puede usar los servicios de captura sin escribir los datos en un archivo de disco mediante el mensaje [**\_ \_ \_ NOFILE SEQUENCE DE WM CAP**](wm-cap-sequence-nofile.md) (o la macro [**capCaptureSequenceNoFile).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) Este mensaje solo es útil junto con las funciones de devolución de llamada que permiten a la aplicación usar los datos de audio y vídeo directamente. Por ejemplo, las aplicaciones de videoconferencia pueden usar este mensaje para obtener fotogramas de vídeo de streaming. Las funciones de devolución de llamada transferirían las imágenes capturadas al equipo remoto.

 

 




