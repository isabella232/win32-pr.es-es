---
description: El atributo Samplingrate especifica la velocidad de muestreo del audio de salida, en Hz.
ms.assetid: d053285c-bf94-465a-99d3-bed7c2d09b1a
title: Atributo Samplingrate
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2daa2751b0c41f5bf2eb030841dad638d8672a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677157"
---
# <a name="samplingrate-attribute"></a>Atributo Samplingrate

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `samplingrate` atributo especifica la velocidad de muestreo del audio de salida, en Hz.

## <a name="possible-values"></a>Valores posibles

El valor debe ser 8000, 11025, 22050, 32000, 44100 o 48000. El valor predeterminado es 44100.

## <a name="applies-to"></a>Se aplica a

[**agrupamiento**](group-element.md)

## <a name="remarks"></a>Observaciones

Establezca este atributo solo si el atributo de **tipo** es `audio` .

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> </dl>

 

 



