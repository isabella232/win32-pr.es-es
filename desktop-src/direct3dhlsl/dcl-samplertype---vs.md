---
title: dcl_samplerType (SM3-vs ASM)
description: Declare una muestra de sombreador de vértices.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996969"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>DCL \_ samplerType (SM3-vs ASM)

Declare una muestra de sombreador de vértices.

## <a name="syntax"></a>Sintaxis



|                      |
|----------------------|
| DCL \_ samplerType s\# |



 

donde:

-   \_samplerType define el tipo de datos de muestra. Esto determina el número de coordenadas que requiere cada coordenada de textura al realizar el muestreo. Se definen las siguientes dimensiones de coordenadas de textura.
    -   \_2D
    -   \_BD
    -   \_cantidad
-   s \# identifica una muestra donde s es una abreviatura de la muestra y \# es el número de muestra. El [muestreador (Direct3D 9 ASM-vs) es un](dx9-graphics-reference-asm-vs-registers-sampler.md)pseudo registro porque no se puede leer ni escribir directamente en ellos.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| samplerType de DCL \_       |      |      |      |       | x    | x     |



 

Todas \_ las instrucciones samplerType de DCL deben aparecer antes de la primera instrucción ejecutable.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




