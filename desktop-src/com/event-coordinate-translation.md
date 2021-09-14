---
title: Traducción de coordenadas de eventos
description: Traducción de coordenadas de eventos
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c40a742ead8fc8d7e431c1caa5210f0978168cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973665"
---
# <a name="event-coordinate-translation"></a>Traducción de coordenadas de eventos

La especificación 96 para los controles requiere que las coordenadas pasadas para los eventos desencadenados por el control cambien de ser HIMETRIC a basarse en puntos. Este cambio hace que el evento pase coordenadas en línea con propiedades y métodos y, por tanto, la traducción de coordenadas ya no es responsabilidad del contenedor. Esto genera ciertos problemas de compatibilidad en los que un control genera eventos mediante una base de coordenadas que no espera; esto solo debe ser un problema en el que un contenedor de controles 96 hospeda un control anterior al 96 anterior al 96 como se muestra a continuación:

-   Cuando un contenedor anterior al 96 hospeda un control 96, el control presentará las coordenadas de evento como puntos, lo que no debería provocar ningún problema en el contenedor, ya que el contenedor debe reconocer el tipo de parámetro.
-   Cuando un contenedor 96 hospeda un control anterior al 96, el control presentará el contenedor con coordenadas y esperará que el contenedor se traduca en cualquier traducción necesaria. Sin embargo, el contenedor 96 esperará que un control se ajuste a la especificación de 96 controles y presente sus coordenadas como puntos. El control usa el [**método TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) en la interfaz [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) proporcionada por el contenedor de la misma manera que lo hace para que las propiedades y los métodos lo consigan.

Como resultado, el usuario de un contenedor 96 que hospeda controles previos a 96 deberá tener en cuenta que puede ser necesaria una traducción adicional de las coordenadas cuando se desencadenan eventos.

 

 




