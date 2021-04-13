---
description: Consta de un parámetro de índice y un color RGBA y se usa para definir los colores del vértice de la malla. El índice define el vértice al que se aplica el color.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895cf56efedfa7214bcfa6acafd32ab9324bbe8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359940"
---
# <a name="indexedcolor"></a>IndexedColor

Consta de un parámetro de índice y un color RGBA y se usa para definir los colores del vértice de la malla. El índice define el vértice al que se aplica el color.

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

Donde:

-   index: un valor DWORD. Vea la descripción anterior.
-   indexColor: una plantilla de ColorRGBA. Vea [**ColorRGBA**](colorrgba.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



