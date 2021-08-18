---
title: defb - vs
description: Define un valor constante booleano, que se debe cargar cada vez que un sombreador se establece en un dispositivo.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e5ace74e275ae63a62306d47d50924e9c4e9a9771027e75659ef72345f69906d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792681"
---
# <a name="defb---vs"></a>defb - vs

Define un valor constante booleano, que se debe cargar cada vez que un sombreador se establece en un dispositivo.

## <a name="syntax"></a>Syntax



| defb dest, booleanValue |
|-------------------------|



 

where

-   dst es el registro de destino.
-   booleanValue es un valor booleano, true o false.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| defb                   |      | x    | x    | x     | x    | x     |



 

La instrucción defb - vs define una constante de sombreador booleano cuyo valor se carga cada vez que se establece un sombreador en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetVertexShaderConstantB.

Hay dos maneras de establecer una constante booleana en un sombreador.

1.  Use defb - vs para definir la constante directamente dentro de un sombreador.
2.  Use los métodos de API para establecer una constante.
    -   Use [**SetVertexShaderConstantB para**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) establecer una constante booleana.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def - vs](def---vs.md)
</dt> <dt>

[defi- vs](defi---vs.md)
</dt> </dl>

 

 