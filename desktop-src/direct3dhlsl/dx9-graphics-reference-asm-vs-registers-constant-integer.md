---
title: Registro de entero constante (referencia de HLSL VS)
description: Los registros de enteros constantes solo se usan en bucle-vs y REP-vs.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984047"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a>Registro de entero constante (referencia de HLSL VS)

Los registros de enteros constantes solo se usan en [bucle-vs](loop---vs.md) y [REP-vs](rep---vs.md).

Se pueden establecer mediante [defi-vs](defi---vs.md) o [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).

Cuando se usa como argumento para la instrucción [de bucle vs](loop---vs.md) :

-   . x es el recuento de iteraciones. ([REP-vs](rep---vs.md) solo usa este componente).
-   . y es el valor inicial del contador de bucle.
-   . z es el paso de incremento para el contador de bucles.

El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.

-   En Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador. La duración de una constante declarada con defx se limita solo a la ejecución de ese sombreador. Por el contrario, las constantes que se establecen mediante las SetXXXShaderConstantX de las API inicializan constantes en el espacio global. Las constantes en el espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.
-   En Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador. Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes independientemente de la técnica utilizada para establecerlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 