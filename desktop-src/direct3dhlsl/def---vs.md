---
title: DEF-vs
description: Define las constantes del sombreador de vértices.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271360"
---
# <a name="def---vs"></a>DEF-vs

Define las constantes del sombreador de vértices.

## <a name="syntax"></a>Sintaxis



| DEF DST, float1, float2, float3, FLOAT4 |
|-----------------------------------------|



 

, donde

-   DST es el registro de destino.
-   float1, float2, float3, FLOAT4 son cuatro números de punto flotante.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| def                    | x    | x    | x    | x     | x    | x     |



 

La instrucción Def define una constante de sombreador cuyo valor se carga cada vez que se establece un sombreador en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por los métodos de API SetVertexShaderConstantF.

Hay dos maneras de establecer una constante en un sombreador.

1.  Use Def-vs para definir la constante directamente dentro de un sombreador.

    DEF-vs solo puede definir constantes de punto flotante.

2.  Use los métodos de la API para establecer una constante.
    -   Use [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) para establecer una constante de punto flotante.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[defi-vs](defi---vs.md)
</dt> <dt>

[defb-vs](defb---vs.md)
</dt> </dl>

 

 