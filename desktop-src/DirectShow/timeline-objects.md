---
description: Objetos de escala de tiempo
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Objetos de escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbcf3496770dee7664e08ffabe6537356c7b37ad13abee1dce149698748745e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072309"
---
# <a name="timeline-objects"></a>Objetos de escala de tiempo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Cada tipo de objeto de la escala de tiempo (origen, seguimiento, efecto, etc.) es un objeto COM distinto. Sin embargo, una aplicación no los crea mediante la **función CoCreateInstance.** En su lugar, llama al [**método IAMTimeline::CreateEmptyNode.**](iamtimeline-createemptynode.md) Este método crea un objeto del tipo solicitado, lo inicializa y devuelve un puntero al objeto . Para obtener más información, vea [Construcción de una escala de tiempo.](constructing-a-timeline.md)

Cada objeto de escala de tiempo expone [**la interfaz IAMTimelineObj.**](iamtimelineobj.md) Además, los distintos tipos de objeto admiten sus propias interfaces especializadas:

-   Origen: [ **IAMTimelineSrc**](iamtimelinesrc.md)
-   Seguimiento: [ **IAMTimelineTrack**](iamtimelinetrack.md)
-   Composición: [ **IAMTimelineComp**](iamtimelinecomp.md)
-   Grupo: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)
-   Efecto: [ **IAMTimelineEffect**](iamtimelineeffect.md)
-   Transición: [ **IAMTimelineTrans**](iamtimelinetrans.md)

Tenga en cuenta que los grupos son un tipo de composición, por lo que admiten [**IAMTimelineComp**](iamtimelinecomp.md), así como su propia [**interfaz IAMTimelineGroup.**](iamtimelinegroup.md)

Además de las interfaces enumeradas anteriormente, los objetos de escala de tiempo exponen otras interfaces secundarias. Estas interfaces determinan las relaciones entre los tipos de objeto.



| Interfaz                                                  | Significado                                                                                                       | Expuesto por                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | El objeto es una pista virtual. Las pistas virtuales pueden residir dentro de composiciones y contener otros objetos de escala de tiempo. | Composition, Track                |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | El objeto puede tener efectos.                                                                                  | Composition, Track, Source        |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | El objeto puede tener transiciones.                                                                              | Composition, Track                |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | El objeto se puede dividir en dos objetos .                                                                     | Seguimiento, origen, efecto, transición |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de los componentes de escala de tiempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



