---
description: Objetos Timeline
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Objetos Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669957"
---
# <a name="timeline-objects"></a>Objetos Timeline

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Cada tipo de objeto de la escala de tiempo (origen, seguimiento, efecto, etc.) es un objeto COM distinto. Sin embargo, una aplicación no las crea mediante la función **CoCreateInstance** . En su lugar, llama al método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) . Este método crea un objeto del tipo solicitado, lo inicializa y devuelve un puntero al objeto. Para obtener más información, consulte [crear una escala de tiempo](constructing-a-timeline.md).

Cada objeto Timeline expone la interfaz [**IAMTimelineObj**](iamtimelineobj.md) . Además, los distintos tipos de objetos admiten sus propias interfaces especializadas:

-   Origen: [ **IAMTimelineSrc**](iamtimelinesrc.md)
-   Seguimiento: [ **IAMTimelineTrack**](iamtimelinetrack.md)
-   Composición: [ **IAMTimelineComp**](iamtimelinecomp.md)
-   Grupo: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)
-   Efecto: [ **IAMTimelineEffect**](iamtimelineeffect.md)
-   Transición: [ **IAMTimelineTrans**](iamtimelinetrans.md)

Tenga en cuenta que los grupos son un tipo de composición, por lo que admiten [**IAMTimelineComp**](iamtimelinecomp.md), así como su propia interfaz [**IAMTimelineGroup**](iamtimelinegroup.md) .

Además de las interfaces enumeradas anteriormente, los objetos Timeline exponen otras interfaces secundarias. Estas interfaces determinan las relaciones entre los tipos de objeto.



| Interfaz                                                  | Significado                                                                                                       | Expuesto por                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | El objeto es una pista virtual. Las pistas virtuales pueden residir dentro de composiciones y contener otros objetos de escala de tiempo. | Composición, seguimiento                |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | El objeto puede tener efectos.                                                                                  | Composición, seguimiento, origen        |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | El objeto puede tener transiciones.                                                                              | Composición, seguimiento                |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | El objeto se puede dividir en dos objetos.                                                                     | Seguimiento, origen, efecto, transición |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de los componentes de la escala de tiempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



