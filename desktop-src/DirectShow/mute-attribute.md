---
description: El atributo mute especifica el estado de exclusión mutua del objeto.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: mute (Atributo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d89632e632ec4dbf0fe76a915e073baa769044fa1eaad455c16dd3065dc1c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791045"
---
# <a name="mute-attribute"></a>mute (Atributo)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `mute` atributo especifica el estado de exclusión mutua del objeto. Si el valor es **TRUE**, no se representan ni el objeto ni sus elementos secundarios. Si el valor es **FALSE**, se representa el objeto y sus elementos secundarios se representan según su propio estado de exclusión mutua. El valor predeterminado es **FALSE**.

## <a name="possible-values"></a>Valores posibles

Los valores siguientes se definen como TRUE: y, Y, t, T, 1. Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).

## <a name="applies-to"></a>Se aplica a

[**clip,**](clip-element.md) [**composite ,**](composite-element.md) [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetMuted**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



