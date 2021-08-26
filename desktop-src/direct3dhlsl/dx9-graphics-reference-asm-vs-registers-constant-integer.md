---
title: Registro de enteros constantes (referencia de HLSL VS)
description: Los registros enteros constantes solo los usa el bucle (vs y rep) frente a .
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b46390303b2ee3aae2243f25d2a5a76385b9e9dd275c2952e8aa93e18f999e9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949905"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a>Registro de enteros constantes (referencia de HLSL VS)

Los registros de enteros constantes solo los usa [el bucle (vs](loop---vs.md) y [rep) frente a](rep---vs.md).

Se pueden establecer mediante [defi - vs o](defi---vs.md) [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).

Cuando se usa como argumento para el [bucle - vs](loop---vs.md) instrucción :

-   .x es el recuento de iteraciones. [(rep: vs](rep---vs.md) usa solo este componente).
-   .y es el valor inicial del contador de bucles.
-   .z es el paso de incremento para el contador de bucle.

El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.

-   Para Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador. La duración de una constante declarada con defx solo se limita a la ejecución de ese sombreador. Por el contrario, las constantes establecidas mediante las API SetXXXShaderConstantX inicializan constantes en el espacio global. Las constantes del espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.
-   Para Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador. Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes, independientemente de la técnica utilizada para establecerlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 