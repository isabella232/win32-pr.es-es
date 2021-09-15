---
title: defb - ps
description: Define un valor constante booleano, que se debe cargar cada vez que un sombreador se establece en un dispositivo.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573873"
---
# <a name="defb---ps"></a>defb - ps

Define un valor constante booleano, que se debe cargar cada vez que un sombreador se establece en un dispositivo.

## <a name="syntax"></a>Sintaxis



| defb dest, booleanValue |
|-------------------------|



 

, donde

-   dst es el registro de destino.
-   booleanValue es un valor booleano único, true o false.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| defb                  |      |      |      |      |      | x    | x     | x    | x     |



 

La instrucción defb define una constante de sombreador booleano cuyo valor se carga cada vez que un sombreador se establece en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetPixelShaderConstantB.

Hay dos maneras de establecer un booleanconstant en un sombreador.

1.  Use defb para definir la constante directamente dentro de un sombreador.
2.  Use los métodos de API para establecer una constante.
    -   Use [**SetPixelShaderConstantB para**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) establecer una constante booleana.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[def - ps](def---ps.md)
</dt> <dt>

[defi- ps](defi---ps.md)
</dt> </dl>

 

 