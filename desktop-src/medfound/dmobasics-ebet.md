---
description: DMO Básico
ms.assetid: eaf453d2-69f8-432a-8a58-1ed70778f182
title: DMO Conceptos básicos (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24c7fb988d5e5225f292585a5562cce22e67c007175fa7ddc4cd86e40ec1d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742364"
---
# <a name="dmo-basics-microsoft-media-foundation"></a>DMO Conceptos básicos (Microsoft Media Foundation)

En este tema se proporciona una breve introducción a las DDO relacionadas con Windows códecs multimedia. Para obtener más información sobre las DDO, vea [Objetos multimedia de DirectX.](../directshow/directx-media-objects.md)

Un DMO es un objeto COM que transforma los datos. Le pasa datos y devuelve los datos transformados. En el caso de un codificador de códecs DMO, se introducen datos multimedia sin comprimir y el DMO proporciona datos multimedia comprimidos. La principal ventaja de usar las DDO es que todas implementan la misma interfaz base, [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), lo que simplifica el trabajo con ellos porque se puede usar el mismo objeto, independientemente del tipo de transformación que se realice.

Dado que hay variables implicadas en cualquier tipo de transformación de datos, la transformación de audio y vídeo debe tener en cuenta la amplia gama de configuraciones de medios posibles. Los Windows de audio y vídeo multimedia también admiten una serie de características especiales que debe poder configurar mediante el DMO.

En general, la información de variables que necesitan las DDO de códec para comprimir y descomprimir medios digitales se transmite de una de estas tres maneras:

-   Establezca el tipo de entrada en el DMO para transmitir las características del medio sin comprimir que se pasa a un codificador DMO y las características del medio comprimido que se pasa a un descodificador DMO.
-   Establezca el tipo de salida en el DMO para transmitir las características de los medios comprimidos que entrega un codificador DMO y las características de los medios sin comprimir que entrega un descodificador DMO.
-   Con los métodos de la **interfaz IPropertyBag,** configure otras opciones que admitan las distintas características de las DDO de códec como propiedades. **IPropertyBag es** una interfaz COM estándar que es compatible con todas las DDO de códec.

Además, algunas características de códec se administran mediante otras interfaces específicas de las DDO de códec. Estas interfaces se enumeran para cada códec en la sección [Objetos de códec](codecobjects.md).

Los tipos de entrada y salida son específicos de los flujos de entrada y salida. Cada secuencia representa una representación discreta del contenido. Por ejemplo, el codificador Windows Media Video DMO un único flujo de entrada y dos secuencias de salida. El flujo de entrada acepta ejemplos de vídeo sin comprimir. El primero de los dos flujos de salida proporciona ejemplos comprimidos; el otro proporciona ejemplos sin comprimir. Los ejemplos individuales de un flujo de salida representan el mismo contenido que los ejemplos correspondientes en la otra secuencia, pero cada secuencia entrega esos ejemplos en un formato diferente.

Cada secuencia (entrada o salida) admite uno o varios tipos de medios. Un tipo de medio, o formato, se describe mediante una estructura [**DMO \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Puede consultar el DMO los tipos admitidos por un flujo de salida llamando a [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype). Este método devuelve un tipo de salida válido (aunque en algunos casos parcialmente incompleto) para esa secuencia. Puede enumerar los tipos de medios admitidos para un flujo de salida realizando llamadas repetidas a **GetOutputType,** incrementando el parámetro de tipo con cada llamada. Cuando el índice de tipo que se pasa está fuera de los límites, el método **devuelve DMO E NO MORE \_ \_ \_ \_ ITEMS**. Los formatos de entrada se pueden enumerar de la misma manera mediante el [**método IMediaObject::GetInputType.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)

Los tipos enumerados por el DMO son solo los tipos "preferidos"; sin embargo, se pueden admiten otros tipos. Puede validar un tipo de salida llamando a [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). Use [**IMediaObject::SetInputType para**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) validar un tipo de entrada. Ambos métodos devolverán **DMO E TYPE NOT \_ \_ \_ \_ ACCEPTED** si la estructura [**DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) que ha pasado no es válida. Algunas DDO requieren que establezca un tipo de salida antes de enumerar los tipos de entrada. Las Windows de códec de vídeo y audio multimedia tienen entradas y salidas que tienen validación interdependiente. Es decir, el tipo de salida que establezca establecerá los criterios de validación para el tipo de entrada. También hay algunas propiedades que, cuando se establecen, modifican los tipos de entrada y salida válidos. Por este motivo, debe establecer todas las propiedades deseadas en el DMO antes de enumerar los tipos.

Cuando haya establecido los tipos de salida y entrada para el DMO, puede empezar a procesar ejemplos. Cada ejemplo de entrada se pasa al códec mediante una llamada a [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput)y el códec entrega cada muestra de salida al realizar una llamada a [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con DDO de códec](workingwithcodecdmos.md)
</dt> </dl>

 

 
