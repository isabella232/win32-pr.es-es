---
title: dcl - (sm2, sm3 - ps asm)
description: Declare un registro de entrada del sombreador de píxeles.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f2ba81650611351970ff4068edaa75d27d34fc4
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130104"
---
# <a name="dcl---sm2-sm3---ps-asm"></a>dcl - (sm2, sm3 - ps asm)

Declare un registro de entrada del sombreador de píxeles.

## <a name="syntax"></a>Sintaxis

dcl \[ \_ pp \] dest \[ .mask\]



 

Donde:

-   \[\_pp \] es una precisión parcial opcional. Vea [Precisión parcial.](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)
-   dest es un registro de destino. Debe ser un registro de [color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn) o un registro de coordenadas de [textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).
-   \[.mask \] es una máscara de escritura opcional que controla en qué componentes del registro de destino se puede escribir. Vea [Máscara de escritura del registro de destino.](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Dcl                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Todas las instrucciones dcl deben aparecer antes de la primera instrucción ejecutable.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




