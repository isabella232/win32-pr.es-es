---
title: Búferes de vídeo
description: Búferes de vídeo
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup macro
- WM_CAP_SET_SEQUENCE_SETUP mensaje
- CapCaptureSetSetup macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e2f3e5b56f995e6a09792260ac2fd6e1ba5cd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245661"
---
# <a name="video-buffers"></a>Búferes de vídeo

Los búferes usados con la captura de vídeo residen en el montón de memoria. El número de búferes usados en una operación de captura puede variar y depender del valor del **miembro wNumVideoRequested** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) y de la memoria del sistema disponible.

Puede recuperar el valor actual de los búferes de vídeo solicitados mediante el mensaje [**\_ GET SEQUENCE \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) El número actual solicitado de búferes de vídeo se almacena en el **miembro wNumVideoRequested** de la **estructura CAPTUREPARMS.** Para solicitar la ubicación y el número de búferes, actualice este miembro y, a continuación, envíe la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje [**SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) de WM CAP (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)

 

 




