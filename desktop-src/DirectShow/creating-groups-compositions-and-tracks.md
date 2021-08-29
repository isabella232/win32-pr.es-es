---
description: Crear composiciones y pistas de grupos
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Crear composiciones y pistas de grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d0fa9812c3f7219882cc93be14f7ff4c0b1a8ae39f96d6798bdc93705cda8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908535"
---
# <a name="creating-groups-compositions-and-tracks"></a>Crear composiciones y pistas de grupos

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Los grupos, composiciones y pistas son las capas intermedias entre la escala de tiempo y los clips de origen. Se distinguen por el tipo de objeto que pueden contener.

-   Las pistas contienen objetos de origen.
-   Las composiciones contienen pistas y otras composiciones, pero no objetos de origen.
-   Los grupos son composiciones de nivel superior. Los grupos contienen composiciones y pistas, pero las composiciones no pueden contener grupos.
-   Una *pista virtual* es cualquier objeto que puede residir dentro de una composición o un grupo. Esto incluye pistas y composiciones.

Estos objetos exponen las interfaces siguientes:



| Interfaz                                                  | Expuesto por           |
|------------------------------------------------------------|----------------------|
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Pistas               |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Pistas, composiciones |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Composiciones, grupos |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Grupos               |



 

Estas interfaces contienen los métodos para agregar objetos a la escala de tiempo.

-   [**IAMTimeline::AddGroup:**](iamtimeline-addgroup.md)inserta un grupo en la escala de tiempo.
-   [**IAMTimelineComp::VTrackInsBefore:**](iamtimelinecomp-vtrackinsbefore.md)inserta una pista virtual en una composición o grupo.
-   [**IAMTimelineTrack::SrcAdd**](iamtimelinetrack-srcadd.md): inserta un origen en una pista.

Por ejemplo, el código siguiente inserta una nueva pista en un grupo. Como se muestra en la tabla anterior, un grupo se considera un tipo de composición y una pista es un tipo de pista virtual. Por lo tanto, para insertar la pista en el grupo, debe consultar el grupo para su interfaz **IAMTimelineComp** y llamar al método **IAMTimelineComp::VTrackInsBefore.**


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



El segundo parámetro de **VTrackInsBefore** especifica la prioridad de la pista virtual. Los niveles de prioridad comienzan en cero. Si especifica el valor –1, la pista virtual se inserta al final de la lista de prioridad. Si especifica un valor en el que ya hay una pista virtual, todo desde ese punto se desplaza hacia abajo en la lista en un nivel de prioridad. No inserte una pista virtual con una prioridad mayor que el número de pistas virtuales, ya que provocará un comportamiento indefinido.

Para eliminar un objeto permanentemente de la escala de tiempo, llame a [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md) en el objeto . Este método quita el objeto y todos sus elementos secundarios. Para quitar un objeto con el fin de reinsertarlo en otro lugar de la escala de tiempo, llame a [**IAMTimelineObj::Remove en su**](iamtimelineobj-remove.md) lugar. A **diferencia de RemoveAll,** este método no elimina los elementos secundarios del objeto. Para quitar todo de la escala de tiempo, [**llame a IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 



