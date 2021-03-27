---
title: defb-vs
description: Define un valor constante booleano, que se debe cargar cada vez que se establece un sombreador en un dispositivo.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bd5ef8ea4218890c025fdebc87154ca1224d33c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995280"
---
# <a name="defb---vs"></a>defb-vs

Define un valor constante booleano, que se debe cargar cada vez que se establece un sombreador en un dispositivo.

## <a name="syntax"></a>Sintaxis



| defb Dest, booleanValue |
|-------------------------|



 

, donde

-   DST es el registro de destino.
-   booleanValue es un valor booleano, ya sea true o false.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| defb                   |      | x    | x    | x     | x    | x     |



 

La instrucción defb-vs define una constante de sombreador booleano cuyo valor se carga cada vez que se establece un sombreador en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetVertexShaderConstantB.

Hay dos maneras de establecer una constante booleana en un sombreador.

1.  Use defb-vs para definir la constante directamente dentro de un sombreador.
2.  Use los métodos de la API para establecer una constante.
    -   Use [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) para establecer una constante booleana.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[DEF-vs](def---vs.md)
</dt> <dt>

[defi-vs](defi---vs.md)
</dt> </dl>

 

 