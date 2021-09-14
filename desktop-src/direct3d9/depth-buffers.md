---
description: Un búfer de profundidad, a menudo denominado z-buffer o w-buffer, es una propiedad del dispositivo que almacena información de profundidad que Direct3D usará.
ms.assetid: vs|directx_sdk|~\depth_buffers.htm
title: Búferes de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1ab41ba98ca5e3b08980ac90a572a19fc8a72a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964995"
---
# <a name="depth-buffers-direct3d-9"></a>Búferes de profundidad (Direct3D 9)

Un búfer de profundidad, a menudo denominado z-buffer o w-buffer, es una propiedad del dispositivo que almacena información de profundidad que Direct3D usará. Cuando Direct3D representa una escena en una superficie de destino, puede usar la memoria de una superficie de búfer de profundidad asociada como un área de trabajo para determinar cómo los píxeles de los polígonos rasterizados se ocultan entre sí. Direct3D usa una superficie de Direct3D fuera de la pantalla como destino en el que se escriben los valores de color finales. La superficie de búfer de profundidad asociada a la superficie de destino de representación se usa para almacenar información de profundidad que indica a Direct3D la profundidad de cada píxel visible en la escena.

Cuando se rasteriza una escena con el almacenamiento en búfer de profundidad habilitado, se prueba cada punto de la superficie de representación. Los valores del búfer de profundidad pueden ser la coordenada z de un punto o su coordenada w homogéneo, desde la ubicación (x, y, z,w) del punto en el espacio de proyección. A menudo, un búfer de profundidad que usa valores z se denomina z-buffer y el que usa valores w se denomina w-buffer. Cada tipo de búfer de profundidad tiene ventajas y desventajas, que se analizan más adelante.

Al principio de la prueba, el valor de profundidad del búfer de profundidad se establece en el valor más grande posible para la escena. El valor de color de la superficie de representación se establece en el valor de color de fondo o en el valor de color de la textura de fondo en ese punto. Cada polígono de la escena se prueba para ver si forma una intersección con la coordenada actual (x,y) en la superficie de representación. Si es así, el valor de profundidad (que será la coordenada z en un búfer z y la coordenada w en un búfer w) en el punto actual se prueba para ver si es menor que el valor de profundidad almacenado en el búfer de profundidad. Si la profundidad del valor del polígono es menor, se almacena en el búfer de profundidad y el valor de color del polígono se escribe en el punto actual de la superficie de representación. Si el valor de profundidad del polígono en ese punto es mayor, se prueba el siguiente polígono de la lista. Este proceso se muestra en el diagrama siguiente.

![diagrama de valores de profundidad de prueba](images/zbuffer.png)

> [!Note]  
> Aunque la mayoría de las aplicaciones no usan esta característica, puede cambiar la comparación que usa Direct3D para determinar qué valores se colocan en el búfer de profundidad y, posteriormente, en la superficie de destino de representación. Para ello, cambie el valor del estado de representación de D3DRS \_ RAGUNC. En algún hardware, cambiar la función de comparación puede deshabilitar las pruebas z jerárquicas.

 

Casi todos los aceleradores del mercado admiten el almacenamiento en búfer z, lo que hace que los búferes z son el tipo más común de búfer de profundidad en la actualidad. Sin embargo, ubicuos, los búferes z tienen sus desventajas. Debido a las matemáticas implicadas, los valores z generados en un búfer z tienden a no distribuirse uniformemente entre el intervalo z-buffer (normalmente de 0,0 a 1,0, ambos incluidos). En concreto, la relación entre los planos de recorte lejos y cercano afecta en gran medida a la distribución desigual de los valores z. Si se usa una relación de distancia de plano lejano a distancia de plano cercano del 100, el 90 % del intervalo de búfer de profundidad se emplea en el primer 10 % del intervalo de profundidad de la escena. Las aplicaciones típicas para el entretenimiento o las simulaciones visuales con escenas exteriores a menudo requieren relaciones de plano lejano/plano próximo de entre 1000 y 10 000. Con una proporción de 1000, el 98 por ciento del intervalo se dedica al primer 2 por ciento del intervalo de profundidad y la distribución se vuelve peor con mayores proporciones. Esto puede provocar artefactos de superficie oculta en objetos lejanos, especialmente cuando se usan búferes de profundidad de 16 bits, la profundidad de bits más comúnmente admitida.

Por otro lado, un búfer de profundidad basado en w suele distribuirse de forma más uniforme entre los planos de recorte cercano y lejano que un búfer Z. La principal ventaja es que la proporción de distancias para los planos de recorte lejanos y cercanos ya no es un problema. Esto permite a las aplicaciones admitir grandes intervalos máximos, a la vez que se sigue obteniendo un almacenamiento en búfer de profundidad relativamente preciso cerca del punto ocular. Un búfer de profundidad basado en w no es perfecto y a veces puede mostrar artefactos de superficie oculta para objetos cercanos. Otro inconveniente del enfoque w-buffered está relacionado con la compatibilidad con hardware: w-buffering no se admite tan ampliamente en hardware como el almacenamiento en búfer z.

El uso de un búfer z requiere sobrecarga durante la representación. Se pueden usar varias técnicas para optimizar la representación cuando se usan búferes z. Para obtener más información, vea [Rendimiento de Z-Buffer.](performance-optimizations.md)

> [!Note]  
> La interpretación real de un valor de profundidad es específica del representador.

 

En esta sección se presenta información sobre el uso de búferes de profundidad para la eliminación de líneas ocultas y superficie oculta.

-   [Consulta de compatibilidad con búferes de profundidad (Direct3D 9)](querying-for-depth-buffer-support.md)
-   [Crear un búfer de profundidad (Direct3D 9)](creating-a-depth-buffer.md)
-   [Habilitación del almacenamiento en búfer de profundidad (Direct3D 9)](enabling-depth-buffering.md)
-   [Recuperar un búfer de profundidad (Direct3D 9)](retrieving-a-depth-buffer.md)
-   [Borrar búferes de profundidad (Direct3D 9)](clearing-depth-buffers.md)
-   [Cambiar el acceso de escritura del búfer de profundidad (Direct3D 9)](changing-depth-buffer-write-access.md)
-   [Cambiar funciones de comparación de búfer de profundidad (Direct3D 9)](changing-depth-buffer-comparison-functions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



