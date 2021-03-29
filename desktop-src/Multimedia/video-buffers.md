---
title: Búferes de vídeo
description: Búferes de vídeo
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e2f3e5b56f995e6a09792260ac2fd6e1ba5cd7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778120"
---
# <a name="video-buffers"></a>Búferes de vídeo

Los búferes que se usan con la captura de vídeo residen en el montón de memoria. El número de búferes utilizados en una operación de captura puede variar y depender del valor del miembro **wNumVideoRequested** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) y de la memoria disponible del sistema.

Puede recuperar el valor actual de los búferes de vídeo solicitados mediante el mensaje de configuración de la [**\_ secuencia de \_ \_ salida \_ Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). El número solicitado actual de búferes de vídeo se almacena en el miembro **wNumVideoRequested** de la estructura **CAPTUREPARMS** . Puede solicitar la ubicación y el número de búferes si actualiza este miembro y, a continuación, envía la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje de configuración de la secuencia de [](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) definición de Cap de WM (o la macro capCaptureSetSetup). [**\_ \_ \_ \_**](wm-cap-set-sequence-setup.md)

 

 




