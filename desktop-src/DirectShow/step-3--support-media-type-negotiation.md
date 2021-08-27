---
description: Implemente la compatibilidad con la negociación de tipos de medios como parte de la escritura de un filtro de transformación. El tipo de medio describe el formato de los datos.
ms.assetid: b2b5dafc-d38d-4ec3-a390-55229495b4f9
title: Paso 3. Compatibilidad con la negociación de tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1558d5b1a7fd9db41fef7e5a9818d93c306f4f15f42099d4cb88f66b34725660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051475"
---
# <a name="step-3-support-media-type-negotiation"></a>Paso 3. Compatibilidad con la negociación de tipos de medios

Este es el paso 3 del tutorial Escribir [filtros de transformación](writing-transform-filters.md).

Cuando se conectan dos pines, deben coincidir en un tipo de medio para la conexión. El tipo de medio describe el formato de los datos. Sin el tipo de medio, un filtro podría entregar un tipo de datos, solo para que otro filtro los trate como otra cosa.

El mecanismo básico para negociar tipos de medios es [**el método IPin::ReceiveConnection.**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) El pin de salida llama a este método en el pin de entrada con un tipo de medio propuesto. El pin de entrada acepta la conexión o la rechaza. Si rechaza la conexión, el pin de salida puede probar otro tipo de medio. Si no se encuentra ningún tipo adecuado, se produce un error en la conexión. Opcionalmente, el pin de entrada puede anunciar una lista de tipos que prefiera, a través del método [**IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) El pin de salida puede usar esta lista cuando propone tipos de medios, aunque no es necesario.

La **clase CTransformFilter** implementa un marco general para este proceso, como se muestra a continuación:

-   El pin de entrada no tiene tipos de medios preferidos. Se basa completamente en el filtro ascendente para proponer el tipo de medio. En el caso de los datos de vídeo, esto tiene sentido, ya que el tipo de medio incluye el tamaño de la imagen y la velocidad de fotogramas. Normalmente, esa información debe proporcionarse mediante un filtro de origen ascendente o un filtro de analizador. En el caso de los datos de audio, el conjunto de formatos posibles es más pequeño, por lo que puede resultar práctico que el pin de entrada ofrezca algunos tipos preferidos. En ese caso, [**invalide CBasePin::GetMediaType en**](cbasepin-getmediatype.md) el pin de entrada.
-   Cuando el filtro ascendente propone un tipo de medio, el pin de entrada llama al método [**CTransformFilter::CheckInputType,**](ctransformfilter-checkinputtype.md) que acepta o rechaza el tipo.
-   El pin de salida no se conectará a menos que el pin de entrada esté conectado primero. Este comportamiento es típico de los filtros de transformación. En la mayoría de los casos, el filtro debe determinar el tipo de entrada para poder establecer el tipo de salida.
-   Cuando el pin de salida se conecta, tiene una lista de tipos de medios que propone al filtro de nivel inferior. Llama al [**método CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) para generar esta lista. El pin de salida también probará los tipos de medios que el filtro de nivel inferior propone.
-   Para comprobar si un tipo de salida determinado es compatible con el tipo de entrada, el pin de salida llama al [**método CTransformFilter::CheckTransform.**](ctransformfilter-checktransform.md)

Los tres **métodos CTransformFilter enumerados** anteriormente son métodos virtuales puros, por lo que la clase derivada debe implementarlos. Ninguno de estos métodos pertenece a una interfaz COM; simplemente forman parte de la implementación proporcionada por las clases base.

En las secciones siguientes se describe cada método con más detalle:

-   [Paso 3A. Implementación del método CheckInputType](step-3a--implement-the-checkinputtype-method.md)
-   [Paso 3B. Implementación del método GetMediaType](step-3b--implement-the-getmediatype-method.md)
-   [Paso 3C. Implementación del método CheckTransform](step-3c--implement-the-checktransform-method.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo se Conectar](how-filters-connect.md)
</dt> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



