---
description: En este tema se describe la diferencia entre los tipos de medios completos y los tipos de medios parciales.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Tipos de medios completos y parciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104f5509835c1f5f179c61b90f2c5f58636d022f4e5710b4b941e0819585fe85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958795"
---
# <a name="complete-and-partial-media-types"></a>Tipos de medios completos y parciales

En este tema se describe la diferencia entre los tipos de medios completos y los tipos de medios parciales.

## <a name="complete-media-types"></a>Tipos de medios completos

Un *tipo* de medio completo es aquel que define completamente el formato de la secuencia multimedia. Dado un tipo de medio completo, un componente de canalización puede analizar los datos de flujo asociados al tipo de medio, sin ambigüedad.

En el caso de los formatos sin comprimir, los temas siguientes definen los atributos necesarios para un tipo de medio completo:

-   Audio: [tipos de medios de audio sin comprimir](uncompressed-audio-media-types.md)
-   Vídeo: [Tipos de medios de vídeo sin comprimir](uncompressed-video-media-types.md)

Para secuencias comprimidas *(o* codificadas), el códec define la definición de un tipo de medio completo. Sin embargo, si se conoce algún atributo de tipo sin comprimir para la secuencia comprimida, estos valores deben incluirse en el tipo de medio para la secuencia comprimida. Por ejemplo, si se conoce el tamaño del fotograma, establezca el atributo [**MF \_ MT FRAME \_ \_ SIZE**](mf-mt-frame-size-attribute.md) en el tipo de medio, aunque técnicamente una secuencia comprimida no tenga un tamaño de fotograma.

## <a name="partial-media-types"></a>Tipos de medios parciales

Un *tipo* de medio parcial carece de uno o varios de los atributos necesarios para un tipo de medio completo. Al enumerar posibles tipos de medios, un componente Microsoft Media Foundation puede dejar un valor sin establecer, para indicar que puede controlar cualquier valor. Por ejemplo, un procesador de vídeo podría dejar sin establecer el atributo [**MF \_ MT FRAME \_ \_ RATE**](mf-mt-frame-rate-attribute.md) para indicar que puede controlar cualquier velocidad de fotogramas y realizará una conversión de velocidad de fotogramas si es necesario.

Si crea un tipo de medio parcial, debe incluir toda la información que sepa. Sin embargo, un tipo de medio no debe incluir información que no sea segura. Es mejor que falte información que incorrecta.

Como mínimo, un tipo de medio parcial debe incluir solo dos atributos: [**MF \_ MT MAJOR \_ \_ TYPE**](mf-mt-major-type-attribute.md) y [**MF MT \_ \_ SUBTYPE**](mf-mt-subtype-attribute.md).

A Media Foundation componentes deben proporcionar tipos de medios completos:

-   Los orígenes multimedia deben proporcionar tipos de salida completos.
-   Los descodificadores deben proporcionar tipos de salida completos, una vez establecido el tipo de entrada. Antes de establecer el tipo de entrada, un descodificador podría proporcionar un tipo de salida parcial.
-   Los codificadores deben proporcionar tipos de entrada completos, una vez establecido el tipo de salida. Antes de establecer el tipo de salida, un codificador podría proporcionar un tipo de entrada parcial.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 



