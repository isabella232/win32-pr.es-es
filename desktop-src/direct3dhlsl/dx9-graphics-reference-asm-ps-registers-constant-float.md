---
title: Registro float constante (referencia de HLSL PS)
description: Registro de entrada del sombreador de píxeles para una constante de punto flotante 4D.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 025c7e7609e7e0d19c15dfa24e27b9f174114e9287a9e09d01d2436b4ef2ef8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982855"
---
# <a name="constant-float-register-hlsl-ps-reference"></a>Registro float constante (referencia de HLSL PS)

Registro de entrada del sombreador de píxeles para una constante de punto flotante 4D.

Se pueden establecer mediante [def - ps](def---ps.md) o [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).

El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.

-   Para Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador. La duración de una constante declarada con defx solo se limita a la ejecución de ese sombreador. Por el contrario, las constantes establecidas mediante las API SetXXXShaderConstantX inicializan constantes en el espacio global. Las constantes del espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.
-   Para Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador. Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes, independientemente de la técnica utilizada para establecerlas.

## <a name="examples"></a>Ejemplos

Este es un ejemplo que declara dos constantes de punto flotante dentro de un sombreador.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Estas constantes se cargan cada vez que se llama a [**SetPixelShader.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)

Si va a establecer valores constantes con la API, no se requiere ninguna declaración de sombreador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 