---
description: Consta de un parámetro de índice y un color RGBA y se usa para definir colores de vértice de malla. El índice define el vértice al que se aplica el color.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b0dcaf850786a18e5fc317276939436b93c3a49765d520aa40f88cd53707d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563735"
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

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



