---
description: Consta de un parámetro de índice y un color RGBA y se usa para definir colores de vértice de malla. El índice define el vértice al que se aplica el color.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895cf56efedfa7214bcfa6acafd32ab9324bbe8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574073"
---
# <a name="indexedcolor"></a>IndexedColor

Consta de un parámetro de índice y un color RGBA y se usa para definir colores de vértice de malla. El índice define el vértice al que se aplica el color.

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

Donde:

-   index: DWORD. Consulte la descripción anterior.
-   indexColor: una plantilla ColorRGBA. Vea [**ColorRGBA**](colorrgba.md).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



