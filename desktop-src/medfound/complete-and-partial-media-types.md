---
description: En este tema se describe la diferencia entre los tipos de medios completos y los tipos de medios parciales.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Tipos de medios completos y parciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547390"
---
# <a name="complete-and-partial-media-types"></a>Tipos de medios completos y parciales

En este tema se describe la diferencia entre los tipos de medios completos y los tipos de medios parciales.

## <a name="complete-media-types"></a>Tipos de medios completos

Un tipo de medio *completo* es aquél que define por completo el formato del flujo multimedia. Dado un tipo de medio completo, un componente de canalización puede analizar los datos de secuencia asociados al tipo de medio, sin ambigüedad.

En el caso de los formatos sin comprimir, en los siguientes temas se definen los atributos necesarios para un tipo de medio completo:

-   Audio: [tipos de medios de audio sin comprimir](uncompressed-audio-media-types.md)
-   Vídeo: [tipos de medios de vídeo sin comprimir](uncompressed-video-media-types.md)

En el caso de las secuencias comprimidas (o *codificadas*), el códec define la definición de un tipo de medio completo. Sin embargo, si se conoce algún atributo de tipo sin comprimir para el flujo comprimido, estos valores deben incluirse en el tipo de medio del flujo comprimido. Por ejemplo, si se conoce el tamaño del marco, establezca el atributo de [**\_ tamaño de \_ marco \_ MF MT**](mf-mt-frame-size-attribute.md) en el tipo de medio, aunque técnicamente un flujo comprimido no tiene un tamaño de marco.

## <a name="partial-media-types"></a>Tipos de medios parciales

Faltan uno o varios de los atributos necesarios para un tipo de medio completo en un tipo de medio *parcial* . Al enumerar los posibles tipos de medios, un componente de Microsoft Media Foundation puede dejar un valor sin establecer para indicar que puede controlar cualquier valor. Por ejemplo, un procesador de vídeo podría dejar el atributo de [**\_ \_ \_ velocidad de fotogramas MF MT**](mf-mt-frame-rate-attribute.md) sin establecer, para indicar que puede controlar cualquier velocidad de fotogramas y realizará una conversión de velocidad de fotogramas si es necesario.

Si crea un tipo de medio parcial, debe incluir toda la información que sepa. Sin embargo, un tipo de medio no debe incluir información que sea incierto. Es mejor que falte información que equivocada.

Como mínimo, un tipo de medio parcial debe incluir solo dos atributos: [**\_ tipo de \_ versión \_ principal MF MT**](mf-mt-major-type-attribute.md) y [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md).

A veces Media Foundation componentes deben proporcionar tipos de medios completos:

-   Los orígenes multimedia deben proporcionar tipos de salida completos.
-   Los descodificadores deben proporcionar tipos de salida completos, una vez establecido el tipo de entrada. Antes de que se establezca el tipo de entrada, un descodificador podría proporcionar un tipo de salida parcial.
-   Los codificadores deben proporcionar tipos de entrada completos, una vez establecido el tipo de salida. Antes de que se establezca el tipo de salida, un codificador podría proporcionar un tipo de entrada parcial.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 



