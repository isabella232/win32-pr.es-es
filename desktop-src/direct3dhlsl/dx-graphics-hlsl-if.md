---
title: if (Instrucción)
description: Ejecute condicionalmente una serie de instrucciones, en función de la evaluación de la expresión condicional.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- if (Instrucción HLSL)
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 66c04a2ac9c995d3eafa0f93171483c784c72814
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473101"
---
# <a name="if-statement"></a>if (Instrucción)

Ejecute condicionalmente una serie de instrucciones, en función de la evaluación de la expresión condicional.

\[*Atributo* \] if ( *Conditional* ) { *Statement Block*; }



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*
</dt> <dd>

Parámetro opcional que controla cómo se compila la instrucción.




| Atributo | Descripción | 
|-----------|-------------|
| branch | Evalúe solo un lado de la instrucción if en función de la condición dada.<blockquote>[!Note]<br />Cuando se usa <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> o <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, cada vez que se usa la bifurcación dinámica se consumen recursos. Por lo tanto, si usa la bifurcación dinámica excesivamente cuando tiene como destino estos perfiles, puede recibir errores de compilación.</blockquote><br /> | 
| quitar información de estructura jerárquica | Evalúe ambos lados de la instrucción if y elija entre los dos valores resultantes. | 




 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*
</dt> <dd>

Expresión [condicional](dx-graphics-hlsl-expressions.md). Se evalúa la expresión y, si es true, se ejecuta el bloque de instrucciones.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*
</dt> <dd>

Una o varias [instrucciones HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando el compilador usa el método de rama para compilar una instrucción if, generará código que solo evaluará un lado de la instrucción if en función de la condición dada. Por ejemplo, en la instrucción if:


```
[branch] if(x)
{
    x = sqrt(x);
}
```



La **instrucción if** tiene un bloque else implícito, que es equivalente a x = x. Dado que hemos indicado al compilador que use el método de rama con el atributo de rama anterior, el código compilado evaluará x y ejecutará solo el lado que se debe ejecutar; si x es cero, ejecutará el lado **else** y, si es distinto de cero, ejecutará el **lado** siguiente.

Por el contrario, si se usa el atributo **flatten,** el código compilado evaluará ambos lados de la **instrucción if** y elegirá entre los dos valores resultantes con el valor original de x. Este es un ejemplo de uso del atributo flatten:


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



Hay ciertos casos en los que el uso de la rama o los atributos aplanado puede generar un error de compilación. El atributo de rama puede producir un error si cualquiera de los lados de la instrucción if contiene una función de degradado, como [**tex2D.**](dx-graphics-hlsl-tex2d.md) El atributo flatten puede producir un error si cualquiera de los lados de la instrucción if contiene una instrucción stream append o cualquier otra instrucción que tenga efectos secundarios.

Una **instrucción if** también puede usar un bloque else opcional. Si la **expresión if** es true, se procesa el código del bloque de instrucciones asociado a la instrucción if. De lo contrario, se procesa el bloque de instrucciones asociado al bloque else opcional.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Flow Control](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





