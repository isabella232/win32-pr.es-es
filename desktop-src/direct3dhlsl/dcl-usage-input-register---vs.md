---
title: dcl_usage entrada (sm1, sm2, sm3 - vs asm)
description: Declare la asociación entre el uso de un elemento de vértice y un índice de uso para un registro de entrada del sombreador de vértices.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae4b024bbce0636127b0ed0fc5f42bc466e1b7fd
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129692"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a>dcl \_ usage input (sm1, sm2, sm3 - vs asm)

Declare la asociación entre el uso de un elemento de vértice y un índice de uso para un registro de entrada del sombreador de vértices.

## <a name="syntax"></a>Sintaxis

dcl \_ usage \[ index \_ \] v\#



 

Donde:

-   El uso \_ de dcl identifica cómo se usarán los datos de registro. Este es el mismo valor que los miembros de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sin el prefijo D3DDECLUSAGE.
-   usage \_ index es un índice entero opcional entre 0 y 15. Modifica los datos de uso. El índice coincide con el índice de uso de una declaración de vértice. Vea [Declaración de vértice (Direct3D 9).](/windows/desktop/direct3d9/vertex-declaration) El índice se anexa al valor de uso (dcl \_ usage ) sin espacio. Si no se proporciona, se supone que es 0.
-   v \# es un registro de [entrada.](dx9-graphics-reference-asm-vs-registers-input.md)

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Uso \_ de dcl             | x    | x    | x    | x     | x    | x     |



 

Todas las instrucciones de uso de dcl \_ deben aparecer antes de la primera instrucción ejecutable.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
