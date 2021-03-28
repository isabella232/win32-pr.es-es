---
title: gather4_po (SM5-ASM)
description: Una variante de gather4, pero en lugar de admitir un desplazamiento inmediato \-8.. 7 \, el desplazamiento viene como parámetro de la instrucción y también tiene un intervalo mayor de \-32.. 31 \.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983874"
---
# <a name="gather4_po-sm5---asm"></a>\_po gather4 (SM5-ASM)

Una variante de [gather4](gather4--sm5---asm-.md), pero en lugar de admitir un desplazamiento inmediato \[ -8.. 7 \] , el desplazamiento viene como parámetro de la instrucción y también tiene un intervalo mayor de \[ -32.. 31 \] .



| gather4 \_ po dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcOffset \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . Select ( \_ componente)\] |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección del resultado de la operación.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] un conjunto de coordenadas de textura.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>         | \[en \] el desplazamiento.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] un registro de textura.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] un registro de muestra.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Los dos primeros componentes del parámetro de desplazamiento de 4 vectores proporcionan desplazamientos de enteros de 32 bits. Los demás componentes de este parámetro se omiten.

Los 6 bits menos significativos de cada valor de desplazamiento se admiten como un valor con signo, lo que produce un \[ intervalo de-32.. 31 \] .

Esta instrucción solo funciona con texturas 2D, a diferencia de **gather4**, que también funciona con TextureCubes.

Los únicos modos que se respetan en la muestra son los modos de direccionamiento. Solo se utiliza el MIP más detallado en la vista de recursos.

Si la dirección se encuentra en un centro de textura, esto no significa que el otro textura se pueda poner a cero.

El parámetro *srcSampler* incluye el \[ componente. Select \_ \] , lo que permite recuperar cualquier componente individual de una textura, incluida la devolución de valores predeterminados para los componentes que faltan.

En el caso de los formatos con componentes float32, si el valor que se va a capturar es normalizado, desnormalizado, +-0 o +-INF, se devuelve al sombreador sin modificar. NaN se devuelve como NaN, pero se puede cambiar la representación de bits exacta del NaN. En el caso de TextureCubes, algunas síntesis de la cuarta textura que faltan deben aparecer en las esquinas, por lo que no se aplica la noción de devolver bits sin modificar para la textura sintetizada, y se pueden vaciar las denormalidades.

Use esta instrucción para extender el intervalo de desplazamiento de **gather4** de forma que sea más grande y programable. El sufijo "PO" en el nombre significa "desplazamiento programable".

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





