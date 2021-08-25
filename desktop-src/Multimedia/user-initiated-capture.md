---
title: User-Initiated capture
description: User-Initiated capture
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca015726aabe7c171f37590a98e60774c34a09c219ef445af3e30f199d5030b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892455"
---
# <a name="user-initiated-capture"></a>User-Initiated capture

Puede recuperar el valor actual de la marca de captura iniciada por el usuario mediante el mensaje [**\_ GET SEQUENCE \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) El valor de la marca se almacena en el **miembro fMakeUserHitOKToCapture** de la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) Puede proporcionar al usuario un control preciso sobre cuándo iniciar una sesión de captura estableciendo este miembro en **TRUE.** AVICap muestra un cuadro de diálogo después de asignar todos los búferes de vídeo y audio para una sesión de captura. Esto permite al usuario eliminar los retrasos de captura debido a la inicialización de software. Si la aplicación usa un pequeño número de búferes de vídeo, es probable que este cuadro de diálogo no sea necesario. El valor predeterminado es **FALSE**.

 

 




