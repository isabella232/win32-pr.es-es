---
title: Tamaño de índice
description: Tamaño de índice
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777119"
---
# <a name="index-size"></a>Tamaño de índice

Cada archivo AVI utiliza un índice de un tamaño especificado para buscar fragmentos de datos de vídeo y audio dentro del archivo. Una entrada en el índice busca un fotograma de vídeo o un búfer de audio de onda. Por consiguiente, el valor del tamaño del índice establece indirectamente el límite superior del número de fotogramas que se pueden capturar en un archivo.

Puede recuperar el tamaño del índice actual mediante el mensaje de configuración de la [**\_ \_ \_ \_ secuencia Get Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). El tamaño actual del índice se almacena en el miembro **dwIndexSize** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Puede especificar un nuevo tamaño de índice como el valor de **dwIndexSize** y, a continuación, enviar la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje de configuración de la secuencia del conjunto de límites de WM (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). [**\_ \_ \_ \_**](wm-cap-set-sequence-setup.md) El tamaño de índice predeterminado es 34.952 entradas (que permiten fotogramas de 32 KB y un número proporcional de búferes de audio).

 

 




