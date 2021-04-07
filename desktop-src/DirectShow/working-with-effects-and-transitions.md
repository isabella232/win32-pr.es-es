---
description: Trabajar con efectos y transiciones
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Trabajar con efectos y transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003150"
---
# <a name="working-with-effects-and-transitions"></a>Trabajar con efectos y transiciones

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Los efectos modifican un solo clip, una pista o una composición. Las transiciones crean seques a partir de una pista o se comparan con otra.

Los [servicios de edición de DirectShow](directshow-editing-services.md) usan objetos de transformación de DirectX para sus transiciones de vídeo y efectos de vídeo. En el caso de las transiciones de vídeo, use cualquier objeto de transformación de DirectX de dos entradas 2D. Para los efectos de vídeo, use cualquier objeto de transformación de DirectX de una entrada 2D. Microsoft ya no admite el desarrollo de objetos de transformación de DirectX de terceros. Sin embargo, se proporcionan varios con DirectShow y otros se proporcionan con Microsoft Internet Explorer. Para obtener más información acerca de las transiciones proporcionadas con Internet Explorer, consulte [referencia de filtros y transiciones visuales](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).

En el caso de los efectos de audio, puede usar cualquier filtro de efecto de audio de DirectShow. DES también proporciona un [efecto de sobre de volumen](volume-envelope-effect.md) para establecer el volumen en un clip o pista. DES no es compatible con las transiciones de audio.

Esta sección contiene los siguientes temas:

-   [Agregar objetos Effect y Transition](adding-effect-and-transition-objects.md)
-   [Vista previa de efectos y transiciones](previewing-effects-and-transitions.md)
-   [Enumerar efectos y transiciones](enumerating-effects-and-transitions.md)
-   [Establecer propiedades en efectos y transiciones](setting-properties-on-effects-and-transitions.md)
-   [Dirección de la transición](transition-direction.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar servicios de edición de DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 
