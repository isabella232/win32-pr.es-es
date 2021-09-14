---
title: " else"
description: La directiva \ else marca una cláusula opcional de un bloque de compilación condicional definido por una directiva \ ifdef, \ ifndef o \ if. La directiva \ else debe ser la última directiva antes de la directiva \endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252459"
---
# <a name="else"></a>\#Más

La **\# directiva else** marca una cláusula opcional de un bloque de compilación condicional definido por una **\# directiva ifdef**, **\# ifndef** o **\# if.** La **\# directiva else** debe ser la última antes de la **\# directiva endif.**

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

 

 




