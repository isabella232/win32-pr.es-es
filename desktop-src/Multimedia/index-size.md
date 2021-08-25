---
title: Tamaño de índice
description: Tamaño de índice
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup macro
- WM_CAP_SET_SEQUENCE_SETUP mensaje
- CapCaptureSetSetup macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9742edb1aa73c7b77a56ef3ab2a29a5ea14a1e70351bec1ecb49507bbd0bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784685"
---
# <a name="index-size"></a>Tamaño de índice

Cada archivo AVI usa un índice de un tamaño especificado para buscar fragmentos de datos de audio y vídeo dentro del archivo. Una entrada del índice busca un fotograma de vídeo o búfer de audio de forma de onda. Por lo tanto, el valor del tamaño del índice establece indirectamente el límite superior en el número de fotogramas que se pueden capturar en un archivo.

Puede recuperar el tamaño del índice actual mediante el mensaje [**\_ GET SEQUENCE \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) El tamaño del índice actual se almacena en el **miembro dwIndexSize** de la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) Puede especificar un nuevo tamaño de índice como el valor de **dwIndexSize** y, a continuación, enviar la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje [**SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) de WM CAP (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) El tamaño del índice predeterminado es de 34 952 entradas (lo que permite 32 000 fotogramas y un número proporcional de búferes de audio).

 

 




