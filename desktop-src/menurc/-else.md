---
title: " else"
description: La Directiva \ else marca una cláusula opcional de un bloque de compilación condicional definido por una directiva \ ifdef, \ ifndef o \ if. La Directiva \ else debe ser la última Directiva antes de la Directiva \ endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776447"
---
# <a name="else"></a>\#else

La directiva **\# else** marca una cláusula opcional de un bloque de compilación condicional definido por una directiva **\# ifdef**, **\# ifndef** o **\# If** . La directiva **\# else** debe ser la última Directiva antes de la directiva **\# endif** .

``` syntax
#else
```

Esta Directiva no tiene parámetros.

## <a name="example"></a>Ejemplo

En este ejemplo se compila la segunda instrucción [**Bitmap**](bitmap-resource.md) solo si no se define DEBUG:

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

 

 




