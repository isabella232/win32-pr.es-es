---
title: " if"
description: La directiva \ if controla la compilación condicional del archivo de recursos comprobando la expresión constante especificada.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d898d0089ab6abeefb8c11e3a781446e498ed7c0f490545189987ec4857f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599724"
---
# <a name="if"></a>\#if

La **\# directiva if** controla la compilación condicional del archivo de recursos comprobando la expresión constante especificada. Si la expresión constante es distinta de **\# cero,** si indica al compilador que continúe procesando instrucciones hasta la siguiente directiva **\# endif**, **\# else** o **\# elif** y, a continuación, vaya a la instrucción después de la directiva **\# endif.** Si la expresión constante es **\# cero,** si indica al compilador que vaya directamente a la siguiente **\# directiva endif**, **\# else** o **\# elif.**

``` syntax
#if constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*
</dt> <dd>

Expresión que se va a comprobar. Este valor es un nombre definido, una constante de entero o una expresión que consta de nombres, enteros y operadores aritméticos y relacionales.

</dd> </dl>

## <a name="example"></a>Ejemplo

En este ejemplo se compila la [**instrucción BITMAP**](bitmap-resource.md) solo si el valor asignado a Version es menor que 3:

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




