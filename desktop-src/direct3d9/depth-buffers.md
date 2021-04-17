---
description: Un búfer de profundidad, que a menudo se denomina búfer z o un búfer w, es una propiedad del dispositivo que almacena información de profundidad que se va a usar en Direct3D.
ms.assetid: vs|directx_sdk|~\depth_buffers.htm
title: Búferes de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1ab41ba98ca5e3b08980ac90a572a19fc8a72a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494915"
---
# <a name="depth-buffers-direct3d-9"></a>Búferes de profundidad (Direct3D 9)

Un búfer de profundidad, que a menudo se denomina búfer z o un búfer w, es una propiedad del dispositivo que almacena información de profundidad que se va a usar en Direct3D. Cuando Direct3D representa una escena en una superficie de destino, puede usar la memoria en una superficie de búfer de profundidad asociada como área de trabajo para determinar cómo se tapaba los píxeles de los polígonos rasterizados. Direct3D usa una superficie de Direct3D fuera de la pantalla como el destino en el que se escriben los valores finales de color. La superficie del búfer de profundidad que está asociada con la superficie de representación-destino se usa para almacenar información de profundidad que indica a Direct3D el grado de profundidad de cada píxel visible en la escena.

Cuando una escena se rasteriza con el almacenamiento en búfer de profundidad habilitado, se prueba cada punto de la superficie de representación. Los valores del búfer de profundidad pueden ser la coordenada z de un punto o su coordenada w homogénea, desde la ubicación del punto (x, y, z, w) en el espacio de proyección. Un búfer de profundidad que usa valores z a menudo se denomina búfer z, y uno que usa valores w se denomina búfer w. Cada tipo de búfer de profundidad tiene ventajas y desventajas, que se describen más adelante.

Al principio de la prueba, el valor de profundidad en el búfer de profundidad se establece en el valor más grande posible para la escena. El valor de color de la superficie de representación se establece en el valor de color de fondo o en el valor de color de la textura de fondo en ese punto. Cada polígono de la escena se prueba para ver si forma una intersección con la coordenada actual (x, y) en la superficie de representación. Si es así, el valor de profundidad, que será la coordenada z en un búfer z, y la coordenada w en un búfer w-en el punto actual se probará para ver si es menor que el valor de profundidad almacenado en el búfer de profundidad. Si la profundidad del valor de polígono es menor, se almacena en el búfer de profundidad y el valor de color del polígono se escribe en el punto actual de la superficie de representación. Si el valor de profundidad del polígono en ese punto es mayor, se prueba el siguiente polígono de la lista. Este proceso se muestra en el diagrama siguiente.

![diagrama de valores de profundidad de la prueba](images/zbuffer.png)

> [!Note]  
> Aunque la mayoría de las aplicaciones no usan esta característica, puede cambiar la comparación que Direct3D usa para determinar qué valores se colocan en el búfer de profundidad y, posteriormente, la superficie de representación-destino. Para ello, cambie el valor de D3DRS \_ ZFUNC Render State. En el hardware, el cambio de la función de comparación puede deshabilitar las pruebas jerárquicas de z.

 

Casi todos los aceleradores del mercado admiten el almacenamiento en búfer z, lo que permite almacenar en búfer z el tipo más común de búfer de profundidad actualmente. Sin embargo, los búferes z tienen sus desventajas. Debido a las matemáticas implicadas, los valores z generados en un búfer z tienden a no distribuirse uniformemente en el intervalo del búfer z (normalmente de 0,0 a 1,0, ambos inclusive). En concreto, la relación entre los planos de recorte Far y Near afecta de forma muy estricta al modo en que se distribuyen los valores z. El uso de una distancia de plano lejano a una relación de distancia cercana al plano de 100, 90 por ciento del intervalo del búfer de profundidad se emplea en el primer 10 por ciento del intervalo de profundidad de la escena. Las aplicaciones típicas para el entretenimiento o las simulaciones visuales con escenas exteriores suelen requerir coeficientes en el margen o en el plano de un punto entre 1.000 y 10.000. Con una proporción de 1.000, el 98 por ciento del intervalo se emplea en el primer 2 por ciento del intervalo de profundidad y la distribución se vuelve peor con las proporciones más altas. Esto puede producir artefactos de superficie ocultos en objetos distantes, especialmente cuando se usan búferes de profundidad de 16 bits, la profundidad de bits más admitida.

Un búfer de profundidad basado en w, por otro lado, se distribuye a menudo más uniformemente entre los planos de clips cercanos y alejados que un búfer z. La principal ventaja es que la relación de las distancias para los planos de recorte lejanos y cercanos ya no es un problema. Esto permite que las aplicaciones admitan grandes intervalos máximos, al tiempo que se sigue obteniendo un almacenamiento en búfer de profundidad relativamente preciso cerca del punto de mira. Un búfer de profundidad basado en w no es perfecto y a veces puede mostrar artefactos de superficie ocultos para objetos cercanos. Otro inconveniente del enfoque de w-buffered está relacionado con la compatibilidad de hardware: el almacenamiento en búfer de w no se admite en el hardware como almacenamiento en búfer de z.

El uso de un búfer z requiere sobrecarga durante la representación. Se pueden usar varias técnicas para optimizar la representación cuando se utilizan búferes z. Para obtener más información, consulte [Z-buffer performance](performance-optimizations.md).

> [!Note]  
> La interpretación real de un valor de profundidad es específica del representador.

 

En esta sección se ofrece información sobre el uso de búferes de profundidad para la eliminación de la línea oculta y oculta.

-   [Consultar la compatibilidad de búfer de profundidad (Direct3D 9)](querying-for-depth-buffer-support.md)
-   [Crear un búfer de profundidad (Direct3D 9)](creating-a-depth-buffer.md)
-   [Habilitar el almacenamiento en búfer de profundidad (Direct3D 9)](enabling-depth-buffering.md)
-   [Recuperar un búfer de profundidad (Direct3D 9)](retrieving-a-depth-buffer.md)
-   [Borrar búferes de profundidad (Direct3D 9)](clearing-depth-buffers.md)
-   [Cambiar el acceso de escritura de búfer de profundidad (Direct3D 9)](changing-depth-buffer-write-access.md)
-   [Cambiar las funciones de comparación de búfer de profundidad (Direct3D 9)](changing-depth-buffer-comparison-functions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación en Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



