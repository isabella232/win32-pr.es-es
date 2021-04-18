---
title: Captura de streaming desde un dispositivo MCI
description: Captura de streaming desde un dispositivo MCI
ms.assetid: 44cbf375-f97e-426a-a703-dfb1b1933138
keywords:
- MCI (interfaz de control multimedia), captura de streaming
- Mensaje WM_CAP_SET_MCI_DEVICE
- capSetMCIDeviceName (macro)
- Mensaje WM_CAP_GET_MCI_DEVICE
- capGetMCIDeviceName (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8cf358a87a812024328abf7fc1aae0509a126f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532361"
---
# <a name="streaming-capture-from-an-mci-device"></a>Captura de streaming desde un dispositivo MCI

Los dispositivos MCI amplían la operación de captura en captura en tiempo real y captura de fotogramas. Puede especificar el dispositivo MCI, como un CD o una grabadora de vídeo (VCR), que actúa como origen de vídeo de la operación de captura mediante el mensaje [**del \_ \_ \_ \_ dispositivo MCI del conjunto de Cap de WM**](wm-cap-set-mci-device.md) (o la macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) ) y especificando el nombre del dispositivo. También puede recuperar el nombre del dispositivo establecido actualmente mediante el mensaje [**Cap de WM \_ \_ obtener \_ \_ dispositivo MCI**](wm-cap-get-mci-device.md) (o la macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) ).

En la captura en tiempo real, la ventana de captura sincroniza la operación de captura y compensa los retrasos asociados con la colocación del origen de vídeo MCI y la inicialización de los recursos (por ejemplo, los búferes de captura) necesarios para capturar los datos. La ventana captura espera que se instale un dispositivo de vídeo MCI válido en el sistema para capturar datos de esta manera.

Las especificaciones para controlar un dispositivo MCI se almacenan en los miembros de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Entre los orígenes de vídeo compatibles con MCI se incluyen VCR y laserdiscs. Si el miembro **fMCIControl** de esta estructura se establece en **true**, la ventana de captura coordina la operación MCI. La ventana de captura utiliza los parámetros especificados en los miembros **dwMCIStartTime** y **dwMCIStopTime** para obtener las posiciones de inicio y detención, en milisegundos, de la secuencia. Si el valor de **fMCIControl** es **false**, el origen de vídeo no se trata como un dispositivo MCI y se omite el contenido de **dwMCIStartTime** y **dwMCIStopTime** .

Puede usar Media Player para comprobar rápidamente que un dispositivo de vídeo MCI esté conectado correctamente al sistema. La reproducción de un dispositivo con Media Player comprueba que la configuración de MCI del dispositivo es correcta. Si aparece una imagen en la pantalla de vídeo, el origen de vídeo se conecta correctamente al hardware de captura.

En la captura de fotogramas, la ventana de captura sincroniza la operación de captura y compensa los retrasos asociados con la colocación del origen de vídeo MCI y la inicialización de los recursos necesarios para capturar los datos. Además, la ventana de captura garantiza que no se quite ningún fotograma; se recorren los fotogramas de vídeo individualmente, asegurándose de que el fotograma se captura y se almacena antes de capturar el siguiente fotograma en el flujo de vídeo.

Las especificaciones para controlar la captura del marco de paso se almacenan en los miembros de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . La captura de paso-fotograma usa los siguientes miembros además de los miembros que se usan para la captura en tiempo real: **fStepMCIDevice**, **fStepCaptureAt2x** y **wStepCaptureAverageFrames**. Si el miembro **fStepMCIDevice** está establecido en **true**, la ventana de captura coordina la captura de fotogramas. La ventana de captura utiliza los parámetros especificados en los miembros **dwMCIStartTime** y **dwMCIStopTime** para las posiciones de inicio y detención, en milisegundos, de la secuencia. La ventana de captura usa **fStepCaptureAt2x** para determinar si el hardware de captura debe capturar fotogramas de vídeo dos veces la resolución normal y usa **wStepCaptureAverageFrames** para especificar el número de veces que se muestrea cada fotograma de la operación de captura.

Si **fStepMCIDevice** es **false**, se usa la captura en tiempo real en lugar de la captura de fotogramas de paso y el contenido de **fStepCaptureAt2x** y **wStepCaptureAverageFrames** se omiten.

Si se especifica una captura de fotogramas de paso y **fStepCaptureAt2x** está establecido en **true**, el hardware de captura capturará dos veces la resolución especificada. (Las resoluciones de alto y ancho se duplican). El software interpola los píxeles de la imagen de resolución superior para generar la imagen en la resolución especificada. Esta forma de promedio puede mejorar la definición de borde de imágenes en un fotograma. Puede habilitar esta opción si el hardware no admite la diezmación basada en hardware y está realizando la captura en formato RGB.

> [!Note]  
> Si el hardware admite la diezmación basada en hardware, puede capturar ejemplos a una velocidad superior a la especificada y usar estos ejemplos adicionales para obtener definiciones de color más coherentes con la imagen original. Los ejemplos adicionales se descartan después de usarse y el hardware pasa muestras al controlador de captura a la velocidad especificada.

 

Si se especifica una captura de paso-fotograma, el miembro **wStepCaptureAverageFrames** especifica el número de veces que se muestrea un fotograma al crear un marco basado en el ejemplo promedio. Esta técnica de promedio reduce el ruido de digitalización aleatorio que aparece en un fotograma. Un valor típico para el número de promedios es 5.

Para obtener más información acerca de MCI, consulte [MCI](mci.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Variaciones de captura](capture-variations.md)
</dt> </dl>

 

 




