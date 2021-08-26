---
description: En este tema se describe cómo los objetos de canalización personalizados pueden admitir velocidades de reproducción variables, incluida la reproducción inversa. Para obtener información sobre el uso del control de velocidad desde una aplicación, vea Control de frecuencia.
ms.assetid: 077678db-ca5a-423b-9430-93497113d639
title: Implementación del control de velocidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3ff90e7b1748efd4cfcff41244164d1d6a997b6208d3e46afa0cdae9aa6bba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114275"
---
# <a name="implementing-rate-control"></a>Implementación del control de velocidad

En este tema se describe cómo los objetos de canalización personalizados pueden admitir velocidades de reproducción variables, incluida la reproducción inversa. Para obtener información sobre el uso del control de velocidad desde una aplicación, vea [Control de frecuencia.](rate-control.md)

Este tema contiene las siguientes secciones:

-   [Orígenes multimedia](#media-sources)
-   [Media Foundation transformaciones](#media-foundation-transforms)
    -   [Reproducción inversa](#reverse-playback)
-   [Receptores multimedia](#media-sinks)
-   [Temas relacionados](#related-topics)

Si va a escribir un objeto Microsoft Media Foundation de canalización (un origen multimedia, una transformación o un receptor multimedia), es posible que tenga que admitir velocidades de reproducción variables. Para ello, implemente las interfaces siguientes:

1.  Implemente [**la interfaz IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
2.  Compatibilidad con **el servicio MF RATE CONTROL \_ \_ \_ SERVICE.** (Vea [Interfaces de servicio).](service-interfaces.md)
3.  Implemente [**la interfaz RECORDSETRateSupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) que obtiene las velocidades de reproducción admitidas por el objeto .
4.  Implemente [**la interfaz IMFRateControl,**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) que obtiene o establece la velocidad de reproducción.

## <a name="media-sources"></a>Orígenes multimedia

Si un origen de medios admite el control de velocidad, debe implementar [**TANTO ASERateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) como [**ATERATEControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). De lo contrario, la sesión multimedia informa de que la velocidad de reproducción mínima y máxima es 1,0, independientemente de qué otros componentes estén en la canalización.

La velocidad de reproducción no afecta a los tiempos de presentación de los ejemplos, por lo que el origen del medio no debe ajustar sus marcas de tiempo. En su lugar, el reloj de presentación se ejecuta a una velocidad más rápida o más lenta. Para la reproducción inversa, el origen entrega muestras en orden inverso, con marcas de tiempo decrecientes.

El *parámetro fThin* del método [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) indica si el origen de medios *debe ajustar el* contenido. La simplificación se aplica principalmente a las secuencias de vídeo. En el modo fino, el origen quita los fotogramas delta y entrega solo fotogramas clave. A velocidades de reproducción muy altas, el origen podría omitir algunos fotogramas clave (por ejemplo, entregar cada otro fotograma clave).

El origen no tiene que quitar muestras de audio en modo fino. Sin embargo, con velocidades de reproducción muy altas, es posible que el origen no pueda leer los datos rápidamente para rellenar las solicitudes de ejemplo de la canalización. En ese caso, es posible que el origen tenga que quitar algunos datos de audio. Si es así, debe intentar entregar muestras de audio cercanas a tiempo a los ejemplos de vídeo (suponiendo que el origen tenga ambos tipos de secuencia).

Cuando una secuencia pasa entre el modo thinned y el no thinned, envía un [evento MEStreamThinMode.](mestreamthinmode.md)

Cuando el origen multimedia completa una llamada a [**SetRate,**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)envía el [evento MESourceRateChanged.](mesourceratechanged.md)

Durante la reproducción inversa:

-   El origen multimedia entrega muestras en orden inverso, sin ajustar las marcas de tiempo.
-   Las marcas de tiempo dentro de una secuencia deben reducirse de forma monónica.
-   El principio del contenido se considera el final de la secuencia. Una vez que cada secuencia multimedia entrega el primer ejemplo de la secuencia (es decir, el tiempo de presentación = 0), envía el [evento MEEndOfStream.](meendofstream.md)

## <a name="media-foundation-transforms"></a>Media Foundation transformaciones

En general, una Media Foundation transformación de datos (MFT) no necesita compatibilidad explícita con el control de velocidad, a menos que MFT implemente la reproducción inversa no fina.

Si un MFT no implementa la interfaz [**IMFRateSupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) la sesión multimedia asume lo siguiente:

-   El MFT admite tasas de reproducción a la baja para la reproducción hacia delante, tanto finas como no finas.
-   MFT admite la reproducción inversa fina, pero no admite la reproducción inversa no fina.

Si alguna de estas condiciones no es verdadera, el MFT debe implementar [**LAFTRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) y [**ELCONTROL DE LA VELOCIDAD DE LA ACTIVIDAD.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)

### <a name="reverse-playback"></a>Reproducción inversa

La sesión multimedia puede reproducirse en orden inverso aunque una o varias transformaciones de la canalización no admitan explícitamente la reproducción inversa.

Si un MFT no expone la interfaz [**IMFRateSupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) la sesión multimedia usa la simplificación para la reproducción inversa, como se muestra a continuación: 

-   La sesión multimedia envía fotogramas clave al MFT de la manera habitual, llamando a [**ASETransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

-   La sesión multimedia quita los fotogramas delta y los reemplaza por [eventos MEStreamTick.](mestreamtick.md)

-   Entre cada ejemplo, la sesión multimedia vacía el MFT, para evitar errores causados por el hecho de que las marcas de tiempo están disminuyendo.

Un ejemplo se considera un fotograma clave si tiene el atributo [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) establecido en **TRUE** y se considera un marco delta si este atributo es **FALSE** o no está establecido.

Si MFT implementa [**LARATESupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)la sesión multimedia usa esta interfaz para detectar si MFT admite la reproducción inversa no fina. Si MFT admite la reproducción inversa no fina, la sesión multimedia entrega todas las muestras, en orden inverso, sin quitar muestras ni vaciar el MFT.

Si un MFT admite la reproducción inversa no fina, debe implementar la interfaz [**DECONTROLRATECONTROL.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) La sesión multimedia usará esta interfaz para notificar al MFT cuándo se produce la reproducción inversa. En ese momento, el MFT debe estar preparado para que las marcas de tiempo disminuyan y para que los marcos delta lleguen en orden inverso. Normalmente, un descodificador tendrá que almacenar en búfer las muestras hasta que haya recibido un grupo completo de imágenes (GOP) y, a continuación, descodificar todo el GOP y generar los marcos descodificados en el orden correcto (inverso).

## <a name="media-sinks"></a>Receptores multimedia

Si un receptor multimedia no tiene *velocidad,* la sesión multimedia asume que el receptor de medios puede controlar cualquier velocidad de reproducción. No es necesario que el receptor multimedia [**implemente LARrateSupport.**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) (Un receptor de medios sin velocidad devuelve MEDIASINK \_ Marca RATELESS del [**método IMFMediaSink::GetCharacteristics).**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)

De lo contrario, un receptor multimedia debe implementar [**LARATESupport si**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) puede controlar las velocidades de reproducción que no son 1.0.

Los receptores de medios no deben [**implementar EL CONTROL DE TASACIÓN.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) Cuando cambia la velocidad de reproducción, el reloj de presentación llama al método [**IMFClockStateSink::OnClockSetRate del**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) receptor multimedia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de velocidad](rate-control.md)
</dt> <dt>

[Búsqueda, Inserción rápida y reproducción inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



