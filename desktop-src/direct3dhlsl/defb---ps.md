---
title: defb-PS
description: Define un valor constante booleano, que se debe cargar cada vez que se establece un sombreador en un dispositivo.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793030"
---
# <a name="defb---ps"></a>defb-PS

Define un valor constante booleano, que se debe cargar cada vez que se establece un sombreador en un dispositivo.

## <a name="syntax"></a>Sintaxis



| defb Dest, booleanValue |
|-------------------------|



 

, donde

-   DST es el registro de destino.
-   booleanValue es un valor booleano único, ya sea true o false.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| defb                  |      |      |      |      |      | x    | x     | x    | x     |



 

La instrucción defb define una constante de sombreador booleana cuyo valor se carga cada vez que se establece un sombreador en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetPixelShaderConstantB.

Hay dos maneras de establecer un BooleanConstant en un sombreador.

1.  Use defb para definir la constante directamente dentro de un sombreador.
2.  Use los métodos de la API para establecer una constante.
    -   Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) para establecer una constante booleana.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[DEF-PS](def---ps.md)
</dt> <dt>

[defi-PS](defi---ps.md)
</dt> </dl>

 

 