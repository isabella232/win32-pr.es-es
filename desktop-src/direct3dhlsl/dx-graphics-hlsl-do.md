---
title: Instrucción do (Ocidl. h)
description: Ejecute una serie de instrucciones de forma continua hasta que se produzca un error en la expresión condicional.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- Instrucción do HLSL
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
ms.openlocfilehash: 46c0ced3c9747f0bfbdf01847b21350a45b68aa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280309"
---
# <a name="do-statement"></a>Instrucción do

Ejecute una serie de instrucciones de forma continua hasta que se produzca un error en la expresión condicional.



|                                                                     |
|---------------------------------------------------------------------|
| \[*Atributo* \] de do { *bloque de instrucciones*;} while ( *condicional* ); |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atribui*
</dt> <dd>

Parámetro opcional que controla cómo se compila la instrucción.



| Atributo | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fastopt   | Reduce el tiempo de compilación, pero produce optimizaciones menos agresivas. Si utiliza este atributo, el compilador no deshará los bucles.<br/> Este atributo solo afecta a los destinos del modelo de sombreador que admiten instrucciones de [interrupción](dx-graphics-hlsl-break.md) . Este atributo está disponible en el modelo de sombreador [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) y en el [modelo de sombreador 3](dx-graphics-hlsl-sm3.md) y versiones posteriores. Es especialmente útil en el [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores cuando el compilador compila bucles. El compilador simula los bucles de forma predeterminada para evaluar si puede deshacerlos. Si no desea que el compilador deshaga los bucles, utilice este atributo para reducir el tiempo de compilación.<br/> |



 

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*
</dt> <dd>

Una o más [instrucciones](dx-graphics-hlsl-statement-blocks.md).

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Instrucción*
</dt> <dd>

[Expresión](dx-graphics-hlsl-expressions.md)condicional. El bloque de instrucciones se ejecuta antes de que se evalúe la expresión. El bucle se cierra cuando la expresión se evalúa como false.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Ocidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de flujo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





