---
title: dcl_samplerType (sm3 - vs asm)
description: Declare un muestreador de sombreador de vértices.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fbcb934ad591274d743f09c810de2db42278261
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129873"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>dcl \_ samplerType (sm3 - vs asm)

Declare un muestreador de sombreador de vértices.

## <a name="syntax"></a>Sintaxis

dcl \_ samplerType s\#



 

donde:

-   \_samplerType define el tipo de datos sampler. Esto determina cuántas coordenadas son necesarias para cada coordenada de textura al realizar el muestreo. Se definen las siguientes dimensiones de coordenadas de textura.
    -   \_2d
    -   \_Cubo
    -   \_volumen
-   s identifica un sampler donde s es una abreviatura del muestreador \# y es el número del \# muestreador. [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s son pseudo registros porque no se pueden leer ni escribir directamente en ellos.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dcl \_ samplerType       |      |      |      |       | x    | x     |



 

Todas las instrucciones \_ dcl samplerType deben aparecer antes de la primera instrucción ejecutable.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




