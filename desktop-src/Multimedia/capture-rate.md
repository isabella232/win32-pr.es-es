---
title: Velocidad de captura
description: Velocidad de captura
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup (macro)
- Estructura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP mensaje
- CapCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93be9e94f5f9085d25c6ad85a30b115d13349169
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266031"
---
# <a name="capture-rate"></a>Velocidad de captura

La velocidad de captura es el número de fotogramas que se capturan cada segundo de una sesión de captura. Puede recuperar la velocidad de captura actual mediante el mensaje [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (o la [**macro capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) La velocidad de captura actual se almacena en el **miembro dwRequestMicroSecPerFrame** de la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) Puede establecer la velocidad de captura especificando el número de microsegundos entre fotogramas sucesivos como valor de este miembro y, a continuación, enviando la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) El valor predeterminado de **dwRequestMicroSecPerFrame** es 66667, que corresponde a 15 fotogramas por segundo.

 

 




