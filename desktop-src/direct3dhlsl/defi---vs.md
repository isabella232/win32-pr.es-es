---
title: defi- vs
description: Define un valor constante entero, que se debe cargar cada vez que un sombreador se establece en un dispositivo.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5568a9d1db49dadb9e0e6497cfd4e5af357054f930c35ec6a7e05d59d5f60965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726685"
---
# <a name="defi---vs"></a>defi- vs

Define un valor constante entero, que se debe cargar cada vez que un sombreador se establece en un dispositivo.

## <a name="syntax"></a>Syntax



| defi dst, integerValue0, integerValue1, integerValue2, integerValue3 |
|----------------------------------------------------------------------|



 

-   dst es el registro de destino.
-   integerValue \# es un valor entero constante.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Defi                   |      | x    | x    | x     | x    | x     |



 

La instrucción defi define una constante de sombreador de enteros cuyo valor se carga cada vez que se establece un sombreador en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetVertexShaderConstantI.

Hay dos maneras de establecer una constante de entero en un sombreador.

1.  Use defi para definir el vector constante entero directamente dentro de un sombreador.
2.  Use los métodos de API para establecer una constante.
    -   Use [**SetVertexShaderConstantI para**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) establecer una constante de entero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def - vs](def---vs.md)
</dt> <dt>

[defb - vs](defb---vs.md)
</dt> </dl>

 

 