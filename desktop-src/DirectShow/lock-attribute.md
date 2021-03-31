---
description: El atributo Lock especifica si se debe editar un objeto. Si el valor es TRUE, la aplicación debe tratar el objeto como bloqueado y no permitir los cambios en ese objeto o en sus elementos secundarios. El valor predeterminado es FALSE.
ms.assetid: 1aa92665-ab3b-4f04-9e6b-905942c197ef
title: Atributo Lock
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7716f047e0df47ffb5e84cb2de0e9fe345836b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806547"
---
# <a name="lock-attribute"></a>Atributo Lock

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `lock` atributo especifica si se debe editar un objeto. Si el valor es **true**, la aplicación debe tratar el objeto como bloqueado y no permitir los cambios en ese objeto o en sus elementos secundarios. El valor predeterminado es **FALSE**.

## <a name="possible-values"></a>Valores posibles

Valores posibles los valores siguientes se definen como TRUE: y, Y, t, T, 1. Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md), [**compuesto**](composite-element.md), [**efecto**](effect-element.md), [**Grupo**](group-element.md), [**escala de tiempo**](timeline-element.md), [**transición**](transition-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetLocked**](iamtimelineobj-setlocked.md)
</dt> </dl>

 

 



