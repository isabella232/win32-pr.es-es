---
title: entrada de dcl_usage (SM1, SM2, SM3-vs ASM)
description: Declare la asociación entre un uso de elemento de vértice y un índice de uso para un registro de entrada del sombreador de vértices.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38113846fe62c37247bb2d3ca522a34dc9282441
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487930"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a>\_entrada de uso de DCL (SM1, SM2, SM3-vs ASM)

Declare la asociación entre un uso de elemento de vértice y un índice de uso para un registro de entrada del sombreador de vértices.

## <a name="syntax"></a>Sintaxis



|                                |
|--------------------------------|
| Índice de uso de DCL \_ \[ \_ \] v\# |



 

Donde:

-   \_el uso de DCL identifica cómo se utilizarán los datos de registro. Este es el mismo valor que los miembros de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sin el prefijo D3DDECLUSAGE.
-   el \_ Índice de uso es un índice entero opcional entre 0 y 15. Modifica los datos de uso. El índice coincide con el índice de uso en una declaración de vértice. Vea [declaración de vértices (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration). El índice se anexa al valor de uso ( \_ uso de DCL) sin espacio. Si no se proporciona, se supone que es 0.
-   v \# es un [registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| uso de DCL \_             | x    | x    | x    | x     | x    | x     |



 

Todas \_ las instrucciones de uso de DCL deben aparecer antes de la primera instrucción ejecutable.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 