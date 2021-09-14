---
description: Define un conjunto de claves de animación. Una clave de matriz es útil para conjuntos de datos de animación que deben representarse como matrices de transformación.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060778"
---
# <a name="animationkey"></a>AnimationKey

Define un conjunto de claves de animación. Una clave de matriz es útil para conjuntos de datos de animación que deben representarse como matrices de transformación.

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

Donde:

-   keyType: especifica si las claves son claves de rotación, escala, posición o matriz (con los enteros 0, 1, 2 o 3, respectivamente).
-   nKeys: número de claves.
-   keys: matriz de claves. Vea [**TimedFloatKeys**](timedfloatkeys.md).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



