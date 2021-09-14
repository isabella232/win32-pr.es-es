---
title: do (Instrucción, Ocidl.h)
description: Ejecute una serie de instrucciones continuamente hasta que se produce un error en la expresión condicional.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- do (Instrucción HLSL)
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f019af77ef0021ad0574bf703ff2a2a52ac0f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888273"
---
# <a name="do-statement"></a>do (Instrucción)

Ejecute una serie de instrucciones continuamente hasta que se produce un error en la expresión condicional.

\[*Atributo* \] do { *Statement Block*; } while( *Conditional* );



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*
</dt> <dd>

Parámetro opcional que controla cómo se compila la instrucción.



| Atributo | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fastopt   | Reduce el tiempo de compilación, pero genera optimizaciones menos agresivas. Si usa este atributo, el compilador no desenrollará bucles.<br/> Este atributo solo afecta a los destinos del modelo de sombreador que admiten [instrucciones de](dx-graphics-hlsl-break.md) interrupción. Este atributo está disponible en el modelo de sombreador [frente \_ a 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) y en el modelo [de sombreador 3](dx-graphics-hlsl-sm3.md) y versiones posteriores. Resulta especialmente útil en el modelo [de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores cuando el compilador compila bucles. El compilador simula bucles de forma predeterminada para evaluar si puede deshacer su inscripción. Si no desea que el compilador desenrolle bucles, use este atributo para reducir el tiempo de compilación.<br/> |



 

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*
</dt> <dd>

Una o varias [instrucciones](dx-graphics-hlsl-statement-blocks.md).

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*
</dt> <dd>

Expresión [condicional](dx-graphics-hlsl-expressions.md). El bloque de instrucciones se ejecuta antes de evaluar la expresión. El bucle se cierra cuando la expresión se evalúa como false.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Ocidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Flow Control](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





