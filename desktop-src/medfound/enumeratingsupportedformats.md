---
description: Configuración de las DDO de códecs
ms.assetid: 431b33f1-ceb0-4f1b-a9f2-72e88b63f973
title: Configuración de las DDO de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4040c0a16c0311d14b0553336e1d9b70a7a6c1fd28a0f01277c955eea55ec7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958335"
---
# <a name="configuring-codec-dmos"></a>Configuración de las DDO de códecs

En este tema se describe el proceso de configuración de las DDO de códec. Cada códec tiene procedimientos específicos, pero la información común a todos se describe aquí.

## <a name="configuring-dmo-inputs-and-outputs"></a>Configuración de DMO entradas y salidas

Cada DMO admite tipos de entrada y salida específicos. Puede recuperar los tipos admitidos para las entradas y salidas llamando a [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) para las entradas e [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) para las salidas. Puede enumerar los formatos admitidos realizando llamadas repetidas a cualquiera de los métodos, incrementando el índice de tipo con cada llamada. Cuando el índice supera el del tipo final admitido, la llamada devuelve DMO \_ E \_ NO MORE \_ \_ ITEMS.

Para los códecs de vídeo, solo se enumera un tipo de salida o un tipo de entrada para un subtipo de medio determinado. Para los códecs de audio, se enumera cada tipo admitido individual. Para obtener más información sobre los tipos admitidos para códecs individuales, vea [Trabajar con audio](workingwithaudio.md) y Trabajar con [vídeo.](workingwithvideo.md)

Después de configurar los tipos de medios para los flujos de entrada y salida, configúrelos llamando a [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject::SetOutputType,**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) respectivamente. Ambos métodos devuelven **DMO E TYPE NOT \_ \_ \_ \_ ACCEPTED** si el tipo especificado no es válido.

## <a name="configuring-the-codec-dmos-for-encoding"></a>Configuración de las DMO de códecs para codificación

Todos los códecs Windows audio multimedia y vídeo admiten una variedad de características de codificación. Estas características se configuran generalmente estableciendo propiedades en el DMO mediante los métodos de la **interfaz IPropertyBag.** Algunas propiedades se configuran mediante interfaces de códec especializadas. Estas interfaces se enumeran para cada códec en la sección [Objetos de códec](codecobjects.md).

El orden general de las operaciones para configurar una codificación DMO es el siguiente:

1.  Configure las características de códec como desee mediante los métodos **de IPropertyBag**.
2.  Use el códec DMO interfaces para configurar características adicionales, si es necesario.
3.  Configure los tipos de entrada y salida. El orden en el que se deben configurar los tipos varía en función de los códecs individuales. Para obtener más información, [vea Trabajar con audio](workingwithaudio.md) y Trabajar con [vídeo.](workingwithvideo.md)

## <a name="configuring-the-codec-dmos-for-decoding"></a>Configuración de las DMO de códecs para la decoding

La descodificación es más sencilla que la codificación, ya que se admiten menos características de descodificador.

El orden general de las operaciones para configurar un DMO es el siguiente:

1.  Configure las características de descodificador como desee mediante los métodos **de IPropertyBag**.
2.  Establezca el tipo de entrada en el tipo utilizado para la salida del codificador.
3.  Configure el tipo de salida. Los tipos de salida admitidos son diferentes para diferentes entradas.

> [!Note]  
> Es importante usar el mismo tipo de medio para la entrada del descodificador que se usó para la salida del codificador. Esto se debe a que los códecs Windows audio multimedia y vídeo usan formatos multimedia con datos adicionales. Estos datos se anexan a la estructura a la que apunta el miembro **pbFormat** de la estructura [**DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) (normalmente [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**WAVEFORMATEX).**](/previous-versions/dd757713(v=vs.85)) Para algunos tipos, los datos adicionales forman parte del tipo de salida del codificador enumerado. Otros tipos requieren que se anexe estos datos manualmente. Sin los datos de formato extendido, no se puede descodificar el contenido comprimido.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con DDO de códec](workingwithcodecdmos.md)
</dt> </dl>

 

 
