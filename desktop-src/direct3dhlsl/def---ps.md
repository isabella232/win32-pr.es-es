---
title: DEF-PS
description: Define las constantes de punto flotante del sombreador de píxeles.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b4f035df97de2645983862dd68aa7ec80fc22d4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078310"
---
# <a name="def---ps"></a>DEF-PS

Define las constantes de punto flotante del sombreador de píxeles.

## <a name="syntax"></a>Sintaxis



| DEF DST, fVvalue1, fValue2, fValue3, fValue4 |
|----------------------------------------------|



 

Donde:

-   DST es el registro de destino.
-   fValue1 to fValue4 son valores de punto flotante.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| def                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Hay dos maneras de establecer una constante de punto flotante en un sombreador de píxeles.

1.  Use Def para definir la constante directamente dentro de un sombreador.
2.  Use la API para establecer una constante con [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).

DEF define una constante de sombreador cuyo valor se carga cada vez que se establece un sombreador en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de la API.

-   Debe aparecer antes de la primera instrucción aritmética o de direccionamiento en el sombreador.
-   Se puede combinar con las instrucciones [DCL-(SM2, SM3-PS ASM)](dcl---ps.md) (que son el otro tipo de instrucción que reside al principio de un sombreador).
-   el registro de DST debe ser un [registro constante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).
-   La máscara de escritura debe estar llena (valor predeterminado).
-   Si un [registro constante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) se define varias veces en un sombreador, el último persiste.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 