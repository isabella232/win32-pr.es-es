---
description: Controlador MSDV
ms.assetid: 146ca753-fe41-49d3-8b1c-077e10a28192
title: Controlador MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7c1bda24980abe84a11613126476ccfe35380d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422762"
---
# <a name="msdv-driver"></a>Controlador MSDV

MSDV es el controlador de Microsoft Modelo de controlador de Windows (WDM) para camascopios DV. El controlador aparece como un filtro DirectShow cuando el dispositivo está conectado. Se enumera en dos categorías de filtro:

-   CLSID \_ VideoInputDeviceCategory ("orígenes de captura de vídeo")
-   \_Representación de KSCATEGORY AM \_ ("dispositivos de representación de transmisión por secuencias WDM")

El nombre descriptivo del filtro es `Microsoft DV Camera and VCR` o un equivalente localizado. En algunos dispositivos, la propiedad **Description** contiene una descripción del modelo específico, que se puede usar en lugar del nombre descriptivo genérico. Para obtener más información, consulte [seleccionar un dispositivo de captura](selecting-a-capture-device.md).

MSDV tiene dos clavijas de salida. Un PIN ofrece fotogramas DV que contienen datos de audio y vídeo intercalados. El otro PIN ofrece fotogramas solo de vídeo sin audio. MSDV no puede transmitir desde ambos PIN a la vez, por lo que solo se puede conectar un PIN de salida a la vez. Para obtener más información acerca de la captura de vídeo desde un dispositivo DV, consulte [Capture DV to file](capture-dv-to-file.md).

![capturar datos de DV desde el dispositivo](images/dv-filters4.png)

La mayoría de los camcorders DV tienen una subunidad de grabadora de cintas de vídeo (VTR), que puede transmitir datos desde la cinta al equipo. Para la aplicación, la captura desde cinta funciona igual que la captura de vídeo en directo. La única diferencia es que la aplicación debe controlar el transporte de cinta externo: iniciar y detener la cinta, rebobinar, etc. Para este propósito, MSDV expone las interfaces [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)y [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) . Para obtener más información acerca del control de un VTR, consulte [control de una videocámara DV](controlling-a-dv-camcorder.md).

También puede transmitir DV desde el equipo a la videocámara. Después, el vídeo se puede ver en la pantalla incorporada del camascopio o grabarse en una cinta. Para admitir esta funcionalidad, MSDV tiene un PIN de entrada que puede recibir un flujo DV intercalado. Cuando el PIN de entrada está conectado, MSDV actúa como un filtro de representador en lugar de un filtro de captura. MSDV no admite búsquedas en este modo. Para obtener más información acerca del envío de DV al dispositivo, consulte [transmisión de DV desde un archivo a una cinta](transmit-dv-from-file-to-tape.md).

![transmisión de datos de DV al dispositivo](images/dv-filters5.png)

Tenga en cuenta que los pin de entrada y salida no se pueden conectar al mismo tiempo, ya que el dispositivo no puede transmitir en ambas direcciones al mismo tiempo.

En muchos camcorders, cambiar entre el modo VTR y el modo de cámara hace que el dispositivo se apague. Por lo tanto, es posible que DirectShow pierda el dispositivo cuando el usuario cambie de modo. Para obtener información sobre los eventos de eliminación de dispositivos, consulte [notificación de eliminación de dispositivos](device-removal-notification.md).

## <a name="remarks"></a>Observaciones

Para obtener información acerca de los formatos DV que admite el controlador MSDV, consulte [**subtipos de vídeo DV**](dv-video-subtypes.md).

Algunas sugerencias sobre la creación de gráficos de filtro con MSDV:

-   No se puede usar [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para representar un PIN de salida en MSDV. (Filter Graph Manager intenta conectar el PIN de salida al pin de entrada de MSDV, que produce un error). En su lugar, use [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) o [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).
-   Cuando un gráfico de filtros contiene MSDV, MSDV debe proporcionar el reloj de referencia para el gráfico. A partir de DirectX 8,0, el administrador de gráficos de filtros elegirá automáticamente MSDV como el reloj de referencia. Con versiones anteriores, debería llamar al método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) en el administrador de gráficos de filtro. Para obtener más información sobre los relojes, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).
-   En función del dispositivo, algunos métodos de **IAMExtDevice**, **IAMExtTransport** y **IAMTimeCodeReader** pueden devolver códigos de error de Windows en lugar de valores **HRESULT** . Entre los posibles códigos de error se incluyen los siguientes.

    | Código de error              | Descripción                                                                                      |
    |-------------------------|--------------------------------------------------------------------------------------------------|
    | tiempo de espera de ERROR \_          | Se agotó el tiempo de espera de un comando de dispositivo externo.                                                        |
    | ERROR \_ req \_ no \_ ACCEP  | El dispositivo no aceptó este comando de dispositivo externo.                                          |
    | ERROR \_ no \_ admitido   | El dispositivo no admite este comando de dispositivo externo.                                        |
    | solicitud de ERROR \_ \_ anulada | Se anuló un comando de dispositivo externo. Es posible que se haya quitado el dispositivo o que se haya restablecido el bus. |

    

     

### <a name="device-information"></a>Información del dispositivo

En Windows Millennium Edition y Windows XP, el moniker de dispositivo del filtro DV admite una propiedad **Description** además de la propiedad **FriendlyName** . Esta propiedad devuelve una descripción del dispositivo, tomada del archivo INF, que normalmente contiene el nombre de marca del dispositivo. Sin embargo, esta propiedad no es compatible con todos los modelos de dispositivos.

Para obtener más información acerca de los monikers de dispositivo, consulte [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).

### <a name="clock-times"></a>Horas de reloj

El controlador MSDV usa el reloj de bus 1394 incluido en los paquetes de datos de 1394 para obtener el reloj. Utiliza estos valores para la marca de tiempo de los ejemplos de medios DV. Dado que este reloj de origen no es el reloj del sistema, las horas se desplazarán finalmente desde el reloj del sistema del equipo. No obstante, como se indicó anteriormente, el administrador de gráficos de filtros seleccionará MSDV como el reloj de referencia del gráfico.

La interfaz [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) notifica la medida actual del controlador de los fotogramas descartados; es posible que este valor no esté perfectamente sincronizado con el número real de fotogramas colocados en un momento dado. Si se quitan los marcos, indica que el sistema no está equilibrado (la producción de datos supera el consumo de datos). Por ejemplo, es posible que el disco duro del usuario no sea lo suficientemente rápido como para admitir velocidades de captura de DV.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



