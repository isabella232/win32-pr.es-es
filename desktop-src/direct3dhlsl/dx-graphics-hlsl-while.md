---
title: while (Instrucción)
description: Ejecuta un bloque de instrucciones hasta que se produce un error en la expresión condicional.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- while (Instrucción HLSL)
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4e9ae7dc0d8280c9b9823d77dcfe5968243a1ddebdaf78e76b03651ee465034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983165"
---
# <a name="while-statement"></a>while (Instrucción)

Ejecuta un bloque de instrucciones hasta que se produce un error en la expresión condicional.

\[*Atributo* \] while ( *Conditional* ) { *Statement Block*; }



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*
</dt> <dd>

Parámetro opcional que controla cómo se compila la instrucción.



| Atributo             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unroll(x)             | Desenrolle el bucle hasta que deje de ejecutarse. Opcionalmente, puede especificar el número máximo de veces que se puede ejecutar el bucle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| bucle                  | Use instrucciones de control de flujo en el sombreador compilado; no desenrolle el bucle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| fastopt               | Reduce el tiempo de compilación, pero genera optimizaciones menos agresivas. Si usa este atributo, el compilador no desenrollará bucles.<br/> Este atributo solo afecta a los destinos del modelo de sombreador que admiten [instrucciones de](dx-graphics-hlsl-break.md) interrupción. Este atributo está disponible en el modelo de sombreador [frente \_ a 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) y el [modelo de sombreador 3](dx-graphics-hlsl-sm3.md) y versiones posteriores. Es especialmente útil en el modelo [de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores cuando el compilador compila bucles. El compilador simula bucles de forma predeterminada para evaluar si puede deshacer su inscripción. Si no desea que el compilador desrolle bucles, use este atributo para reducir el tiempo de compilación.<br/> |
| permitir \_ condición \_ uav | Permite que una condición de terminación del bucle de sombreador de proceso se base en una lectura UAV. El bucle no debe contener intrínsecos de sincronización.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*
</dt> <dd>

Expresión [condicional](dx-graphics-hlsl-expressions.md). Si la expresión se evalúa como true, se ejecuta el bloque de instrucciones. El bucle finaliza cuando la expresión se evalúa como false.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*
</dt> <dd>

Una o varias [instrucciones](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Flow Control](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





