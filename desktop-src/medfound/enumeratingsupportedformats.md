---
description: Configuración de códecs DMOs
ms.assetid: 431b33f1-ceb0-4f1b-a9f2-72e88b63f973
title: Configuración de códecs DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 564c0e6c566d9f583a495238f3ea6f0716d7adde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496816"
---
# <a name="configuring-codec-dmos"></a>Configuración de códecs DMOs

En este tema se describe el proceso de configuración del códec DMOs. Cada códec tiene procedimientos específicos, pero la información común a todos se describe aquí.

## <a name="configuring-dmo-inputs-and-outputs"></a>Configuración de entradas y salidas de DMO

Cada DMO admite tipos de entrada y salida concretos. Puede recuperar los tipos admitidos para las entradas y salidas llamando a [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) para las entradas y [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) para las salidas. Puede enumerar los formatos admitidos realizando llamadas repetidas a cualquier método, incrementando el índice de tipo con cada llamada. Cuando el índice supera el del tipo compatible final, la llamada devuelve DMO \_ E \_ no hay \_ más \_ elementos.

En el caso de los códecs de vídeo, solo se enumera un tipo de salida o de entrada para un subtipo de medio determinado. En el caso de los códecs de audio, se enumera cada tipo compatible individual. Para obtener más información sobre los tipos admitidos para códecs individuales, consulte [trabajar con audio](workingwithaudio.md) y [trabajar con vídeo](workingwithvideo.md).

Después de configurar los tipos de medios para los flujos de entrada y salida, establézcalo llamando a [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) y [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) respectivamente. Ambos métodos devuelven **el \_ tipo DMO E \_ \_ no \_ aceptado** si el tipo especificado no es válido.

## <a name="configuring-the-codec-dmos-for-encoding"></a>Configuración del códec DMOs para la codificación

Todos los códecs de Windows Media Audio y vídeo admiten una variedad de características de codificación. Estas características se configuran generalmente mediante el establecimiento de propiedades en DMO mediante los métodos de la interfaz **IPropertyBag** . Algunas propiedades se configuran mediante interfaces de códec especializadas. Estas interfaces se enumeran para cada códec en la sección [objetos de códec](codecobjects.md).

El orden general de las operaciones para configurar DMO de codificación es el siguiente:

1.  Configure las características del códec según sea necesario mediante los métodos de **IPropertyBag**.
2.  Use las interfaces de códec DMO para configurar características adicionales, si es necesario.
3.  Configure los tipos de entrada y salida. El orden en que deben configurarse los tipos varía en los códecs individuales. Para obtener más información, consulte [trabajar con audio](workingwithaudio.md) y [trabajar con vídeo](workingwithvideo.md).

## <a name="configuring-the-codec-dmos-for-decoding"></a>Configuración del códec DMOs para la descodificación

La descodificación es más sencilla que la codificación, ya que se admiten menos características de descodificador.

El orden general de las operaciones para configurar una DMO de descodificación es el siguiente:

1.  Configure las características del descodificador según sea necesario mediante los métodos de **IPropertyBag**.
2.  Establezca el tipo de entrada en el tipo que se usa para la salida del codificador.
3.  Configure el tipo de salida. Los tipos de salida admitidos son diferentes para las distintas entradas.

> [!Note]  
> Es importante usar el mismo tipo de medio para la entrada del descodificador que se usó para la salida del codificador. Esto se debe a que los códecs de Windows Media Audio y vídeo usan formatos de medios con datos adicionales. Estos datos se anexan a la estructura a la que apunta el miembro **pbFormat** de la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) (normalmente [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))). Para algunos tipos, los datos adicionales forman parte del tipo de salida del codificador enumerado. Otros tipos requieren que anexe estos datos manualmente. Sin los datos de formato extendido, no se puede descodificar el contenido comprimido.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
