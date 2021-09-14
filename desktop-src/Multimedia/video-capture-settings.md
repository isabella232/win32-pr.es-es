---
title: Captura de vídeo Configuración
description: Captura de vídeo Configuración
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- Estructura CAPTUREPARMS
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup (macro)
- WM_CAP_SET_SEQUENCE_SETUP mensaje
- CapCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245624"
---
# <a name="video-capture-settings"></a>Captura de vídeo Configuración

La [**estructura CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) contiene los parámetros de control para la captura de vídeo de streaming. Esta estructura controla varios aspectos del proceso de captura y permite realizar las siguientes tareas:

-   Especifique la velocidad de fotogramas.
-   Especifique el número de búferes de vídeo asignados.
-   Deshabilite y habilite la captura de audio.
-   Especifique el intervalo de tiempo para la captura.
-   Especifique si se usa un dispositivo MCI (VCR o videodisc) durante la captura.
-   Especifique el control de teclado o mouse para finalizar el streaming.
-   Especifique el tipo de promedio de vídeo aplicado durante la captura.

Puede recuperar la configuración de captura actual dentro de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) enviando el mensaje [**GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la macro [**capCaptureGetSetup)**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) a una ventana de captura. Puede establecer una o varias configuraciones de captura actuales actualizando los miembros adecuados de la estructura **CAPTUREPARMS** y, a continuación, enviando el mensaje [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) y **CAPTUREPARMS** a una ventana de captura.

 

 




