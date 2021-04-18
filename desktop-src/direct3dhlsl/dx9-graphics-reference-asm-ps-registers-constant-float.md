---
title: Registro Float constante (referencia de PS de HLSL)
description: Registro de entrada del sombreador de píxeles para una constante de punto flotante 4D.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05bb382b745d172ea4b81f9920154e7c79a58c2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421150"
---
# <a name="constant-float-register-hlsl-ps-reference"></a>Registro Float constante (referencia de PS de HLSL)

Registro de entrada del sombreador de píxeles para una constante de punto flotante 4D.

Se pueden establecer mediante [Def-PS](def---ps.md) o [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).

El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.

-   En Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador. La duración de una constante declarada con defx se limita solo a la ejecución de ese sombreador. Por el contrario, las constantes que se establecen mediante las SetXXXShaderConstantX de las API inicializan constantes en el espacio global. Las constantes en el espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.
-   En Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador. Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes independientemente de la técnica utilizada para establecerlas.

## <a name="examples"></a>Ejemplos

Este es un ejemplo en el que se declaran dos constantes de punto flotante dentro de un sombreador.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Estas constantes se cargan cada vez que se llama a [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) .

Si está estableciendo valores constantes con la API, no se requiere ninguna declaración de sombreador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 