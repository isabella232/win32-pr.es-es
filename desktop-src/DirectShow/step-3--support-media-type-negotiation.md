---
description: Paso 3.
ms.assetid: b2b5dafc-d38d-4ec3-a390-55229495b4f9
title: Paso 3. Compatibilidad con la negociación de tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3ff8539d0d7de2c9b7300ddb90ad86ca471710
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914126"
---
# <a name="step-3-support-media-type-negotiation"></a>Paso 3. Compatibilidad con la negociación de tipos de medios

Este es el paso 3 del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).

Cuando dos patillas se conectan, deben aceptar un tipo de medio para la conexión. El tipo de medio describe el formato de los datos. Sin el tipo de medio, un filtro podría proporcionar un tipo de datos, solo para que otro filtro lo trate como algo más.

El mecanismo básico para negociar tipos de medios es el método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) . El PIN de salida llama a este método en el PIN de entrada con un tipo de medio propuesto. El PIN de entrada acepta la conexión o la rechaza. Si rechaza la conexión, el PIN de salida puede intentar otro tipo de medio. Si no se encuentra ningún tipo adecuado, se produce un error en la conexión. Opcionalmente, el PIN de entrada puede anunciar una lista de tipos que prefiere, a través del método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) . El PIN de salida puede utilizar esta lista cuando propone tipos de medios, aunque no es necesario.

La clase **CTransformFilter** implementa un marco general para este proceso, como se indica a continuación:

-   El PIN de entrada no tiene tipos de medios preferidos. Se basa completamente en el filtro de nivel superior para proponer el tipo de medio. En el caso de los datos de vídeo, esto tiene sentido, ya que el tipo de medio incluye el tamaño de la imagen y la velocidad de fotogramas. Normalmente, esa información debe proporcionarse mediante un filtro de origen o un filtro de analizador de nivel superior. En el caso de los datos de audio, el conjunto de formatos posibles es más pequeño, por lo que puede ser práctico que el PIN de entrada ofrezca algunos tipos preferidos. En ese caso, invalide [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) en el PIN de entrada.
-   Cuando el filtro de nivel superior propone un tipo de medio, el PIN de entrada llama al método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) , que acepta o rechaza el tipo.
-   El PIN de salida no se conectará a menos que el PIN de entrada se conecte primero. Este comportamiento es habitual para los filtros de transformación. En la mayoría de los casos, el filtro debe determinar el tipo de entrada antes de que pueda establecer el tipo de salida.
-   Cuando el PIN de salida se conecta, tiene una lista de tipos de medios que se propone al filtro de bajada. Llama al método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) para generar esta lista. El PIN de salida también probará los tipos de medios que propone el filtro de nivel inferior.
-   Para comprobar si un tipo de salida determinado es compatible con el tipo de entrada, el PIN de salida llama al método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .

Los tres métodos **CTransformFilter** enumerados anteriormente son métodos virtuales puros, por lo que la clase derivada debe implementarlos. Ninguno de estos métodos pertenece a una interfaz COM; simplemente forman parte de la implementación proporcionada por las clases base.

En las secciones siguientes se describe cada método con más detalle:

-   [Paso 3A. Implementar el método CheckInputType](step-3a--implement-the-checkinputtype-method.md)
-   [Paso 3B. Implementar el método GetMediaType](step-3b--implement-the-getmediatype-method.md)
-   [Paso 3C. Implementar el método CheckTransform](step-3c--implement-the-checktransform-method.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo se conectan los filtros](how-filters-connect.md)
</dt> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



