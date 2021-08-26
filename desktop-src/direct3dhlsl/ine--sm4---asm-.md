---
title: ine (sm4 - asm)
description: Comparación de enteros vectoriales por componente no igual.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0170dd8b5cfd6284356699bc065e5581a601f8868bfd6c0db99a6a53f9bcfd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023855"
---
# <a name="ine-sm4---asm"></a>ine (sm4 - asm)

Comparación de enteros vectoriales por componente no igual.



| ine dest \[ .mask \] , src0 \[ .swzzle \] , src1 \[ .sw swle\] |
|-------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Contiene el valor que se va a comparar con *src1.*<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Contiene el valor que se va a comparar con *src0.*<br/>    |



 

## <a name="remarks"></a>Comentarios

Realiza la comparación de enteros (*src0* != *src1*) para cada componente y escribe el resultado *en dest*.

Si la comparación es verdadera, 0xFFFFFFFF se devuelve para ese componente. De lo 0x0000000 se devuelven los 0x0000000

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Shader Model 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





