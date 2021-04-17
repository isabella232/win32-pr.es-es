---
description: El atributo STOP especifica la hora de detención de un objeto, relativa al objeto primario.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: detener atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6deb3f2a422cb8100da32c0427caf6436e72fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688215"
---
# <a name="stop-attribute"></a>detener atributo

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `stop` atributo especifica la hora de detención de un objeto, relativa al objeto primario.

## <a name="possible-values"></a>Valores posibles

Debe ser una cadena con el formato *HH: mm: SS. FF* , donde *HH* = hours, *mm* = minutes, *SS* = seconds y *FF* = fracciones de segundo. Ejemplo: 1:04:30.512. Se pueden omitir las unidades iniciales. Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md), [**efecto**](effect-element.md), [**transición**](transition-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



