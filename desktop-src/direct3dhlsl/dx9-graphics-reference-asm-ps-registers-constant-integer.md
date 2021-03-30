---
title: Registro de entero constante (referencia de PS de HLSL)
description: Los registros de enteros constantes solo se usan en loop-PS y REP-PS.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b03a27a95f84ae30a70147caaf5662e1949cf18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984038"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a>Registro de entero constante (referencia de PS de HLSL)

Los registros de enteros constantes solo se usan en [Loop-PS](loop---ps.md) y [REP-PS](rep---ps.md).

Se pueden establecer mediante [defi-PS](defi---ps.md) o [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).

Cuando se usa como argumento para la instrucción [de bucle-PS](loop---ps.md) :

-   . x es el recuento de iteraciones. ([REP-PS](rep---ps.md) usa solo este componente).
-   . y es el valor inicial del contador de bucle.
-   . z es el paso de incremento para el contador de bucles.



| Versiones del sombreador de píxeles     | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| Registro de entero constante |      |      |      |      |      |       | x    | x    | x     |



 

El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.

-   En Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador. La duración de una constante declarada con defx se limita solo a la ejecución de ese sombreador. Por el contrario, las constantes que se establecen mediante las SetXXXShaderConstantX de las API inicializan constantes en el espacio global. Las constantes en el espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.
-   En Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador. Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes independientemente de la técnica utilizada para establecerlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 