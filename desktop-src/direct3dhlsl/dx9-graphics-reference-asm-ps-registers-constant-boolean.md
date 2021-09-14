---
title: Registro booleano constante (referencia de HLSL PS)
description: Este registro es una colección de bits usados en instrucciones de control de flujo estático (por ejemplo, si bool - ps - else - ps - endif - ps).
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4868be7c22ce5a6a1881ad7db8acf0af65330c04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360804"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a>Registro booleano constante (referencia de HLSL PS)

Este registro es una colección de bits usados en instrucciones de control de flujo estático (por ejemplo, [si bool - ps](if-bool---ps.md)else -  -  [ps](else---ps.md)  -  [endif - ps](endif---ps.md)). Hay 16 de ellos, por lo tanto, un sombreador puede tener 16 condiciones de rama independientes. Se pueden establecer mediante [defb - ps](defb---ps.md) o [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).

El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.

-   Para Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador. La duración de una constante declarada con defx solo se limita a la ejecución de ese sombreador. Por el contrario, las constantes establecidas mediante las API SetXXXShaderConstantX inicializan constantes en el espacio global. Las constantes del espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.
-   Para Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador. Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes, independientemente de la técnica utilizada para establecerlas.



| Versiones del sombreador de píxeles     | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| Registro booleano constante |      |      |      |      |      |       | x    | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 