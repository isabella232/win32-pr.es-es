---
description: En este tema se describe cómo los objetos de canalización personalizados pueden admitir velocidades de reproducción variables, incluida la reproducción inversa. Para obtener información sobre el uso del control de tasa desde una aplicación, vea Rate (control).
ms.assetid: 077678db-ca5a-423b-9430-93497113d639
title: Control de tasa de implementación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5fd78cbbb95316a0d4ed12a50c9d3aa8954fe8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083036"
---
# <a name="implementing-rate-control"></a>Control de tasa de implementación

En este tema se describe cómo los objetos de canalización personalizados pueden admitir velocidades de reproducción variables, incluida la reproducción inversa. Para obtener información sobre el uso del control de tasa desde una aplicación, vea [Rate (control](rate-control.md)).

Este tema contiene las siguientes secciones:

-   [Orígenes multimedia](#media-sources)
-   [Media Foundation transformaciones](#media-foundation-transforms)
    -   [Reproducción inversa](#reverse-playback)
-   [Receptores de medios](#media-sinks)
-   [Temas relacionados](#related-topics)

Si está escribiendo un objeto de canalización de Microsoft Media Foundation (un origen multimedia, una transformación o un receptor multimedia), es posible que necesite admitir velocidades de reproducción variables. Para ello, implemente las interfaces siguientes:

1.  Implemente la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Admite el servicio de **\_ \_ control \_ de tarifas de MF** . (Consulte [interfaces de servicio](service-interfaces.md)).
3.  Implemente la interfaz [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , que obtiene las velocidades de reproducción admitidas por el objeto.
4.  Implemente la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) , que obtiene o establece la velocidad de reproducción.

## <a name="media-sources"></a>Orígenes multimedia

Si un origen multimedia admite el control de velocidad, debe implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) y [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). De lo contrario, la sesión multimedia informa de que la velocidad de reproducción mínima y máxima es 1,0, independientemente de qué otros componentes se encuentran en la canalización.

La velocidad de reproducción no afecta a los tiempos de presentación de los ejemplos, por lo que el origen multimedia no debe ajustar sus marcas de tiempo. En su lugar, el reloj de la presentación se ejecuta a una velocidad mayor o menor. Para la reproducción inversa, el origen proporciona muestras en orden inverso, con marcas de tiempo decrecientes.

El parámetro *fThin* del método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) indica si el origen de medios debe *fino* el contenido. El ligero se aplica principalmente a las secuencias de vídeo. En el modo delgado, el origen quita los fotogramas Delta y entrega solo fotogramas clave. En velocidades de reproducción muy altas, el origen podría omitir algunos fotogramas clave (por ejemplo, entregarlos todos los demás fotogramas clave).

El origen no tiene que quitar ejemplos de audio en modo delgado. Sin embargo, con una velocidad de reproducción muy alta, el origen podría no ser capaz de leer los datos nough Fast para rellenar las solicitudes de ejemplo de la canalización. En ese caso, es posible que el origen tenga que quitar algunos datos de audio. Si es así, debe intentar proporcionar ejemplos de audio cercanos al tiempo a los ejemplos de vídeo (suponiendo que el origen tiene ambos tipos de secuencias).

Cuando una secuencia realiza una transición entre el modo delgado y no delgado, envía un evento [MEStreamThinMode](mestreamthinmode.md) .

Cuando el origen multimedia completa una llamada a [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate), envía el evento [MESourceRateChanged](mesourceratechanged.md) .

Durante la reproducción inversa:

-   El origen de medios ofrece ejemplos en orden inverso, sin ajustar las marcas de tiempo.
-   Las marcas de tiempo dentro de un flujo se deben reducir de monotónica.
-   El principio del contenido se considera el final de la secuencia. Después de que cada secuencia de medios entregue el primer ejemplo en la secuencia (es decir, tiempo de presentación = 0), envía el evento [MEEndOfStream](meendofstream.md) .

## <a name="media-foundation-transforms"></a>Media Foundation transformaciones

En general, una transformación de Media Foundation (MFT) no necesita compatibilidad explícita con el control de velocidad, a menos que la MFT implemente una reproducción inversa no simplificada.

Si una MFT no implementa la interfaz [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , la sesión multimedia asume lo siguiente:

-   La MFT admite las tarifas de reproducción de arbitrarias para la reproducción hacia delante, tanto las delgadas como las no reducidas.
-   La MFT admite la reproducción inversa simplificada, pero no admite la reproducción inversa no simplificada.

Si alguna de estas condiciones no se cumple, el MFT debe implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) y [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).

### <a name="reverse-playback"></a>Reproducción inversa

La sesión multimedia puede reproducirse en orden inverso incluso si una o varias transformaciones de la canalización no admiten explícitamente la reproducción inversa.

Si una MFT no expone la interfaz [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , la sesión multimedia utiliza el *ligero* para la reproducción inversa, como se indica a continuación:

-   La sesión multimedia envía fotogramas clave a la MFT de la manera habitual, llamando a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

-   La sesión multimedia quita los fotogramas Delta y los reemplaza con eventos [MEStreamTick](mestreamtick.md) .

-   Entre cada ejemplo, la sesión multimedia vacía la MFT para evitar errores causados por el hecho de que las marcas de tiempo están disminuyendo.

Un ejemplo se considera un fotograma clave si tiene el atributo [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) establecido en **true** y se considera un fotograma Delta si este atributo es **false** o no está establecido.

Si la MFT implementa [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport), la sesión multimedia usa esta interfaz para detectar si la MFT admite la reproducción inversa no simplificada. Si la MFT admite la reproducción inversa no simplificada, la sesión multimedia entrega todos los ejemplos, en orden inverso, sin quitar muestras ni vaciar la MFT.

Si una MFT admite la reproducción inversa no simplificada, debe implementar la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) . La sesión multimedia usará esta interfaz para notificar a la MFT cuando se produzca la reproducción inversa. En ese momento, el MFT debe estar preparado para que se reduzcan las marcas de tiempo y para que los fotogramas Delta lleguen en orden inverso. Normalmente, un descodificador necesitará almacenar en búfer muestras hasta que haya recibido un grupo completo de imágenes (GOP) y, a continuación, descodificar el GOP completo y generar los fotogramas descodificados en el orden correcto (inverso).

## <a name="media-sinks"></a>Receptores de medios

Si un receptor de medios tiene pocas *tasas*, la sesión multimedia supone que el receptor de medios puede controlar cualquier velocidad de reproducción. No es necesario que el receptor de medios implemente [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). (Un receptor de medios sin velocidad devuelve el MEDIASINK \_ Marca sin tasa del método [**IMFMediaSink:: GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) ).

De lo contrario, un receptor de medios debe implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) si puede controlar velocidades de reproducción distintas de 1,0.

Los receptores de medios no deben implementar [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Cuando cambia la velocidad de reproducción, el reloj de la presentación llama al método [**IMFClockStateSink:: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) del receptor de medios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de tasa](rate-control.md)
</dt> <dt>

[Búsqueda, avance rápido y reproducción inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



