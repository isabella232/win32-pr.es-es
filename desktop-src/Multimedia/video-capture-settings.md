---
title: Configuración de captura de vídeo
description: Configuración de captura de vídeo
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- Estructura CAPTUREPARMS
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665613"
---
# <a name="video-capture-settings"></a>Configuración de captura de vídeo

La estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) contiene los parámetros de control para streaming de vídeo. Esta estructura controla varios aspectos del proceso de captura y permite realizar las siguientes tareas:

-   Especifique la velocidad de fotogramas.
-   Especifique el número de búferes de vídeo asignados.
-   Deshabilitar y habilitar la captura de audio.
-   Especifique el intervalo de tiempo para la captura.
-   Especifique si se usa un dispositivo MCI (VCR o videodisco) durante la captura.
-   Especifique el control del teclado o del mouse para finalizar el streaming.
-   Especifique el tipo de promedio de vídeo que se aplica durante la captura.

Puede recuperar la configuración de captura actual dentro de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) mediante el envío del mensaje de [**\_ \_ \_ \_ configuración de salida de Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ) a una ventana de captura. Puede establecer una o varias configuraciones de captura actuales si actualiza los miembros adecuados de la estructura **CAPTUREPARMS** y, a continuación, envía el mensaje de configuración de la secuencia de [**definición de Cap de WM \_ \_ \_ \_**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ) y **CAPTUREPARMS** a una ventana de captura.

 

 




