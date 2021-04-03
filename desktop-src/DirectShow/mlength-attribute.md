---
description: El atributo mlength especifica la duración de un archivo de código fuente. Este valor debe ser la duración real o se pueden producir errores de representación.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Atributo mlength
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997620"
---
# <a name="mlength-attribute"></a>Atributo mlength

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `mlength` atributo especifica la duración de un archivo de código fuente. Este valor debe ser la duración real o se pueden producir errores de representación.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valores posibles

Debe ser una cadena con el formato *HH: mm: SS. FF* , donde *HH* = hours, *mm* = minutes, *SS* = seconds y *FF* = fracciones de segundo. Ejemplo: 1:04:30.512. Se pueden omitir las unidades iniciales. Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



