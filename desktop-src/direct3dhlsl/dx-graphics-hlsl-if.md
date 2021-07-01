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
ms.openlocfilehash: df4a1f049526422f39c3529395481548943c7e84
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118960"
---
# <a name="if-statement"></a>if (Instrucción)

Ejecute condicionalmente una serie de instrucciones, en función de la evaluación de la expresión condicional.

\[*Atributo* \] if ( *Conditional* ) { *Statement Block*; }



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*
</dt> <dd>

Parámetro opcional que controla cómo se compila la instrucción.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>branch</td>
<td>Evalúe solo un lado de la instrucción if en función de la condición dada.
<blockquote>
[!Note]<br />
Cuando se usa <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> o <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0,</a>cada vez que se usa la bifurcación dinámica se consumen recursos. Por lo tanto, si usa la bifurcación dinámica excesivamente cuando tiene como destino estos perfiles, puede recibir errores de compilación.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>quitar información de estructura jerárquica</td>
<td>Evalúe ambos lados de la instrucción if y elija entre los dos valores resultantes.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*
</dt> <dd>

Expresión [condicional](dx-graphics-hlsl-expressions.md). Se evalúa la expresión y, si es true, se ejecuta el bloque de instrucciones.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*
</dt> <dd>

Una o varias [instrucciones HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando el compilador usa el método de rama para compilar una instrucción if, generará código que evaluará solo un lado de la instrucción if en función de la condición dada. Por ejemplo, en la instrucción if:


```
[branch] if(x)
{
    x = sqrt(x);
}
```



La **instrucción if** tiene un bloque else implícito, que es equivalente a x = x. Dado que hemos indicado al compilador que use el método de rama con el atributo de rama anterior, el código compilado evaluará x y ejecutará solo el lado que se debe ejecutar; si x es cero, ejecutará  el otro lado y, si es distinto de cero, ejecutará el **lado** siguiente.

Por el contrario, si se usa el atributo **flatten,** el código compilado evaluará ambos lados de la **instrucción if** y elegirá entre los dos valores resultantes con el valor original de x. Este es un ejemplo de un uso del atributo flatten:


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



Hay ciertos casos en los que el uso de la rama o los atributos planos puede generar un error de compilación. El atributo de rama puede producir un error si cualquiera de los lados de la instrucción if contiene una función de degradado, como [**texas2D.**](dx-graphics-hlsl-tex2d.md) El atributo flatten puede producir un error si cualquiera de los lados de la instrucción if contiene una instrucción stream append o cualquier otra instrucción que tenga efectos secundarios.

Una **instrucción if** también puede usar un bloque else opcional. Si la **expresión if** es true, se procesa el código del bloque de instrucciones asociado a la instrucción if. De lo contrario, se procesa el bloque de instrucciones asociado al bloque else opcional.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control de flujo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





