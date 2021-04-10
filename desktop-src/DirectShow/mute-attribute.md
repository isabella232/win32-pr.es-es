---
description: El atributo MUTE especifica el estado de silencio del objeto.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: silenciar atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152462"
---
# <a name="mute-attribute"></a>silenciar atributo

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `mute` atributo especifica el estado de silencio del objeto. Si el valor es **true**, no se representan el objeto ni sus elementos secundarios. Si el valor es **false**, el objeto se representa y sus elementos secundarios se representan según su propio estado de silencio. El valor predeterminado es **FALSE**.

## <a name="possible-values"></a>Valores posibles

Los siguientes valores se definen como TRUE: y, Y, t, T, 1. Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md), [**compuesto**](composite-element.md), [**efecto**](effect-element.md), [**Grupo**](group-element.md), [**escala de tiempo**](timeline-element.md), [**transición**](transition-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetMuted**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



