---
description: En esta sección se trata el uso de datos del sensor de luz ambiente y cómo se pueden optimizar las características de la interfaz de usuario y el contenido del programa para muchas condiciones de iluminación.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Creación de Light-Aware interfaces de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073557"
---
# <a name="creating-light-aware-user-interfaces"></a>Creación de Light-Aware interfaces de usuario

En esta sección se trata el uso de datos del sensor de luz ambiente y cómo se pueden optimizar las características de la interfaz de usuario y el contenido del programa para muchas condiciones de iluminación.

Los sensores de luz ambiental exponen datos que se pueden usar para determinar varios aspectos de las condiciones de iluminación donde se encuentra el sensor. Los sensores de luz ambiental pueden exponer el brillo general de un entorno (iluminación) y otros aspectos de la luz circundante, como la temperatura del color o la coloración.

Los equipos pueden ser más útiles de varias maneras cuando el sistema responde a las condiciones de iluminación. Esto incluye controlar el brillo de la pantalla del equipo (una nueva característica totalmente compatible en Windows 7), ajustar automáticamente el nivel de iluminación de los teclados iluminados e incluso el control de brillo para otras luces (como la iluminación de botones, las luces de actividad, entre otras).

Los programas de usuario final también pueden beneficiarse de los sensores de luz. Los programas pueden aplicar un tema adecuado para una condición de iluminación determinada, como un tema al aire libre específico y un tema interior. Quizás el aspecto más importante de la integración del sensor de luz con los programas es la legibilidad y las optimizaciones de legibilidad basadas en condiciones de iluminación.

Sensor API le permite crear estos programas. Considere el siguiente escenario:

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a>Escenario: Uso del portátil para navegar a un restaurante

Supongamos que quiere usar el equipo para ayudarle a navegar a un nuevo restaurante. Empiece por su casa, busque la dirección del restaurante y planee la ruta. En la captura de pantalla siguiente se muestra cómo el programa de navegación podría optimizar su interfaz de usuario para mostrar información detallada en condiciones de iluminación interior.

![interfaz de usuario diseñada para iluminación interior.](images/nav-normal.png)

Cuando se va a su automóvil, se encuentra con un desenlazón directo, lo que dificulta la lectura de la pantalla del portátil. En la captura de pantalla siguiente se muestra cómo el programa podría modificar su interfaz de usuario para maximizar la legibilidad o legibilidad en la luz directa. En esta vista, se ha omitido gran parte del detalle y se maximiza el contraste.

![interfaz de usuario diseñada para condiciones de iluminación directa.](images/nav-contrast.png)

A medida que se acerca al restaurante, se acerca la noche y se pone oscuro fuera. En la siguiente captura de pantalla, la interfaz de usuario del programa de navegación se ha optimizado para la visualización con poca luz. Al usar colores más oscuros en general, esta interfaz de usuario es fácil de ver en el automóvil oscuro.

![interfaz de usuario diseñada para la visualización con poca luz.](images/nav-lowlight.png)

En el resto de esta sección, explorará algunas cosas que puede hacer para optimizar los programas para diversas condiciones de iluminación y cómo puede usar sensor API para ayudar a habilitar la interfaz de usuario con luz.

## <a name="in-this-section"></a>En esta sección

-   [Aspectos básicos de Light-Aware interfaces de usuario](fundamentals-of-light-aware-user-interfaces.md)
-   [Ejemplos de interfaces Light-Aware usuario](examples-of-light-aware-user-interfaces.md)
-   [Optimización de la experiencia del usuario](optimizing-the-user-experience.md)
-   [Descripción e interpretación de los valores de Trass](understanding-and-interpreting-lux-values.md)
-   [Uso de datos del sensor de luz](handling-data-from-multiple-light-sensors.md)

 

 



