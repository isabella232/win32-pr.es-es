---
description: Aspectos básicos de las interfaces de usuario de Light-Aware
ms.assetid: 7ea391cb-f72b-4ac1-99be-c957d4ccc8af
title: Aspectos básicos de las interfaces de usuario de Light-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce71ab67e11684d14b188fef7ae73500edb7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816694"
---
# <a name="fundamentals-of-light-aware-user-interfaces"></a>Aspectos básicos de las interfaces de usuario de Light-Aware

El término *interfaz de* usuario que tiene en cuenta la luz es un programa que utiliza datos de sensor ligero para optimizar el contenido, los controles y otros gráficos para una experiencia de usuario óptima en muchas condiciones de iluminación, que van desde la oscuridad hasta la luz solar directa. Quizás las optimizaciones más importantes son la legibilidad, la legibilidad y las interacciones en la luz solar directa, ya que las pantallas normalmente no funcionan correctamente en estas condiciones. En esta sección, nos centramos en tres propiedades de la interfaz de usuario: escala, contraste y color. Estas propiedades se pueden cambiar para optimizar la experiencia del usuario visual.

## <a name="scale-and-brightness"></a>Escala y brillo

En general, los objetos más grandes son más fáciles de ver. Cuando el equipo se encuentra en condiciones de iluminación adversas (por ejemplo, en la luz solar directa), el contenido es más grande, lo que puede ayudar a mejorar la legibilidad y la interactivación de ese contenido.

Las siguientes fotografías comparan un portátil en la luz solar directa con un brillo de pantalla y niveles de zoom típicos para un portátil en las mismas condiciones de iluminación con la interfaz de usuario con reconocimiento ligero. La primera fotografía muestra el conjunto de pantallas al brillo del 40% con los niveles de zoom normales. La segunda fotografía muestra el conjunto de pantallas al brillo del 100% con niveles de zoom mayores.

![la pantalla del equipo portátil tiene un brillo del 40% con niveles de zoom normales](images/laptop-40.png)![la pantalla del portátil tiene un brillo del 100% con niveles de zoom mayores](images/laptop-100.png)

### <a name="varying-font-size"></a>Tamaño de fuente variable

Si aumenta el tamaño de la fuente que se usa para mostrar texto, el texto es más legible en condiciones de iluminación adversas. El estilo de fuente, el tipo de fuente y otras características también pueden variar para optimizar la legibilidad y la legibilidad. Por ejemplo, las fuentes Sans Serif suelen ser más fáciles de leer que las fuentes serif.

![fuente sans serif comparada con la fuente serif](images/fonts.png)

### <a name="zooming-content"></a>Zoom de contenido

Si el programa implementa zoom, se puede usar para escalar el contenido. El zoom mejora la legibilidad mientras que al alejar permite que el programa muestre más contenido.

### <a name="altering-vector-graphic-rendering-properties"></a>Modificar propiedades de representación de gráficos vectoriales

Si el programa representa primitivas de gráficos vectoriales (como líneas, círculos, etc.), las características de la representación se pueden modificar para optimizar la legibilidad. Por ejemplo, si el programa representa rectángulos, el ancho de las líneas que se usan para representar los rectángulos se podría escalar (más ancho en el exterior y más estrecho para las puertas) para optimizar la apariencia y la legibilidad del contenido del gráfico vectorial.

## <a name="contrast"></a>Compare

Cuando se usan pantallas LCD en condiciones de iluminación brillante, se reduce el contraste global de la pantalla. Cuando la pantalla se inunda con luz (desde el sol, por ejemplo), se reduce la percepción del usuario de las áreas oscuras en la pantalla. En general, esto hace que sea importante aumentar el contraste del contenido y la interfaz de usuario cuando la luz ambiente es brillante. Puede ser conveniente usar una combinación de colores monocromo para maximizar el contraste en estas condiciones de iluminación. Otra manera de aumentar el contraste es reemplazar el contenido de bajo contraste (por ejemplo, un modo de foto aérea en un programa de asignación) por elementos de contraste alto (como el modo de gráficos de la calle de negro en blanco).

## <a name="color"></a>Color

Los colores que usa un programa para mostrar su contenido pueden tener un efecto drástico en la experiencia general del usuario y la legibilidad del contenido representado. Al cambiar el contraste de color en función de la luz ambiente, puede hacer que el contenido sea más legible en condiciones de iluminación adversa, como la luz de exterior brillante o la luz del interior oscuro.

Una manera de aumentar el contraste de color es a través de la saturación de color. Otra manera es usar colores complementarios en lugar de colores adyacentes para mejorar la legibilidad. Los colores complementarios son pares de colores que son de matiz opuesto, como azul y amarillo. En el siguiente ejemplo en paralelo se muestra cómo el uso de colores complementarios puede ayudar a mejorar el contraste de color.

![ejemplo de los efectos del color de texto en la legibilidad.](images/color.png)

 

 



