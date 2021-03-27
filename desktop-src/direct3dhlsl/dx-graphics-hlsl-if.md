---
title: if (Instrucción)
description: Ejecutar condicionalmente una serie de instrucciones, en función de la evaluación de la expresión condicional.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- Instrucción If HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e8a3c20e73b9783d39b4f4cbdb7c0be5b75fcda
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104077250"
---
# <a name="if-statement"></a>if (Instrucción)

Ejecutar condicionalmente una serie de instrucciones, en función de la evaluación de la expresión condicional.



|                                                               |
|---------------------------------------------------------------|
| \[*Atributo* \] de if ( *condicional* ) { *bloque de instrucciones*;} |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atribui*
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
<td>Evalúa solo un lado de la instrucción if en función de la condición especificada.
<blockquote>
[!Note]<br />
Al usar el modelo de <a href="dx-graphics-hlsl-sm2.md">sombreador 2. x</a> o el <a href="dx-graphics-hlsl-sm3.md">modelo de sombreador 3,0</a>, cada vez que se usa la bifurcación dinámica, se consumen recursos. Por lo tanto, si utiliza la bifurcación dinámica de forma excesiva cuando tiene como destino estos perfiles, puede recibir errores de compilación.
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

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Instrucción*
</dt> <dd>

[Expresión](dx-graphics-hlsl-expressions.md)condicional. La expresión se evalúa y, si es true, se ejecuta el bloque de instrucciones.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*
</dt> <dd>

Una o varias [instrucciones de HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando el compilador usa el método Branch para compilar una instrucción if, generará código que evaluará solo un lado de la instrucción if en función de la condición especificada. Por ejemplo, en la instrucción If:


```
[branch] if(x)
{
    x = sqrt(x);
}
```



La instrucción **If** tiene un bloque else implícito, que es equivalente a x = x. Dado que hemos indicado al compilador que use el método Branch con el atributo Branch anterior, el código compilado evaluará x y ejecutará solo el lado que se debe ejecutar; Si x es cero, se ejecutará el lado **else** y, si es distinto de cero, se ejecutará el lado **then** .

Por el contrario, si se utiliza el atributo **Flatten** , el código compilado evaluará ambos lados de la instrucción **If** y elegirá entre los dos valores resultantes usando el valor original de x. A continuación se muestra un ejemplo de uso del atributo Flatten:


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



Hay algunos casos en los que el uso de los atributos de bifurcación o de acoplamiento puede generar un error de compilación. Se puede producir un error en el atributo Branch si cualquiera de los lados de la instrucción If contiene una función de degradado, como [**tex2D**](dx-graphics-hlsl-tex2d.md). Se puede producir un error en el atributo Flatten si cualquiera de los lados de la instrucción If contiene una instrucción Stream Append o cualquier otra instrucción que tenga efectos secundarios.

Una instrucción **If** también puede utilizar un bloque else opcional. Si la expresión **If** es true, se procesa el código del bloque de instrucciones asociado a la instrucción if. De lo contrario, se procesa el bloque de instrucciones asociado al bloque else opcional.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de flujo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





