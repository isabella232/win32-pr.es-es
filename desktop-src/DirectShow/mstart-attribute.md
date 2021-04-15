---
description: El atributo mstart especifica la hora de inicio de un clip, relativa al archivo multimedia original.
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: Atributo mstart
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb637dd0c5f924a593370ceb0fb205adf5d589ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494321"
---
# <a name="mstart-attribute"></a>Atributo mstart

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `mstart` atributo especifica la hora de inicio de un clip, relativa al archivo multimedia original.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valores posibles

Debe ser una cadena con el formato *HH: mm: SS. FF* , donde *HH* = hours, *mm* = minutes, *SS* = seconds y *FF* = fracciones de segundo. Ejemplo: 1:04:30.512. Se pueden omitir las unidades iniciales. Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



