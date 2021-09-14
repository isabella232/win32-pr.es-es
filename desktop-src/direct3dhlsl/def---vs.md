---
title: def - vs
description: Define constantes del sombreador de vértices.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360819"
---
# <a name="def---vs"></a>def - vs

Define constantes del sombreador de vértices.

## <a name="syntax"></a>Sintaxis



| def dst, float1, float2, float3, float4 |
|-----------------------------------------|



 

, donde

-   dst es el registro de destino.
-   float1, float2, float3, float4 son cuatro números de punto flotante.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| def                    | x    | x    | x    | x     | x    | x     |



 

La instrucción def define una constante de sombreador cuyo valor se carga cada vez que se establece un sombreador en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por los métodos de API SetVertexShaderConstantF.

Hay dos maneras de establecer una constante en un sombreador.

1.  Use def - vs para definir la constante directamente dentro de un sombreador.

    def: vs solo puede definir constantes de punto flotante.

2.  Use los métodos de API para establecer una constante.
    -   Use [**SetVertexShaderConstantF para**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) establecer una constante de punto flotante.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[defi- vs](defi---vs.md)
</dt> <dt>

[defb - vs](defb---vs.md)
</dt> </dl>

 

 