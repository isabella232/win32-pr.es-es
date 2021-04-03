---
title: " elif"
description: La Directiva \ Elif marca una cláusula opcional de un bloque de compilación condicional definido por una directiva \ ifdef, \ ifndef o \ if.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075857"
---
# <a name="elif"></a>\#elif

La directiva **\# Elif** marca una cláusula opcional de un bloque de compilación condicional definido por una directiva **\# ifdef**, **\# ifndef** o **\# If** . La directiva controla la compilación condicional del archivo de recursos comprobando la expresión constante especificada. Si la expresión constante es distinta de cero, **\# Elif** indica al compilador que continúe con el procesamiento de las instrucciones hasta la siguiente directiva **\# endif**, **\# else** o **\# Elif** y, a continuación, vaya a la instrucción después de **\# endif**. Si la expresión constante es cero, **\# Elif** indica al compilador que vaya a la siguiente directiva **\# endif**, **\# else** o **\# Elif** . Puede usar cualquier número de directivas **\# Elif** en un bloque condicional.

``` syntax
#elif constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*expresión constante*
</dt> <dd>

Expresión que se va a comprobar. Este valor es un nombre definido, una constante de tipo entero o una expresión que consta de nombres, enteros y operadores aritméticos y relacionales.

</dd> </dl>

## <a name="example"></a>Ejemplo

En este ejemplo, **\# Elif** indica al compilador que procese la segunda instrucción de [**mapa de bits**](bitmap-resource.md) solo si el valor asignado a la versión de nombre es inferior a 7. La propia directiva **\# Elif** solo se procesa si la versión es mayor o igual que 3.

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




