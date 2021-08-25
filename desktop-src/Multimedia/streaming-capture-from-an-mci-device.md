---
title: Captura de streaming desde un dispositivo MCI
description: Captura de streaming desde un dispositivo MCI
ms.assetid: 44cbf375-f97e-426a-a703-dfb1b1933138
keywords:
- MCI (interfaz de control multimedia), captura de streaming
- WM_CAP_SET_MCI_DEVICE mensaje
- CapSetMCIDeviceName macro
- WM_CAP_GET_MCI_DEVICE mensaje
- CapGetMCIDeviceName macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d469465f47e908bda2512261ea638ad23e931a43cbb0449df676829469c3d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892595"
---
# <a name="streaming-capture-from-an-mci-device"></a>Captura de streaming desde un dispositivo MCI

Los dispositivos MCI aumentan la operación de captura en la captura en tiempo real y la captura de fotogramas paso a paso. Puede especificar el dispositivo MCI, como una grabadora videodisc o video-recorder (VCR), que actúa como origen de vídeo para la operación de captura mediante el mensaje [**WM \_ CAP SET \_ \_ MCI \_ DEVICE**](wm-cap-set-mci-device.md) (o la macro [**capSetMCIDeviceName)**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) y especificando el nombre del dispositivo. También puede recuperar el nombre del dispositivo establecido actualmente mediante el mensaje [**\_ GET \_ \_ MCI \_ DEVICE**](wm-cap-get-mci-device.md) de WM CAP (o la macro [**capGetMCIDeviceName).**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename)

En la captura en tiempo real, la ventana de captura sincroniza la operación de captura y compensa los retrasos asociados con la posición del origen de vídeo de MCI y la inicialización de los recursos (como los búferes de captura) necesarios para capturar datos. La ventana de captura espera que se instale un dispositivo de vídeo MCI válido en el sistema para capturar datos de esta manera.

Las especificaciones para controlar un dispositivo MCI se almacenan en los miembros de la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) Los orígenes de vídeo compatibles con MCI incluyen vcr y escánerdiscs. Si el **miembro fMCIControl** de esta estructura se establece en **TRUE,** la ventana de captura coordina la operación MCI. La ventana de captura usa los parámetros especificados en los miembros **dwMCIStartTime** y **dwMCIStopTime** para obtener las posiciones inicial y de detención, en milisegundos, de la secuencia. Si el valor de **fMCIControl** es **FALSE,** el origen del vídeo no se trata como un dispositivo MCI y se omite el contenido de **dwMCIStartTime** y **dwMCIStopTime.**

Puede usar Media Player para comprobar rápidamente que un dispositivo de vídeo MCI está conectado correctamente al sistema. La reproducción de un dispositivo Media Player comprueba que la configuración de MCI del dispositivo es correcta. Si aparece una imagen en la pantalla de vídeo, el origen del vídeo se conecta correctamente al hardware de captura.

En la captura de fotogramas paso a paso, la ventana de captura sincroniza la operación de captura y compensa los retrasos asociados al posicionamiento del origen de vídeo de MCI e inicialización de los recursos necesarios para capturar datos. Además, la ventana de captura garantiza que no se descarta ningún fotograma; se desplaza por los fotogramas de vídeo individualmente, lo que garantiza que el fotograma se captura y se almacena antes de capturar el fotograma siguiente en la secuencia de vídeo.

Las especificaciones para controlar la captura de fotogramas paso a paso se almacenan en los miembros de la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) La captura de fotogramas paso a paso usa los siguientes miembros además de los miembros usados para la captura en tiempo real: **fStepMCIDevice**, **fStepCaptureAt2x** y **wStepCaptureAverageFrames**. Si el **miembro fStepMCIDevice** está establecido en **TRUE,** la ventana de captura coordina la captura de fotogramas paso a paso. La ventana de captura usa los parámetros especificados en los miembros **dwMCIStartTime** y **dwMCIStopTime** para las posiciones de inicio y detención, en milisegundos, de la secuencia. La ventana de captura usa **fStepCaptureAt2x** para determinar si el hardware de captura debe capturar fotogramas de vídeo con el doble de resolución normal y **usa wStepCaptureAverageFrames** para especificar el número de veces que se muestrea cada fotograma de la operación de captura.

Si **fStepMCIDevice** es **FALSE,** se usa la captura en tiempo real en lugar de la captura de fotogramas paso a paso y se omite el contenido de **fStepCaptureAt2x** y **wStepCaptureAverageFrames.**

Si se especifica una captura de fotogramas paso a paso y **fStepCaptureAt2x** se establece en **TRUE,** el hardware de captura captura el doble de la resolución especificada. (Las resoluciones del alto y el ancho se duplican). El software interpola los píxeles de la imagen de resolución superior para generar la imagen en la resolución especificada. Esta forma de promedio puede mejorar la definición del borde de las imágenes en un marco. Puede habilitar esta opción si el hardware no admite la decimación basada en hardware y está capturando en formato RGB.

> [!Note]  
> Si el hardware admite la decimación basada en hardware, puede capturar muestras a una velocidad superior a la especificada y usar estas muestras adicionales para obtener definiciones de color más coherentes con la imagen original. Las muestras adicionales se descartan después de su uso y el hardware pasa muestras al controlador de captura a la velocidad especificada.

 

Si se especifica una captura de fotogramas paso a paso, el **miembro wStepCaptureAverageFrames** especifica el número de veces que se muestrea un fotograma al crear un fotograma basado en el promedio de ejemplo. Esta técnica de promedio reduce el ruido de digitalización aleatorio que aparece en un fotograma. Un valor típico para el número de promedios es 5.

Para obtener más información sobre MCI, vea [MCI](mci.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar variaciones](capture-variations.md)
</dt> </dl>

 

 




