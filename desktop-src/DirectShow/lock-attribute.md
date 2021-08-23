---
description: El atributo lock especifica si se debe editar un objeto. Si el valor es TRUE, la aplicación debe tratar el objeto como bloqueado y no permitir cambios en ese objeto o sus secundarios. El valor predeterminado es FALSE.
ms.assetid: 1aa92665-ab3b-4f04-9e6b-905942c197ef
title: lock (Atributo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdd1718c25aab136219af436543df064bd8f68bb53ea15b00e09e6a18188c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502325"
---
# <a name="lock-attribute"></a>lock (Atributo)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `lock` atributo especifica si se debe editar un objeto. Si el valor es **TRUE,** la aplicación debe tratar el objeto como bloqueado y no permitir cambios en ese objeto o sus secundarios. El valor predeterminado es **FALSE**.

## <a name="possible-values"></a>Valores posibles

Valores posibles Los valores siguientes se definen como TRUE: y, Y, t, T, 1. Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetLocked**](iamtimelineobj-setlocked.md)
</dt> </dl>

 

 



