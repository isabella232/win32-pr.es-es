---
description: El atributo mute especifica el estado de exclusión mutua del objeto.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: mute (Atributo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254271"
---
# <a name="mute-attribute"></a>mute (Atributo)

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `mute` atributo especifica el estado de exclusión mutua del objeto. Si el valor es **TRUE**, no se representan ni el objeto ni sus elementos secundarios. Si el valor es **FALSE**, se representa el objeto y sus elementos secundarios se representan según su propio estado de exclusión mutua. El valor predeterminado es **FALSE**.

## <a name="possible-values"></a>Valores posibles

Los valores siguientes se definen como TRUE: y, Y, t, T, 1. Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetMuted**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



