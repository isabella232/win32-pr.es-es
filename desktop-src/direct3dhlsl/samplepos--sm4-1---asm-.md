---
title: samplepos (sm4.1 - asm)
description: Consulta la posición de un ejemplo en una vista de recursos de sombreador determinada o en el rasterizador.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573689"
---
# <a name="samplepos-sm41---asm"></a>samplepos (sm4.1 - asm)

Consulta la posición de un ejemplo en una vista de recursos de sombreador determinada o en el rasterizador.



| samplepos dest \[ .mask \] , srcResource \[ .swzzle, \] sampleIndex (operando escalar) |
|--------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] El recurso de sombreador.<br/>                         |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[en \] El índice del ejemplo.<br/>                     |



 

## <a name="remarks"></a>Observaciones

Esta instrucción devuelve la posición de ejemplo 2D de *sampleIndex* para el recurso especificado. Solo es válido para los recursos que se pueden cargar mediante [**ld2dms,**](ld2dms--sm4-1---asm-.md) a menos que el rasterizador se especifique *como srcResource*.

*srcResource puede* ser un registro t \# (una vista de recursos de sombreador) o un registro de rasterizador.

La instrucción calcula el vector de punto flotante (Xposition, Yposition, 0, 0).

Swzzle en *srcResource* permite que los valores devueltos se desdoguen arbitrariamente antes de que se escriban en el destino. La posición de ejemplo es relativa al centro del píxel, en función del sistema de coordenadas de píxeles.

Si *sampleIndex* está fuera de los límites, se devuelve un vector cero. Si no hay ningún recurso enlazado a la ranura especificada, se devuelve 0.

**samplepos** se puede usar para aspectos como los resolución personalizados en el código del sombreador.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





