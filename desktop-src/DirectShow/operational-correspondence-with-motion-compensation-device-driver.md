---
description: Correspondencia operativa con el controlador de dispositivo de compensación de movimiento
ms.assetid: bd92a0f4-98d9-497a-99b9-0cf432347daf
title: Correspondencia operativa con el controlador de dispositivo de compensación de movimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cca960ed8cbdae212bbe5e9f3b25316125a7456
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362379"
---
# <a name="operational-correspondence-with-motion-compensation-device-driver"></a>Correspondencia operativa con el controlador de dispositivo de compensación de movimiento

Esta sección contiene una descripción del lado del controlador de dispositivo de compensación de movimiento de la interfaz va de DirectX. (Referencia:Windows 2000 DDK - Controladores de gráficos - Guía de diseño - 3.0 DirectDraw DDI - Compensación de movimiento 3.12. Consulte el Windows DDK para obtener documentación sobre las estructuras en negrita).

Los elementos siguientes hacen referencia a las entradas a las que se accede a través de la estructura **\_ MOTIONCOMPCALLBACKS de DD:**

1.  Al principio del procesamiento pertinente, se usa **DdMoCompCreate** del controlador del dispositivo para notificar al controlador que el descodificador de software comenzará a usar un objeto de aceleración de vídeo.
2.  Los GUID recibidos de [**IAMVideoAccelerator::GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) se originan en **los DdMoCompGetGUID del** controlador de dispositivo.
3.  Una llamada a [**IAMVideoAccelerator::GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) del pin de entrada de bajada devuelve datos de **DdMoCompGetFormats del** controlador de dispositivo.
4.  La estructura de datos DXVA ConnectMode del descodificador \_ [**IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) se pasa a **DdMoCompCreate** del controlador de dispositivo.
5.  Los datos devueltos [**desde IAMVideoAccelerator::GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo) se originan en **DdMoCompGetBuffInfo del** controlador de dispositivo.
6.  El **DdMoCompRender** del controlador de dispositivo recibe los búferes enviados mediante [**IAMVideoAccelerator::Execute.**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute)
7.  El uso [**de IAMVideoAccelerator::QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) invoca el **DdMoCompQueryStatus** del controlador de dispositivo. El descodificador de host verá un código de retorno de DDERR WASSTCELADRAWING de DdMoCompQueryStatus como un código de retorno E PENDING de \_ \_ **IAMVideoAccelerator::QueryRenderStatus**.
8.  **DdMoCompBeginFrame** del controlador de dispositivo recibe los datos enviados a [**IAMVideoAccelerator::BeginFrame.**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) Se necesita un código de retorno E PENDING de DdMoCompBeginFrame para que el descodificador de host pueda ver E PENDING en respuesta a \_ \_ **IAMVideoAccelerator::BeginFrame**.
9.  El **DdMoCompEndFrame** del controlador de dispositivo recibe los datos enviados a [**IAMVideoAccelerator::EndFrame.**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe)
10. Al final del procesamiento pertinente, se usa **DdMoCompDestroy** del controlador del dispositivo para notificar al controlador que el objeto de aceleración de vídeo actual ya no se usará, de modo que el controlador pueda realizar cualquier limpieza necesaria.

 

 



