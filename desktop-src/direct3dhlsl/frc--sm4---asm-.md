---
title: frc (sm4 - asm)
description: Por componente, extraiga el componente fraccionario.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d7726837a8c88e21b1756c08963a08f3714a9cdb4d93159ed80848166d84e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907618"
---
# <a name="frc-sm4---asm"></a>frc (sm4 - asm)

Por componente, extraiga el componente fraccionario.



| frc \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\] |
|-------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/> *dest*  =  *src0*  -  [round \_ ni](round-ni--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El componente de la operación.<br/>                                                                                        |



 

## <a name="remarks"></a>Comentarios

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.



| **src**  | **-inf** | **-F**     | **-denorm** | **-0** | **+0** | **+denorm** | **+F**     | **+inf** | **NaN** |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **Dest** | NaN      | \[+0 a 1) | +0          | +0     | +0     | +0          | \[+0 a 1) | NaN      | NaN     |



 

F significa número finito-real.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





