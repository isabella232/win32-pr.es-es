---
title: dcl_input_control_point_count (sm5 - asm)
description: Declare el recuento de puntos de control de entrada del sombreador de casco en la sección declaración del sombreador de casco.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c5414d5c660cf0bbce2b6219769cd36d4da9bbf3e59d9d130bfce0e0dceea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789885"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a>Recuento de \_ puntos de control de entrada \_ \_ \_ dcl (sm5 - asm)

Declare el recuento de puntos de control de entrada del sombreador de casco en la sección declaración del sombreador de casco.



| dcl \_ input control point count \_ \_ \_ {1..32} |
|-------------------------------------------|



 



| Elemento                                                   | Descripción                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[en \] El recuento de puntos de control de entrada.<br/> |



 

## <a name="remarks"></a>Comentarios

Se requiere al menos un punto de control de entrada; puede estar vacío si no es necesario.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





