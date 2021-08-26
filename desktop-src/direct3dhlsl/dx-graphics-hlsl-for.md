---
title: for (Instrucción)
description: Ejecuta de forma iterativa una serie de instrucciones basadas en la evaluación de la expresión condicional.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- for (Instrucción HLSL)
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 001683c612aefb56d8257977ce7efe99d162a0919d39c678ee4074128a019a31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068195"
---
# <a name="for-statement"></a>for (Instrucción)

Ejecuta de forma iterativa una serie de instrucciones basadas en la evaluación de la expresión condicional.

\[*Atributo* \] for ( *Initializer; Condicional; Iterator* ) { *Bloque de instrucciones*; }



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*
</dt> <dd>

Parámetro opcional que controla cómo se compila la instrucción. Cuando no se especifica ningún atributo, el compilador intentará primero emitir una versión revertida del bucle y, si se produce un error, o si algunas operaciones serían más fáciles si el bucle se anuló, revertirá a una versión no inscrita del bucle.



| Atributo             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unroll(x)             | Desenrolle el bucle hasta que deje de ejecutarse. Opcionalmente, puede especificar el número máximo de veces que se va a ejecutar el bucle. No es compatible con el **\[ atributo de \]** bucle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| bucle                  | Genere código que use el control de flujo para ejecutar cada iteración del bucle. No es compatible con el **\[ atributo unroll. \]**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| fastopt               | Reduce el tiempo de compilación, pero genera optimizaciones menos agresivas. Si usa este atributo, el compilador no desenrollará bucles.<br/> Este atributo solo afecta a los destinos del modelo de sombreador que admiten [instrucciones de](dx-graphics-hlsl-break.md) interrupción. Este atributo está disponible en el modelo de sombreador [frente \_ a 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) y en el modelo [de sombreador 3](dx-graphics-hlsl-sm3.md) y versiones posteriores. Resulta especialmente útil en el modelo [de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores cuando el compilador compila bucles. El compilador simula bucles de forma predeterminada para evaluar si puede deshacer su inscripción. Si no desea que el compilador desenrolle bucles, use este atributo para reducir el tiempo de compilación. <br/> |
| permitir \_ condición \_ uav | Permite que una condición de terminación de bucle de sombreador de proceso se base en una lectura UAV. El bucle no debe contener intrínsecos de sincronización.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inicializador*
</dt> <dd>

Valor inicial del contador de bucles.

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*
</dt> <dd>

Expresión [condicional](dx-graphics-hlsl-expressions.md). Si la expresión condicional se evalúa como true, se ejecuta el bloque de instrucciones. El bucle finaliza cuando la expresión se evalúa como false.

</dd> <dt>

<span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterador*
</dt> <dd>

Actualice el valor del contador de bucles.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*
</dt> <dd>

Una o varias [instrucciones HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los **\[ atributos \] unroll** y **\[ loop \]** son mutuamente excluyentes y generarán errores del compilador cuando se especifiquen ambos.

Los **\[ atributos \] de condición fastopt** **\[ y allow \_ uav \_ \]** se omiten si **\[ se especifica unroll. \]**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Flow Control](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





