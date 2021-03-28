---
title: defi-PS
description: Define un valor constante de tipo entero, que se debe cargar cada vez que se establece un sombreador en un dispositivo.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149492"
---
# <a name="defi---ps"></a>defi-PS

Define un valor constante de tipo entero, que se debe cargar cada vez que se establece un sombreador en un dispositivo.

## <a name="syntax"></a>Sintaxis



| defi DST, integerValue |
|------------------------|



 

-   DST es el registro de destino.
-   integerValue es un valor entero constante.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| defi                  |      |      |      |      |      | x    | x     | x    | x     |



 

La instrucción defi define una constante de sombreador cuyo valor se carga cada vez que se establece un sombreador en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetPixelShaderConstantB.

Hay dos maneras de establecer una constante en un sombreador.

1.  Use defi para definir la constante directamente dentro de un sombreador.
2.  Use los métodos de la API para establecer una constante.
    -   Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) para establecer una constante booleana.
    -   Use [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) para establecer una constante de punto flotante.
    -   Use [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) para establecer una constante de tipo entero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 