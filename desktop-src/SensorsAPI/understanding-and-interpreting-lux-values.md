---
description: El tipo de datos del sensor principal para los sensores de luz ambiente se luminancia en lux (lúmenes por metro cuadrado). Los principios descritos en este tema se basan en tomar valores de Lux como entrada y reaccionar a esos datos en un programa.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Descripción e interpretación de los valores de Lux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082988"
---
# <a name="understanding-and-interpreting-lux-values"></a>Descripción e interpretación de los valores de Lux

El tipo de datos del sensor principal para los sensores de luz ambiente se luminancia en lux (lúmenes por metro cuadrado). Los principios descritos en este tema se basan en tomar valores de Lux como entrada y reaccionar a esos datos en un programa.

Las lecturas de Lux son directamente proporcionales a la energía por metro cuadrado que se absorbe por segundo. La percepción humana de los niveles de luz no es tan sencilla. La percepción humana de la luz es complicada porque nuestros ojos se están ajustando constantemente y otros procesos biológicos están afectando a nuestra percepción. Sin embargo, podemos pensar en esta percepción desde una perspectiva simplificada creando varios intervalos de interés con umbrales superiores e inferiores conocidos.

En el siguiente conjunto de datos de ejemplo se representan umbrales aproximados para las condiciones de iluminación comunes y el paso de iluminación correspondiente. En este caso, cada paso de iluminación representa un cambio en el entorno de iluminación.

> [!Note]  
> Este conjunto de datos es para la ilustración y puede que no sea completamente preciso para todos los usuarios o situaciones.

 



| Condición de iluminación | Desde (Lux) | A (Lux) | Valor medio (Lux) | Paso de iluminación |
|--------------------|------------|----------|------------------|---------------|
| Tono negro        | 0          | 10       | 5                | 1             |
| Muy oscuro          | 11         | 50       | 30               | 2             |
| Inpuertas oscuras       | 51         | 200      | 125              | 3             |
| Atenuar inpuertas        | 201        | 400      | 300              | 4             |
| Interiores normales     | 401        | 1000     | 700              | 5             |
| Indoors brillantes     | 1001       | 5000     | 3000             | 6             |
| Atenuar en el exterior       | 5001       | 10 000   | 7500             | 7             |
| En el exterior de la nube    | 10.001     | 30,000   | 20 000           | 8             |
| Luz solar directa    | 30.001     | 100 000  | 65.000           | 9             |



 

Si visualizamos estos datos mediante los valores medios de esta tabla, vemos que la relación de lux a iluminación-paso no es lineal, tal como se muestra en el gráfico siguiente.

![gráfico luminancia lineal](images/luxtostep.png)

Sin embargo, si vemos estos datos con una escala logarítmica en el eje x, podemos ver que emerge una relación lineal aproximadamente.

![gráfico luminancia logarítmico](images/luxlogtostep.png)

### <a name="an-example-transform"></a>Transformación de ejemplo

En función del conjunto de datos de ejemplo para los sensores de luz ambiente que se proporcionaron anteriormente, podría llegar a la siguiente ecuación para asignar valores lux a la percepción humana. En este ejemplo, los valores esperados van de 0 lux a 1 millón Lux.

![ecuación de valor Lux](images/sensor-lux-equation.jpg)

Esta ecuación produce valores que varían en un modo lineal aproximadamente entre 0,0 y 1,0. Este resultado indica cómo cambió la iluminación percibida por el usuario en función del conjunto de datos de ejemplo que se mostró anteriormente.

 

 



