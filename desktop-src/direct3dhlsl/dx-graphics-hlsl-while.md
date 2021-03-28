---
title: while (Instrucción)
description: Ejecuta un bloque de instrucciones hasta que se produce un error en la expresión condicional.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- while (instrucción) HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 190d5474b5e016b41426db67a0c96d98787f79ff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076616"
---
# <a name="while-statement"></a>while (Instrucción)

Ejecuta un bloque de instrucciones hasta que se produce un error en la expresión condicional.



|                                                                  |
|------------------------------------------------------------------|
| \[*Atributo* \] de while ( *condicional* ) { *bloque de instrucciones*;} |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atribui*
</dt> <dd>

Parámetro opcional que controla cómo se compila la instrucción.



| Atributo             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| deshacer (x)             | Desponga el bucle hasta que deje de ejecutarse. Opcionalmente, puede especificar el número máximo de veces que se puede ejecutar el bucle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| bucle                  | Usar instrucciones de control de flujo en el sombreador compilado; no deshaga el bucle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| fastopt               | Reduce el tiempo de compilación, pero produce optimizaciones menos agresivas. Si utiliza este atributo, el compilador no deshará los bucles.<br/> Este atributo solo afecta a los destinos del modelo de sombreador que admiten instrucciones de [interrupción](dx-graphics-hlsl-break.md) . Este atributo está disponible en el modelo de sombreador [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) y en el [modelo de sombreador 3](dx-graphics-hlsl-sm3.md) y versiones posteriores. Es especialmente útil en el [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores cuando el compilador compila bucles. El compilador simula los bucles de forma predeterminada para evaluar si puede deshacerlos. Si no desea que el compilador deshaga los bucles, utilice este atributo para reducir el tiempo de compilación.<br/> |
| permitir \_ \_ condición UAV | Permite que una condición de finalización del bucle del sombreador de cálculo se base en una lectura UAV. El bucle no debe contener intrínsecos de sincronización.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Instrucción*
</dt> <dd>

[Expresión](dx-graphics-hlsl-expressions.md)condicional. Si la expresión se evalúa como true, se ejecuta el bloque de instrucciones. El bucle finaliza cuando la expresión se evalúa como false.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*
</dt> <dd>

Una o más [instrucciones](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de flujo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





