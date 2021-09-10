---
title: User-Initiated capture
description: User-Initiated capture
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371948"
---
# <a name="user-initiated-capture"></a>User-Initiated capture

Puede recuperar el valor actual de la marca de captura iniciada por el usuario mediante el mensaje [**\_ GET SEQUENCE \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) El valor de la marca se almacena en el **miembro fMakeUserHitOKToCapture** de la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) Puede proporcionar al usuario un control preciso sobre cuándo iniciar una sesión de captura estableciendo este miembro en **TRUE.** AVICap muestra un cuadro de diálogo después de asignar todos los búferes de audio y vídeo para una sesión de captura. Esto permite al usuario eliminar los retrasos de captura debido a la inicialización de software. Si la aplicación usa un pequeño número de búferes de vídeo, este cuadro de diálogo probablemente no sea necesario. El valor predeterminado es **FALSE**.

 

 




