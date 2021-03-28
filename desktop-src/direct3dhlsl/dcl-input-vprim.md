---
title: dcl_input vPrim (SM4-ASM)
description: '\_vPrim de entrada de DCL (SM4-ASM)'
ms.assetid: 75287673-21d6-4eb7-829f-7f2f340aec54
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9742c6066d66d7aa4121c1d1d1df98a37cb0147e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419993"
---
# <a name="dcl_input-vprim-sm4---asm"></a>\_vPrim de entrada de DCL (SM4-ASM)

Declara que un sombreador de geometría utiliza su vPrim de registro de entrada escalar.



| \_ *vPrim* de entrada de DCL |
|--------------------|



 



| Elemento                                                                                       | Descripción                                                                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*<br/> | \[en \] un escalar de 32 bits, que se puede aplicar a cada primitiva interior de un sombreador de geometría.<br/> |



 

No se puede aplicar el escalar a ningún primitivo adyacente.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               | x               |              |



 

Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





