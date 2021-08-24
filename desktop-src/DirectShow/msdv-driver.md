---
description: Controlador MSDV
ms.assetid: 146ca753-fe41-49d3-8b1c-077e10a28192
title: Controlador MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5377471f61944c60f57720df6bc64482681d64515f54c853d78cfa405842ff15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748634"
---
# <a name="msdv-driver"></a>Controlador MSDV

MSDV es el controlador de Microsoft Windows Driver Model (WDM) para cámaras de vídeo DV. El controlador aparece como un filtro DirectShow cuando el dispositivo está conectado. Se enumera en dos categorías de filtro:

-   CLSID \_ VideoInputDeviceCategory ("Orígenes de captura de vídeo")
-   AM \_ KSCATEGORY \_ RENDER ("WDM Streaming Rendering Devices")

El nombre descriptivo del filtro es `Microsoft DV Camera and VCR` o un equivalente localizado. En algunos dispositivos, la **propiedad Description** contiene una descripción del modelo específico, que se puede usar en lugar del nombre descriptivo genérico. Para obtener más información, consulte [Selección de un dispositivo de captura.](selecting-a-capture-device.md)

MSDV tiene dos pines de salida. Un pin entrega fotogramas DV que contienen datos de audio y vídeo intercalados. El otro pin proporciona fotogramas solo de vídeo sin audio. MSDV no puede transmitir desde ambos pines a la vez, por lo que solo se puede conectar un pin de salida a la vez. Para obtener más información sobre cómo capturar vídeo desde un dispositivo DV, vea [Capture DV to File (Capturar DV en archivo).](capture-dv-to-file.md)

![captura de datos dv desde el dispositivo](images/dv-filters4.png)

La mayoría de las cámaras dv tienen una subunidad de grabadora de cintas de vídeo (VTR), que puede transmitir datos desde la cinta al equipo. Para la aplicación, la captura desde la cinta funciona igual que la captura de vídeo en directo. La única diferencia es que la aplicación debe controlar el transporte de cinta externo: iniciar y detener la cinta, rebobinar, etc. Para ello, MSDV expone las interfaces [**IAMExtDevice,**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice) [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)y [**IAMTimecodeReader.**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) Para obtener más información sobre cómo controlar una VTR, vea [Controlar una cámara de vídeo DV](controlling-a-dv-camcorder.md).

También puede transmitir DV desde el equipo a la cámara de vídeo. A continuación, el vídeo se puede ver en la pantalla incorporada de la cámara de vídeo o grabarse en cinta. Para admitir esta funcionalidad, MSDV tiene un pin de entrada que puede recibir una secuencia DV intercalada. Cuando el pin de entrada está conectado, MSDV actúa como un filtro de representador en lugar de un filtro de captura. MSDV no admite la búsqueda en este modo. Para obtener más información sobre cómo enviar DV al dispositivo, vea [Transmitir DV de archivo a cinta.](transmit-dv-from-file-to-tape.md)

![transmitir datos dv al dispositivo](images/dv-filters5.png)

Tenga en cuenta que los pines de entrada y salida no se pueden conectar al mismo tiempo, porque el dispositivo no puede transmitir en ambas direcciones al mismo tiempo.

En muchas cámaras de vídeo, el cambio entre el modo VTR y el modo de cámara hace que el dispositivo se apague. Por lo tanto, DirectShow puede perder el dispositivo cuando el usuario cambia de modo. Para obtener información sobre los eventos de eliminación de dispositivos, vea [Notificación de eliminación de dispositivos](device-removal-notification.md).

## <a name="remarks"></a>Comentarios

Para obtener información sobre qué formatos DV son compatibles con el controlador MSDV, vea [**Dv Video Subtypes ( Subtipos de vídeo DV).**](dv-video-subtypes.md)

Algunas sugerencias sobre la creación de gráficos de filtro con MSDV:

-   No se puede [**usar IGraphBuilder::Render para**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) representar un pin de salida en MSDV. (El administrador Graph filtro intenta conectar el pin de salida al pin de entrada de MSDV, lo que produce un error). En su lugar, [**use IGraphBuilder::Conectar**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) [**o ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).
-   Cuando un gráfico de filtro contiene MSDV, MSDV debe proporcionar el reloj de referencia para el gráfico. A partir de DirectX 8.0, filter Graph Manager elegirá automáticamente MSDV como reloj de referencia. Con versiones anteriores, debería llamar al método [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) en el Administrador de Graph filtros. Para obtener más información sobre los relojes, vea [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).
-   Según el dispositivo, algunos métodos de **IAMExtDevice,** **IAMExtTransport** y **IAMTimeCodeReader** podrían devolver Windows códigos de error en lugar de **valores HRESULT.** Los códigos de error posibles incluyen lo siguiente.

    | Código de error              | Descripción                                                                                      |
    |-------------------------|--------------------------------------------------------------------------------------------------|
    | TIEMPO DE ESPERA \_ DE ERROR          | Se ha pasado el tiempo de espera de un comando de dispositivo externo.                                                        |
    | ERROR \_ REQ \_ NOT \_ ACCEP  | El dispositivo no aceptó este comando de dispositivo externo.                                          |
    | ERROR \_ NO \_ ADMITIDO   | El dispositivo no admite este comando de dispositivo externo.                                        |
    | SOLICITUD DE ERROR \_ \_ ANULADA | Se anuló un comando de dispositivo externo. Posiblemente se quitó el dispositivo o se produjo un restablecimiento de bus. |

    

     

### <a name="device-information"></a>Información del dispositivo

En Windows Edition y Windows XP, el moniker de dispositivo del filtro DV admite una propiedad **Description** además de **la propiedad FriendlyName.** Esta propiedad devuelve una descripción del dispositivo, tomada del archivo INF, que normalmente contiene el nombre de marca del dispositivo. Sin embargo, esta propiedad no es compatible con todos los modelos de dispositivo.

Para obtener más información sobre los monikers de dispositivo, [vea Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).

### <a name="clock-times"></a>Horas de reloj

El controlador MSDV usa el reloj de bus 1394 que se encuentra en los paquetes de datos 1394 para derivar el reloj. Usa estos valores para marcar el tiempo de los ejemplos de medios DV. Dado que este reloj de origen no es el reloj del sistema del equipo, las horas finalmente se desplazarán del reloj del sistema del equipo. Sin embargo, como se indicó anteriormente, de forma predeterminada el Administrador de Graph filtro seleccionará MSDV como reloj de referencia del gráfico.

La [**interfaz IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) informa de la medida actual del controlador de fotogramas descartados; Es posible que este valor no esté perfectamente sincronizado con el número real de fotogramas descartados en un momento dado. Si se descartan fotogramas, indica que el sistema no está equilibrado (la producción de datos supera el consumo de datos). Por ejemplo, es posible que el disco duro del usuario no sea lo suficientemente rápido como para admitir las tasas de captura de DV.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



