---
description: Trabajar con efectos y transiciones
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Trabajar con efectos y transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272559"
---
# <a name="working-with-effects-and-transitions"></a>Trabajar con efectos y transiciones

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Los efectos modifican un solo clip, pista o composición. Las transiciones crean seques de una pista o composiciones a otra.

[DirectShow Editing Services usa](directshow-editing-services.md) objetos de transformación de DirectX para sus transiciones de vídeo y efectos de vídeo. Para las transiciones de vídeo, use cualquier objeto de transformación directX de dos entradas 2D. Para los efectos de vídeo, use cualquier objeto de transformación directX de una entrada 2D. Microsoft ya no admite el desarrollo de objetos de transformación de DirectX de terceros. Sin embargo, varios se proporcionan con DirectShow y otros se proporcionan con Microsoft Internet Explorer. Para obtener más información sobre las transiciones proporcionadas con Internet Explorer, vea [Visual Filters and Transitions Reference](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).

Para los efectos de audio, puede usar cualquier filtro DirectShow efecto de audio. DES también proporciona un [efecto de sobre de volumen](volume-envelope-effect.md) para establecer el volumen en una pista o clip. DES no admite transiciones de audio.

Esta sección contiene los siguientes temas:

-   [Agregar objetos de efecto y transición](adding-effect-and-transition-objects.md)
-   [Vista previa de efectos y transiciones](previewing-effects-and-transitions.md)
-   [Enumerar efectos y transiciones](enumerating-effects-and-transitions.md)
-   [Establecer propiedades en efectos y transiciones](setting-properties-on-effects-and-transitions.md)
-   [Dirección de transición](transition-direction.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DirectShow Editing Services](using-directshow-editing-services.md)
</dt> </dl>

 

 
