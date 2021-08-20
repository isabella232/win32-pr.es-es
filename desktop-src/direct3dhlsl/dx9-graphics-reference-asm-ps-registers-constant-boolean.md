---
title: Registro booleano constante (referencia de HLSL PS)
description: Este registro es una colección de bits que se usan en las instrucciones de control de flujo estático (por ejemplo, si bool - ps - else - ps - endif - ps).
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e86a447d9c0a8ec2d57d2cc7a3f2b7e25714d0d29f2c09add72ab17780b8d8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090398"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a>Registro booleano constante (referencia de HLSL PS)

Este registro es una colección de bits que se usan en las instrucciones de control de flujo estático (por ejemplo, [si bool - ps](if-bool---ps.md)else -  -  [ps](else---ps.md)  -  [endif - ps](endif---ps.md)). Hay 16, por lo tanto, un sombreador puede tener 16 condiciones de rama independientes. Se pueden establecer mediante [defb - ps](defb---ps.md) o [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).

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

 

 