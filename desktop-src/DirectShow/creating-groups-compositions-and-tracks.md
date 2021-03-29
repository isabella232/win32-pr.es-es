---
description: Creación de composiciones y seguimientos de grupos
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Creación de composiciones y seguimientos de grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906856"
---
# <a name="creating-groups-compositions-and-tracks"></a>Creación de composiciones y seguimientos de grupos

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Los grupos, las composiciones y las pistas son las capas intermedias entre la escala de tiempo y los clips de origen. Se distinguen por el tipo de objeto que pueden contener.

-   Las pistas contienen objetos de origen.
-   Las composiciones contienen pistas y otras composiciones, pero no objetos de origen.
-   Los grupos son composiciones de nivel superior. Los grupos contienen composiciones y pistas, pero las composiciones no pueden contener grupos.
-   Una *pista virtual* es cualquier objeto que puede residir dentro de una composición o un grupo. Esto incluye las pistas y las composiciones.

Estos objetos exponen las interfaces siguientes:



| Interfaz                                                  | Expuesto por           |
|------------------------------------------------------------|----------------------|
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Pistas               |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Pistas, composiciones |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Composiciones, grupos |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Grupos               |



 

Estas interfaces contienen los métodos para agregar objetos a la escala de tiempo.

-   [**IAMTimeline:: addgroup**](iamtimeline-addgroup.md): inserta un grupo en la escala de tiempo.
-   [**IAMTimelineComp:: VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): inserta una pista virtual en una composición o un grupo.
-   [**IAMTimelineTrack:: SrcAdd**](iamtimelinetrack-srcadd.md): inserta un origen en una pista.

Por ejemplo, el código siguiente inserta una nueva pista en un grupo. Como se muestra en la tabla anterior, un grupo se considera un tipo de composición y una pista es un tipo de pista virtual. Por lo tanto, para insertar la pista en el grupo, debe consultar el grupo de su interfaz **IAMTimelineComp** y llamar al método **IAMTimelineComp:: VTrackInsBefore** .


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



El segundo parámetro de **VTrackInsBefore** especifica la prioridad de la pista virtual. Los niveles de prioridad comienzan en cero. Si especifica el valor-1, se insertará la pista virtual al final de la lista de prioridades. Si especifica un valor en el que ya existe una pista virtual, todo desde ese punto se desplaza hacia abajo en la lista en un nivel de prioridad. No inserte una pista virtual con una prioridad mayor que el número de pistas virtuales, porque provocará un comportamiento no definido.

Para eliminar un objeto de forma permanente de la escala de tiempo, llame a [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md) en el objeto. Este método quita el objeto y todos sus elementos secundarios. Para quitar un objeto con el fin de volver a insertarlo en otra parte de la escala de tiempo, llame a [**IAMTimelineObj:: Remove**](iamtimelineobj-remove.md) en su lugar. A diferencia de **RemoveAll**, este método no elimina los elementos secundarios del objeto. Para quitar todo de la escala de tiempo, llame a [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 



