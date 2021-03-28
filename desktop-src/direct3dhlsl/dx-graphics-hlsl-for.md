---
title: for (Instrucción)
description: Ejecuta una serie de instrucciones de forma iterativa, en función de la evaluación de la expresión condicional.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- for (instrucción HLSL)
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148897"
---
# <a name="for-statement"></a>for (Instrucción)

Ejecuta una serie de instrucciones de forma iterativa, en función de la evaluación de la expresión condicional.



|                                                                                       |
|---------------------------------------------------------------------------------------|
| \[*Atributo* \] de para ( *inicializador; Instrucción Iterator* ) { *bloque de instrucciones*;} |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atribui*
</dt> <dd>

Parámetro opcional que controla cómo se compila la instrucción. Cuando no se especifica ningún atributo, el compilador intentará primero emitir una versión revertida del bucle y, en caso de que se produzca un error, o si algunas operaciones serían más fáciles si el bucle se hubiera inscrito, revertiría a una versión no repuesta del bucle.



| Atributo             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| deshacer (x)             | Desponga el bucle hasta que deje de ejecutarse. Opcionalmente, puede especificar el número máximo de veces que se va a ejecutar el bucle. No es compatible con el atributo de **\[ bucle \]** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| bucle                  | Generar código que usa el control de flujo para ejecutar cada iteración del bucle. No es compatible con el atributo **\[ unroll \]** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| fastopt               | Reduce el tiempo de compilación, pero produce optimizaciones menos agresivas. Si utiliza este atributo, el compilador no deshará los bucles.<br/> Este atributo solo afecta a los destinos del modelo de sombreador que admiten instrucciones de [interrupción](dx-graphics-hlsl-break.md) . Este atributo está disponible en el modelo de sombreador [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) y en el [modelo de sombreador 3](dx-graphics-hlsl-sm3.md) y versiones posteriores. Es especialmente útil en el [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores cuando el compilador compila bucles. El compilador simula los bucles de forma predeterminada para evaluar si puede deshacerlos. Si no desea que el compilador deshaga los bucles, utilice este atributo para reducir el tiempo de compilación. <br/> |
| permitir \_ \_ condición UAV | Permite que una condición de finalización del bucle del sombreador de cálculo se base en una lectura UAV. El bucle no debe contener intrínsecos de sincronización.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inicializador*
</dt> <dd>

Valor inicial del contador de bucles.

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Instrucción*
</dt> <dd>

[Expresión](dx-graphics-hlsl-expressions.md)condicional. Si la expresión condicional se evalúa como true, se ejecuta el bloque de instrucciones. El bucle finaliza cuando la expresión se evalúa como false.

</dd> <dt>

<span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Apunta*
</dt> <dd>

Actualice el valor del contador de bucle.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*
</dt> <dd>

Una o varias [instrucciones de HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los atributos **\[ unroll \]** y **\[ Loop \]** se excluyen mutuamente y generarán errores del compilador cuando se especifiquen ambos.

Los atributos **\[ fastopt \]** y **\[ Allow \_ UAV \_ Condition \]** se omiten si se especifica **\[ unroll \]** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de flujo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





