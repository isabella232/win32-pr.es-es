---
description: Aspectos básicos de Light-Aware interfaces de usuario
ms.assetid: 7ea391cb-f72b-4ac1-99be-c957d4ccc8af
title: Aspectos básicos de Light-Aware interfaces de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8955180dfc57219d3b640c6463f2ee2025f22500d3d29b688bc4b0c154895f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890211"
---
# <a name="fundamentals-of-light-aware-user-interfaces"></a>Aspectos básicos de Light-Aware interfaces de usuario

El  término interfaz de usuario ligera hace referencia a un programa que usa datos de sensores claros para optimizar su contenido, controles y otros gráficos para una experiencia de usuario óptima en muchas condiciones de iluminación, que van desde la deserción hasta la iluminación directa. Quizás las optimizaciones más importantes son la legibilidad, la legibilidad y las interacciones en la sensibilidad directa, ya que las pantallas no suelen tener un buen rendimiento en estas condiciones. En esta sección, nos centraremos en tres propiedades de la interfaz de usuario: escala, contraste y color. Estas propiedades se pueden cambiar para optimizar la experiencia del usuario visual.

## <a name="scale-and-brightness"></a>Escala y brillo

En general, los objetos más grandes son más fáciles de ver. Cuando el equipo se encuentra en condiciones de iluminación adversas (por ejemplo, en la receptación directa), hacer que el contenido sea mayor puede ayudar a mejorar la legibilidad e interactiva de ese contenido.

Las fotografías siguientes comparan un portátil con niveles de brillo y zoom típicos de un equipo portátil en las mismas condiciones de iluminación con una interfaz de usuario ligera. La primera fotografía muestra la pantalla establecida en un 40 % de brillo con niveles de zoom normales. La segunda fotografía muestra la pantalla establecida en un brillo del 100 % con mayores niveles de zoom.

![Pantalla de portátil con un brillo del 40 % con niveles de zoom normales](images/laptop-40.png)![Pantalla de portátil con un brillo del 100 % con mayores niveles de zoom](images/laptop-100.png)

### <a name="varying-font-size"></a>Variación del tamaño de fuente

Si aumenta el tamaño de la fuente que se usa para mostrar texto, el texto es más legible en condiciones de iluminación adversas. El estilo de fuente, la cara de fuente y otras características también pueden variar para optimizar la legibilidad y la legibilidad. Por ejemplo, las fuentes sans serif suelen ser más fáciles de leer que las fuentes serif.

![fuente sans serif en comparación con la fuente serif](images/fonts.png)

### <a name="zooming-content"></a>Acercar contenido

Si el programa implementa el zoom, se puede usar para escalar el contenido. El acercamiento mejora la legibilidad, mientras que el zoom hacia fuera permite que el programa muestre más contenido.

### <a name="altering-vector-graphic-rendering-properties"></a>Modificar las propiedades de representación de gráficos vectoriales

Si el programa representa primitivas gráficas vectoriales (como líneas, círculos, entre otros), las características de la representación se pueden modificar para optimizar la legibilidad. Por ejemplo, si el programa representa rectángulos, el ancho de las líneas que se usan para representar los rectángulos se podría escalar (más ancho para exteriores y más estrecho para interiores) para optimizar la apariencia y legibilidad del contenido gráfico vectorial.

## <a name="contrast"></a>Compare

Cuando se usan pantallas DE COLOR AZUL en condiciones de iluminación brillantes, se reduce el contraste general de la pantalla. Cuando la pantalla se desborda con luz (por ejemplo, desde el sol), se reduce la percepción del usuario de las áreas oscuras en la pantalla. En general, esto hace que sea importante aumentar el contraste del contenido y la interfaz de usuario cuando la luz ambiente es brillante. Puede ser conveniente usar una combinación de colores monocromática para maximizar el contraste en estas condiciones de iluminación. Otra manera de aumentar el contraste es reemplazar el contenido de contraste bajo (por ejemplo, un modo de foto aérea en un programa de asignación) por elementos de contraste alto (como el modo gráfico de vector de calle en blanco y negro).

## <a name="color"></a>Color

Los colores que usa un programa para mostrar su contenido pueden tener un efecto drástico en la experiencia general del usuario y la legibilidad del contenido representado. Al cambiar el contraste de color en función de la luz ambiente, puede hacer que el contenido sea más legible en condiciones de iluminación adversas, como luz exterior brillante o luz interior oscura.

Una manera de aumentar el contraste de color es a través de la saturación del color. Otra manera es usar colores complementarios en lugar de colores adyacentes para mejorar la legibilidad. Los colores complementarios son pares de colores que son de matiz opuesto, como azul y amarillo. En el siguiente ejemplo en paralelo se muestra cómo el uso de colores complementarios puede ayudar a mejorar el contraste de color.

![ejemplo de los efectos del color del texto en la legibilidad.](images/color.png)

 

 



