---
title: Traducción de coordenadas de eventos
description: Traducción de coordenadas de eventos
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c40a742ead8fc8d7e431c1caa5210f0978168cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778756"
---
# <a name="event-coordinate-translation"></a>Traducción de coordenadas de eventos

La especificación 96 para los controles requiere que las coordenadas pasadas para los eventos desencadenados por el control cambien de HIMETRIC a puntos basados en. Este cambio hace que el evento pase de coordenadas en línea con propiedades y métodos, por lo que la conversión de coordenadas ya no es responsabilidad del contenedor. Esto produce ciertos problemas de compatibilidad en los que un control desencadena eventos mediante una base de coordenadas que no espera, solo debe ser un problema en el que un contenedor de control de 96 hospeda un control anterior a 96 anterior como se indica a continuación:

-   Cuando un contenedor anterior a 96 hospeda un control 96, el control presentará las coordenadas de eventos como puntos, por lo que el contenedor no tendrá ningún problema porque el contenedor debe reconocer el tipo de parámetro.
-   Cuando un contenedor 96 hospeda un control anterior a 96, el control presentará el contenedor con coordenadas y esperará el contenedor a cualquier traducción necesaria. Sin embargo, el contenedor 96 esperará que un control se ajuste a la especificación de los controles 96 y presente sus coordenadas como puntos. El control usa el método [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) en la interfaz [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) proporcionada por el contenedor de la misma manera que para las propiedades y los métodos para lograrlo.

Como resultado, el usuario de un contenedor 96 que hospede controles anteriores a 96 tendrá que tener en cuenta que puede ser necesaria una traducción adicional de las coordenadas cuando se activan los eventos.

 

 




