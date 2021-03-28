---
title: Registro booleano constante (referencia de PS de HLSL)
description: Este registro es una colección de bits que se usa en las instrucciones de control de flujo estático (por ejemplo, si es bool-PS-else-PS-endif-PS).
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4868be7c22ce5a6a1881ad7db8acf0af65330c04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793012"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a>Registro booleano constante (referencia de PS de HLSL)

Este registro es una colección de bits utilizada en las instrucciones de control de flujo estático (por ejemplo, [si es bool-PS](if-bool---ps.md)  -  [else-PS](else---ps.md)  -  [endif-PS](endif---ps.md)). Hay 16 de ellos, por lo tanto, un sombreador puede tener 16 condiciones de rama independientes. Se pueden establecer mediante [defb-PS](defb---ps.md) o [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).

El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.

-   En Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador. La duración de una constante declarada con defx se limita solo a la ejecución de ese sombreador. Por el contrario, las constantes que se establecen mediante las SetXXXShaderConstantX de las API inicializan constantes en el espacio global. Las constantes en el espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.
-   En Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador. Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes independientemente de la técnica utilizada para establecerlas.



| Versiones del sombreador de píxeles     | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| Registro booleano constante |      |      |      |      |      |       | x    | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 