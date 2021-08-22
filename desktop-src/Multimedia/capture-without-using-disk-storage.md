---
title: Capturar sin usar discos Storage
description: Capturar sin usar discos Storage
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- WM_CAP_SEQUENCE_NOFILE mensaje
- CapCaptureSequenceNoFile macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea708bd99cc2c325623eb53d734fadb2acdd0112e3a727fae9bfa741b8d301e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691625"
---
# <a name="capture-without-using-disk-storage"></a>Capturar sin usar discos Storage

Puede usar los servicios de captura sin escribir los datos en un archivo de disco mediante el mensaje [**WM \_ CAP SEQUENCE \_ \_ NOFILE**](wm-cap-sequence-nofile.md) (o la macro [**capCaptureSequenceNoFile).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) Este mensaje solo es útil junto con las funciones de devolución de llamada que permiten a la aplicación usar directamente los datos de audio y vídeo. Por ejemplo, las aplicaciones de videoconferencia pueden usar este mensaje para obtener fotogramas de vídeo de streaming. Las funciones de devolución de llamada transferirían las imágenes capturadas al equipo remoto.

 

 




