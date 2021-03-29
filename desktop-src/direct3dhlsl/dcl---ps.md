---
title: 'DCL: (SM2, SM3-PS ASM)'
description: Declare un registro de entrada del sombreador de píxeles.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad61ea8d733ed01fcd2e57ba06c38e0b3efac682
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419959"
---
# <a name="dcl---sm2-sm3---ps-asm"></a>DCL: (SM2, SM3-PS ASM)

Declare un registro de entrada del sombreador de píxeles.

## <a name="syntax"></a>Sintaxis



|                           |
|---------------------------|
| DCL \[ \_ PP \] dest \[ . Mask\] |



 

Donde:

-   \[\_PP \] es una precisión parcial opcional. Vea [precisión parcial](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).
-   dest es un registro de destino. Debe ser un registro de [color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (VN) o un [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN).
-   \[. Mask \] es una máscara de escritura opcional que controla los componentes del registro de destino en los que se puede escribir. Consulte [máscara de escritura de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DCL                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Todas las instrucciones de DCL deben aparecer antes de la primera instrucción ejecutable.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




