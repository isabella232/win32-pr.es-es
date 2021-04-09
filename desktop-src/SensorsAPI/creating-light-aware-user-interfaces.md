---
description: En esta sección se trata el uso de datos del sensor de luz ambiente y cómo se pueden optimizar las características de la interfaz de usuario y el contenido del programa para muchas condiciones de iluminación.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Crear interfaces de usuario Light-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002467"
---
# <a name="creating-light-aware-user-interfaces"></a>Crear interfaces de usuario Light-Aware

En esta sección se trata el uso de datos del sensor de luz ambiente y cómo se pueden optimizar las características de la interfaz de usuario y el contenido del programa para muchas condiciones de iluminación.

Los sensores de luz ambiente exponen los datos que se pueden usar para determinar diversos aspectos de las condiciones de iluminación en las que se encuentra el sensor. Los sensores de luz ambiente pueden exponer el brillo general de un entorno (luminancia) y otros aspectos de la luz circundante, como la cromaticidad o la temperatura de color.

Los equipos pueden ser más útiles de varias maneras cuando el sistema responde a las condiciones de iluminación. Esto incluye controlar el brillo de la pantalla del equipo (una característica nueva y totalmente compatible en Windows 7), ajustar automáticamente el nivel de iluminación de los teclados iluminados e incluso controlar la luminosidad de otras luces (como la iluminación del botón, las luces de actividad, etc.).

Los programas de usuario final también pueden beneficiarse de los sensores ligeros. Los programas pueden aplicar un tema adecuado para una condición de iluminación determinada, como un tema de exterior específico y un tema de interior. Quizás el aspecto más importante de la integración del sensor de luz con los programas es la legibilidad y las optimizaciones de legibilidad basadas en condiciones de iluminación.

La API de sensor permite crear dichos programas. Considere el siguiente escenario:

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a>Escenario: uso del portátil para navegar a un restaurante

Supongamos que desea utilizar su equipo para ayudarle a desplazarse a un restaurante nuevo. Comience en su casa, busque la dirección del restaurante y planee la ruta. En la siguiente captura de pantalla se muestra cómo el programa de navegación podría optimizar su interfaz de usuario para mostrar información detallada en condiciones de iluminación interior.

![interfaz de usuario diseñada para la iluminación interior.](images/nav-normal.png)

Cuando se desplaza fuera de su coche, tiene una luz solar directa, lo que dificulta la lectura de la pantalla del portátil. En la captura de pantalla siguiente se muestra cómo el programa puede modificar su interfaz de usuario para maximizar la legibilidad y la legibilidad en la luz directa. En esta vista, gran parte de los detalles se han omitido y el contraste está maximizado.

![interfaz de usuario diseñada para condiciones de iluminación directa.](images/nav-contrast.png)

A medida que se acerque al restaurante, los enfoques de la noche y se oscurecerán. En la siguiente captura de pantalla, la interfaz de usuario del programa de navegación se ha optimizado para la visualización con poca luz. Al usar los colores más oscuros en general, esta interfaz de usuario es fácil de mirar en el coche oscuro.

![interfaz de usuario diseñada para visualización con poca luz.](images/nav-lowlight.png)

En el resto de esta sección, explorará algunas cosas que puede hacer para optimizar los programas para diversas condiciones de iluminación y cómo puede usar la API de sensor para ayudar a habilitar la interfaz de usuario de reconocimiento ligero.

## <a name="in-this-section"></a>En esta sección

-   [Aspectos básicos de las interfaces de usuario de Light-Aware](fundamentals-of-light-aware-user-interfaces.md)
-   [Ejemplos de interfaces de usuario Light-Aware](examples-of-light-aware-user-interfaces.md)
-   [Optimización de la experiencia del usuario](optimizing-the-user-experience.md)
-   [Descripción e interpretación de los valores de Lux](understanding-and-interpreting-lux-values.md)
-   [Uso de datos del sensor de luz](handling-data-from-multiple-light-sensors.md)

 

 



