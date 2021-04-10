---
description: Aspectos básicos de DMO
ms.assetid: eaf453d2-69f8-432a-8a58-1ed70778f182
title: Aspectos básicos de DMO (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b1aca2fcd7e70cf78e2e95135aee73c454b910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275118"
---
# <a name="dmo-basics-microsoft-media-foundation"></a>Aspectos básicos de DMO (Microsoft Media Foundation)

En este tema se proporciona una breve descripción de DMOs en relación con los códecs de Windows Media. Para obtener más información sobre DMOs, vea [objetos multimedia de DirectX](../directshow/directx-media-objects.md).

Un DMO es un objeto COM que transforma los datos. Le pasa datos y devuelve los datos transformados. En el caso de un codificador de códecs DMO, se especifican los datos de medios sin comprimir y DMO entrega datos de medios comprimidos. La principal ventaja de usar DMOs es que todos implementan la misma interfaz base, [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), que simplifica el trabajo con ellos, ya que puede usar el mismo objeto, independientemente del tipo de transformación que se realice.

Dado que hay variables implicadas en cualquier tipo de transformación de datos, la transformación audio y vídeo debe tener en cuenta la amplia gama de configuraciones de medios posibles. Los códecs de Windows Media Audio y vídeo también admiten una serie de características especiales que debe poder configurar mediante DMO.

En general, la información de variable que necesita el códec DMOs para comprimir y descomprimir los medios digitales se transmite de una de estas tres maneras:

-   Establezca el tipo de entrada en DMO para transmitir las características del medio sin comprimir que pasa a un codificador DMO y las características de los medios comprimidos que pasa a un descodificador DMO.
-   Establezca el tipo de salida en DMO para transmitir las características de los medios comprimidos entregados por un codificador DMO y las características de los medios sin comprimir entregados por un descodificador DMO.
-   Mediante los métodos de la interfaz **IPropertyBag** , configure otras opciones que admitan las distintas características del códec DMOs como propiedades. **IPropertyBag** es una interfaz com estándar que es compatible con todos los DMOs de códec.

Además, algunas características de códec se administran mediante otras interfaces específicas del códec DMOs. Estas interfaces se enumeran para cada códec en la sección [objetos de códec](codecobjects.md).

Los tipos de entrada y salida son específicos de los flujos de entrada y salida. Cada flujo representa una representación discreta del contenido. Por ejemplo, el codificador Windows Media Video DMO tiene un solo flujo de entrada y dos flujos de salida. El flujo de entrada acepta muestras de vídeo sin comprimir. El primero de los dos flujos de salida ofrece ejemplos comprimidos; el otro proporciona ejemplos sin comprimir. Los ejemplos individuales de un flujo de salida representan el mismo contenido que los ejemplos correspondientes en el otro flujo, pero cada flujo entrega esos ejemplos en un formato diferente.

Cada secuencia (entrada o salida) admite uno o varios tipos de medios. Un tipo de medio, o formato, se describe mediante una estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Puede consultar a DMO los tipos que son compatibles con un flujo de salida mediante una llamada a [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype). Este método devuelve un tipo de salida válido (aunque en algunos casos parcialmente incompleto) para esa secuencia. Puede enumerar los tipos de medios admitidos para un flujo de salida realizando llamadas repetidas a **GetOutputType**, incrementando el parámetro de tipo con cada llamada. Cuando el índice de tipo que se pasa está fuera de los límites, el método **devuelve \_ DMO \_ E \_ ningún \_ elemento más**. Los formatos de entrada se pueden enumerar de la misma manera mediante el método [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) .

Los tipos enumerados por DMO son solo los tipos "preferidos"; sin embargo, es posible que se admitan otros tipos. Puede validar un tipo de salida llamando a [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). Use [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) para validar un tipo de entrada. Ambos métodos devolverán el **\_ tipo DMO E \_ \_ no \_ aceptado** si la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) que pasó no es válida. Algunos DMOs requieren que se establezca un tipo de salida antes de enumerar los tipos de entrada. Los códecs de Windows Media Audio y vídeo DMOs tienen entradas y salidas que tienen validación interdependiente. Es decir, el tipo de salida que establezca establecerá los criterios de validación para el tipo de entrada. También hay algunas propiedades que, cuando se establecen, modifican los tipos de entrada y salida válidos. Por esta razón, debe establecer todas las propiedades deseadas en el DMO antes de enumerar los tipos.

Cuando haya establecido los tipos de entrada y salida para DMO, puede empezar a procesar ejemplos. Cada ejemplo de entrada se pasa al códec mediante una llamada a [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput), y el códec entrega cada ejemplo de salida cuando se realiza una llamada a [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
