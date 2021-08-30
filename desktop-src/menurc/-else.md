---
title: " else"
description: La directiva \ else marca una cláusula opcional de un bloque de compilación condicional definido por una directiva \ ifdef, \ ifndef o \ if. La directiva \ else debe ser la última directiva antes de la directiva \endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aade46f8d2af211d4ed09e596ec3a42fa57d141d3d533bdbe34be09d9e9988c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060205"
---
# <a name="else"></a>\#Más

La **\# directiva else** marca una cláusula opcional de un bloque de compilación condicional definido por una **\# directiva ifdef**, **\# ifndef** o **\# if.** La **\# directiva else** debe ser la última directiva antes de la **\# directiva endif.**

``` syntax
#else
```

Esta directiva no tiene parámetros.

## <a name="example"></a>Ejemplo

En este ejemplo se compila la segunda [**instrucción BITMAP**](bitmap-resource.md) solo si no se define DEBUG:

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




