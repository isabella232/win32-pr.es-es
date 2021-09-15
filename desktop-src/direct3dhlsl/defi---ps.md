---
title: defi - ps
description: Define un valor constante entero, que se debe cargar cada vez que un sombreador se establece en un dispositivo.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466957"
---
# <a name="defi---ps"></a>defi - ps

Define un valor constante entero, que se debe cargar cada vez que un sombreador se establece en un dispositivo.

## <a name="syntax"></a>Sintaxis



| defi dst, integerValue |
|------------------------|



 

-   dst es el registro de destino.
-   integerValue es un valor entero constante.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Defi                  |      |      |      |      |      | x    | x     | x    | x     |



 

La instrucción defi define una constante de sombreador cuyo valor se carga cada vez que un sombreador se establece en un dispositivo. Se denominan constantes inmediatas. Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetPixelShaderConstantB.

Hay dos maneras de establecer una constante en un sombreador.

1.  Use defi para definir la constante directamente dentro de un sombreador.
2.  Use los métodos de API para establecer una constante.
    -   Use [**SetPixelShaderConstantB para**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) establecer una constante booleana.
    -   Use [**SetPixelShaderConstantF para**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) establecer una constante de punto flotante.
    -   Use [**SetPixelShaderConstantI para**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) establecer una constante de entero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 