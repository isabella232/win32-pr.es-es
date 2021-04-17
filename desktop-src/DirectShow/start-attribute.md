---
description: El atributo Start especifica la hora de inicio de un objeto, relativa al objeto primario.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: Atributo de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b377d0d83c86b981400a784904cf0423f0cca20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688227"
---
# <a name="start-attribute"></a>Atributo de inicio

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `start` atributo especifica la hora de inicio de un objeto, relativa al objeto primario.

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

 

 



