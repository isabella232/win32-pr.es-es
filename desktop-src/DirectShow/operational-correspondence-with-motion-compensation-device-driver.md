---
description: Correspondencia operativa con el controlador de dispositivo de compensación de movimiento
ms.assetid: bd92a0f4-98d9-497a-99b9-0cf432347daf
title: Correspondencia operativa con el controlador de dispositivo de compensación de movimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cca960ed8cbdae212bbe5e9f3b25316125a7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274674"
---
# <a name="operational-correspondence-with-motion-compensation-device-driver"></a>Correspondencia operativa con el controlador de dispositivo de compensación de movimiento

Esta sección contiene una descripción del lado del controlador de dispositivo de compensación de movimiento de la interfaz de DirectX VA. (Referencia: Windows 2000 DDK-controladores de gráficos-guía de diseño-3,0 DirectDraw DDI-3,12 compensación de movimiento. Vea el DDK de Windows para obtener documentación sobre las estructuras en negrita).

Los elementos siguientes hacen referencia a las entradas a las que se accede a través de la estructura **DD \_ MOTIONCOMPCALLBACKS** :

1.  Al principio del procesamiento pertinente, se usa el **DdMoCompCreate** del controlador del dispositivo para notificar al controlador que el descodificador de software comenzará a usar un objeto de aceleración de vídeo.
2.  Los GUID recibidos de [**IAMVideoAccelerator:: GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) proceden de la **DdMoCompGetGUIDs** del controlador del dispositivo.
3.  Una llamada a [**IAMVideoAccelerator:: GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) del PIN de entrada de nivel inferior devuelve datos de la **DdMoCompGetFormats** del controlador del dispositivo.
4.  La \_ estructura de datos de DXVA ConnectMode de [**IAMVideoAcceleratorNotify:: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) del descodificador se pasa a la **DdMoCompCreate** del controlador del dispositivo.
5.  Los datos devueltos de [**IAMVideoAccelerator:: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo) proceden de la **DdMoCompGetBuffInfo** del controlador del dispositivo.
6.  Los búferes enviados mediante [**IAMVideoAccelerator:: Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) los recibe el **DdMoCompRender** del controlador del dispositivo.
7.  El uso de [**IAMVideoAccelerator:: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) invoca la **DdMoCompQueryStatus** del controlador del dispositivo. Un código de retorno de DDERR \_ WASSTILLDRAWING de DdMoCompQueryStatus lo verá el descodificador de host como código de retorno E \_ pendiente de **IAMVideoAccelerator:: QueryRenderStatus**.
8.  Los datos enviados a [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) son recibidos por la **DdMoCompBeginFrame** del controlador del dispositivo. Un código de retorno E \_ Pending es necesario desde DdMoCompBeginFrame para que \_ el descodificador de host pueda verlo en respuesta a **IAMVideoAccelerator:: BeginFrame**.
9.  Los datos enviados a [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) son recibidos por la **DdMoCompEndFrame** del controlador del dispositivo.
10. Al final del procesamiento pertinente, se usa el **DdMoCompDestroy** del controlador del dispositivo para notificar al controlador que ya no se usará el objeto de aceleración de vídeo actual, de modo que el controlador pueda realizar cualquier limpieza necesaria.

 

 



