---
title: dcl_tgsm_raw (sm5 - asm)
description: Declare una referencia a una región de espacio de memoria compartida disponible para el grupo de subprocesos del sombreador de proceso.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0945cde7719129ca43368e50258c02727103209b8d467932e79acd1e1150c89f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024695"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a>dcl \_ tgsm \_ raw (sm5 - asm)

Declare una referencia a una región de espacio de memoria compartida disponible para el grupo de subprocesos del sombreador de proceso.



| dcl \_ tgsm \_ raw g , \# byteCount |
|-------------------------------|



 



| Elemento                                                                                                       | Descripción                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*G\#*<br/>                                                 | \[en \] Una referencia a un bloque de tamaño *byteCount* de memoria compartida sin tipo. <br/> |
| <span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*<br/> | \[en \] Debe ser un múltiplo de 4. <br/>                                             |



 

## <a name="remarks"></a>Comentarios

El almacenamiento total de todos los g debe ser <= la cantidad de memoria compartida disponible por grupo de subprocesos, que \# es 32 kB.

En un caso extremo, puede declarar 8192 g s totales, cada \# uno con un *byteCount* de 4.

En el extremo opuesto, puede declarar un solo g \# con un *byteCount* de 32768.

> [!Note]  
> cs \_ 4 \_ 0 y cs \_ 4 \_ 1 [admiten dcl \_ tgsm \_ estructurado,](dcl-tgsm-structured--sm5---asm-.md)pero no **dcl \_ tgsm \_ raw**.

 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





