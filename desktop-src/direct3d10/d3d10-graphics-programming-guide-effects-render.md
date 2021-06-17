---
description: Obtenga información sobre cómo representar un efecto para Direct3D 10. Un efecto se puede usar para almacenar información o para representar mediante un grupo de estado.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Representación de un efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79db595585c6587648fba12afa5fbb22ff33e845
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262577"
---
# <a name="rendering-an-effect-direct3d-10"></a>Representación de un efecto (Direct3D 10)

Un efecto se puede usar para almacenar información o para representar mediante un grupo de estado. Cada técnica especifica sombreadores de vértices, sombreadores de geometría, sombreadores de píxeles, estado del sombreador, muestreador y estado de textura y otro estado de canalización. Por lo tanto, una vez que haya organizado el estado en un efecto, puede encapsular el efecto de representación que resulta de ese estado mediante la creación y representación del efecto.

Hay algunos pasos para preparar un efecto para la representación. La primera es la compilación, que comprueba la HLSL como el código con la sintaxis del lenguaje HLSL y las reglas del marco de trabajo de efecto. Puede compilar un efecto desde la aplicación mediante llamadas API o puede compilar un efecto sin conexión mediante la utilidad del compilador effect. Una vez que el efecto se haya compilado correctamente, puede crearlo mediante una llamada a un conjunto diferente (pero muy similar) de API.

Una vez creado el efecto, hay dos pasos restantes para usarlo. En primer lugar, debe inicializar los valores de estado de efecto (los valores de las variables de efecto) mediante una serie de métodos para establecer el estado. Para algunas variables, esto se puede hacer una vez cuando se crea un efecto. otros deben actualizarse cada vez que la aplicación llama al bucle de representación. Una vez establecidas las variables de efecto, se le dice al tiempo de ejecución que represente el efecto mediante la aplicación de una técnica. Estos temas se tratan con más detalle a continuación.

-   [Compilación de un efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-compile.md)
-   [Crear un efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-create.md)
-   [Establecer estado de efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-set-state.md)
-   [Aplicar una técnica (Direct3D 10)](d3d10-graphics-programming-guide-effects-apply-technique.md)

Naturalmente, hay [consideraciones de rendimiento para](d3d10-graphics-programming-guide-effects-performance.md) usar efectos. Estas consideraciones son en gran medida las mismas si no usa ningún efecto. Aspectos como minimizar la cantidad de cambios de estado o organizar las variables que deben actualizarse por frecuencia. Estas tácticas se usan para minimizar la cantidad de datos que se deben enviar desde la CPU a la GPU y, por tanto, minimizar los posibles problemas de sincronización.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



