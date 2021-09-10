---
title: Tamaño de índice
description: Tamaño de índice
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup (macro)
- WM_CAP_SET_SEQUENCE_SETUP mensaje
- CapCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372074"
---
# <a name="index-size"></a>Tamaño de índice

Cada archivo AVI usa un índice de un tamaño especificado para buscar fragmentos de datos de audio y vídeo dentro del archivo. Una entrada en el índice busca un fotograma de vídeo o búfer de audio de forma de onda. Por lo tanto, el valor del tamaño del índice establece indirectamente el límite superior en el número de fotogramas que se pueden capturar en un archivo.

Puede recuperar el tamaño del índice actual mediante el mensaje [**\_ GET SEQUENCE \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la [**macro capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) El tamaño del índice actual se almacena en el **miembro dwIndexSize** de la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) Puede especificar un nuevo tamaño de índice como el valor de **dwIndexSize** y, a continuación, enviar la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) El tamaño de índice predeterminado es de 34 952 entradas (lo que permite 32 000 fotogramas y un número proporcional de búferes de audio).

 

 




