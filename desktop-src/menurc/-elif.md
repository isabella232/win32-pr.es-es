---
title: " elif"
description: La directiva \ elif marca una cláusula opcional de un bloque de compilación condicional definido por una directiva \ ifdef, \ ifndef o \ if.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571637"
---
# <a name="elif"></a>\#Elif

La **\# directiva elif** marca una cláusula opcional de un bloque de compilación condicional definido por una **\# directiva ifdef**, **\# ifndef** o **\# if.** La directiva controla la compilación condicional del archivo de recursos comprobando la expresión constante especificada. Si la expresión constante es distinta de cero, **\# elif** indica al compilador que continúe procesando instrucciones hasta la siguiente **\# directiva endif**, **\# else** o **\# elif** y, a continuación, omite la instrucción después **\# de endif**. Si la expresión constante es cero, **\# elif** indica al compilador que vaya directamente a la siguiente **\# directiva endif**, **\# else** o **\# elif.** Puede usar cualquier número de directivas **\# elif** en un bloque condicional.

``` syntax
#elif constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*
</dt> <dd>

Expresión que se va a comprobar. Este valor es un nombre definido, una constante de entero o una expresión que consta de nombres, enteros y operadores aritméticos y relacionales.

</dd> </dl>

## <a name="example"></a>Ejemplo

En este ejemplo, **\# elif** indica al compilador que procese la segunda instrucción [**BITMAP**](bitmap-resource.md) solo si el valor asignado al nombre Version es menor que 7. La **\# propia directiva elif** se procesa solo si Version es mayor o igual que 3.

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

 

 




