---
title: def - ps
description: Define constantes de punto flotante del sombreador de píxeles.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce5f842f44e915d3f3240618261b501f2240c3636227f930538e1bbcbe0d9367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726565"
---
# <a name="def---ps"></a>def - ps

Define constantes de punto flotante del sombreador de píxeles.

## <a name="syntax"></a>Syntax



| def dst, fVvalue1, fValue2, fValue3, fValue4 |
|----------------------------------------------|



 

Donde:

-   dst es el registro de destino.
-   fValue1 a fValue4 son valores de punto flotante.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| def                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Hay dos maneras de establecer una constante de punto flotante en un sombreador de píxeles.

1.  Use def para definir la constante directamente dentro de un sombreador.
2.  Use la API para establecer una constante [**con SetPixelShaderConstantF.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

def define una constante de sombreador cuyo valor se carga cada vez que un sombreador se establece en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API.

-   Debe aparecer antes de la primera instrucción aritmética o de direccionamiento en el sombreador.
-   Se puede mezclar con [instrucciones dcl - (sm2, sm3 - ps asm)](dcl---ps.md) (que son el otro tipo de instrucción que reside al principio de un sombreador).
-   dst register debe ser un [registro constante.](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
-   La máscara de escritura debe estar completa (valor predeterminado).
-   Si un [registro constante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) se define varias veces en un sombreador, se conserva el último.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 