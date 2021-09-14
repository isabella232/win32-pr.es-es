---
description: El tipo de datos del sensor principal para los sensores de luz ambiente es ilusoncia en azul (unidades por metro cuadrado). Los principios descritos en este tema se basan en tomar valores como entrada y reaccionar a esos datos en un programa.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Descripción e interpretación de los valores de Trasn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265143"
---
# <a name="understanding-and-interpreting-lux-values"></a>Descripción e interpretación de los valores de Trasn

El tipo de datos del sensor principal para los sensores de luz ambiente es ilusoncia en azul (unidades por metro cuadrado). Los principios descritos en este tema se basan en tomar valores como entrada y reaccionar a esos datos en un programa.

Las lecturas de los libros son directamente proporcionales a la energía por metro cuadrado que se trata por segundo. La percepción humana de los niveles de luz no es tan sencilla. La percepción humana de la luz es complicada porque nuestros ojos se están ajustando constantemente y otros procesos productivos afectan a nuestra percepción. Sin embargo, podemos pensar en esta percepción desde una perspectiva simplificada mediante la creación de varios intervalos de interés con umbrales superiores e inferiores conocidos.

El siguiente conjunto de datos de ejemplo representa umbrales aproximados para condiciones de iluminación comunes y el paso de iluminación correspondiente. Aquí, cada paso de iluminación representa un cambio en el entorno de iluminación.

> [!Note]  
> Este conjunto de datos es para ilustrar y puede que no sea completamente preciso para todos los usuarios o situaciones.

 



| Condición de iluminación | From (lx) | To (lx) | Valor medio (lx) | Paso de iluminación |
|--------------------|------------|----------|------------------|---------------|
| Pitch Black        | 0          | 10       | 5                | 1             |
| Muy oscuro          | 11         | 50       | 30               | 2             |
| Dark Indoors       | 51         | 200      | 125              | 3             |
| Dim Indoors        | 201        | 400      | 300              | 4             |
| Interiores normales     | 401        | 1000     | 700              | 5             |
| Bright Indoors     | 1001       | 5000     | 3000             | 6             |
| Dim Outdoors       | 5001       | 10 000   | 7500             | 7             |
| Cloudy Outdoors    | 10,001     | 30,000   | 20 000           | 8             |
| Efecto directo    | 30,001     | 100 000  | 65,000           | 9             |



 

Si visualizamos estos datos con los valores medio de esta tabla, vemos que la relación entre la iluminación y el paso no es lineal, como se muestra en el gráfico siguiente.

![gráfico de iluminance lineal](images/luxtostep.png)

Sin embargo, si vemos estos datos mediante una escala logarítmica en el eje X, podemos ver que surge una relación aproximadamente lineal.

![Gráfico de iluminación logarítmica](images/luxlogtostep.png)

### <a name="an-example-transform"></a>Una transformación de ejemplo

Según el conjunto de datos de ejemplo para los sensores de luz ambiente proporcionados anteriormente, podría llegar a la siguiente ecuación para asignar valores de mapa a la percepción humana. En este ejemplo, los valores esperados oscilan entre 0 y 1 000 000.

![ecuación de valor de yón](images/sensor-lux-equation.jpg)

Esta ecuación da como resultado valores que varían de forma aproximadamente lineal entre 0,0 y 1,0. Este resultado indica cómo cambió la iluminación percibida por el usuario en función del conjunto de datos de ejemplo que se mostró anteriormente.

 

 



