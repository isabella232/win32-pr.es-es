---
title: User-Initiated captura
description: User-Initiated captura
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903714"
---
# <a name="user-initiated-capture"></a>User-Initiated captura

Puede recuperar el valor actual de la marca de captura iniciada por el usuario mediante el mensaje de configuración de la [**\_ \_ \_ \_ secuencia Get Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). El valor de la marca se almacena en el miembro **fMakeUserHitOKToCapture** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Puede proporcionar al usuario un control preciso sobre cuándo iniciar una sesión de captura estableciendo este miembro en **true**. AVICap muestra un cuadro de diálogo después de asignar todos los búferes de vídeo y audio para una sesión de captura. Esto permite al usuario eliminar los retrasos de captura debido a la inicialización del software. Si la aplicación usa un número pequeño de búferes de vídeo, es probable que este cuadro de diálogo no sea necesario. El valor predeterminado es **FALSE**.

 

 




