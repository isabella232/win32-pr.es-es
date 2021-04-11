---
description: Se puede usar un efecto para almacenar información o para representar mediante un grupo de estado.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Representar un efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfba9432412846e2dc634d6ab68be999b504e06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274889"
---
# <a name="rendering-an-effect-direct3d-10"></a>Representar un efecto (Direct3D 10)

Se puede usar un efecto para almacenar información o para representar mediante un grupo de estado. Cada técnica especifica sombreadores de vértices, sombreadores de geometría, sombreadores de píxeles, estado del sombreador, estado de la muestra y textura y otro estado de la canalización. Por tanto, una vez que haya organizado el estado en un efecto, puede encapsular el efecto de representación resultante de ese estado mediante la creación y representación del efecto.

Hay algunos pasos para preparar un efecto para la representación. La primera es la compilación, que comprueba el código de HLSL como el código con la sintaxis del lenguaje HLSL y las reglas del marco de efecto. Puede compilar un efecto desde la aplicación mediante llamadas API o puede compilar un efecto sin conexión mediante la utilidad del compilador de efecto. Una vez que el efecto se ha compilado correctamente, créelo llamando a un conjunto de API diferente (pero muy similar).

Una vez creado el efecto, hay dos pasos restantes para usarlo. En primer lugar, debe inicializar los valores de estado del efecto (los valores de las variables de efecto) mediante una serie de métodos para establecer el estado. En el caso de algunas variables, esto se puede hacer una vez cuando se crea un efecto; otros deben actualizarse cada vez que la aplicación llame al bucle de representación. Una vez establecidas las variables de efecto, se indica al tiempo de ejecución que represente el efecto aplicando una técnica. Estos temas se describen con más detalle a continuación.

-   [Compilación de un efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-compile.md)
-   [Crear un efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-create.md)
-   [Establecer el estado del efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-set-state.md)
-   [Aplicar una técnica (Direct3D 10)](d3d10-graphics-programming-guide-effects-apply-technique.md)

Naturalmente, existen [consideraciones de rendimiento](d3d10-graphics-programming-guide-effects-performance.md) para el uso de efectos. Estas consideraciones son en gran medida las mismas si no está utilizando un efecto. Cosas como, minimizar la cantidad de cambios de estado u organizar las variables que deben actualizarse por frecuencia. Estas tácticas se usan para minimizar la cantidad de datos que deben enviarse desde la CPU a la GPU y, por tanto, minimizar los posibles problemas de sincronización.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



