---
description: El atributo Time especifica la hora a la que un parámetro presupone un nuevo valor, en relación con el inicio de la transición o efecto.
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: Atributo de hora
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279507"
---
# <a name="time-attribute"></a>Atributo de hora

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `time` atributo especifica la hora a la que un parámetro presupone un nuevo valor, en relación con el inicio de la transición o efecto.

## <a name="possible-values"></a>Valores posibles

Debe ser una cadena con el formato *HH: mm: SS. FF* , donde *HH* = hours, *mm* = minutes, *SS* = seconds y *FF* = fracciones de segundo. Ejemplo: 1:04:30.512. Se pueden omitir las unidades iniciales. Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.

## <a name="applies-to"></a>Se aplica a

[**en**](at-element.md), [ **lineal**](linear-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> </dl>

 

 



