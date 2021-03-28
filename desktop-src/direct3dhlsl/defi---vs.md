---
title: defi-vs
description: Define un valor constante de tipo entero, que se debe cargar cada vez que se establece un sombreador en un dispositivo.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533393"
---
# <a name="defi---vs"></a>defi-vs

Define un valor constante de tipo entero, que se debe cargar cada vez que se establece un sombreador en un dispositivo.

## <a name="syntax"></a>Sintaxis



| defi DST, integerValue0, integerValue1, integerValue2, integerValue3 |
|----------------------------------------------------------------------|



 

-   DST es el registro de destino.
-   integerValue \# es un valor entero constante.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| defi                   |      | x    | x    | x     | x    | x     |



 

La instrucción defi define una constante de sombreador de enteros cuyo valor se carga cada vez que se establece un sombreador en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetVertexShaderConstantI.

Hay dos maneras de establecer una constante de tipo entero en un sombreador.

1.  Use defi para definir el vector de constante entero directamente dentro de un sombreador.
2.  Use los métodos de la API para establecer una constante.
    -   Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) para establecer una constante de tipo entero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[DEF-vs](def---vs.md)
</dt> <dt>

[defb-vs](defb---vs.md)
</dt> </dl>

 

 