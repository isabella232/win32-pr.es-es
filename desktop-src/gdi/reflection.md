---
description: Algunas aplicaciones proporcionan características que reflejan (o reflejar) objetos dibujados en el área de cliente.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Reflexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984838"
---
# <a name="reflection"></a>Reflexión

Algunas aplicaciones proporcionan características que reflejan (o reflejar) objetos dibujados en el área de cliente. Las aplicaciones que contienen capacidades de reflexión usan la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer los valores adecuados en la transformación espacio global en el espacio de página. Esta función recibe un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados. Los miembros eM11 y eM22 de XFORM especifican los componentes de reflexión horizontal y vertical, respectivamente.

La *transformación reflexión* crea una imagen reflejada de un objeto con respecto al eje x o y. En Resumen, la reflexión es simplemente una escala negativa. Para generar una reflexión horizontal, las coordenadas x se multiplican por 1. Para generar una reflexión vertical, las coordenadas y se multiplican por 1.

La reflexión horizontal se puede representar mediante el siguiente algoritmo:

``` syntax
x' = -x 
```

donde x es la coordenada x y x ' es el resultado de la reflexión.

La matriz de 2 por 2 que generó la reflexión horizontal contiene los siguientes valores:

``` syntax
|-1    0| 
|0     1| 
```

La reflexión vertical se puede representar mediante el siguiente algoritmo:

``` syntax
y' = -y 
```

donde y es la coordenada y y ' y ' es el resultado de la reflexión.

La matriz de 2 por 2 que generó la reflexión vertical contiene los siguientes valores:

``` syntax
|1    0| 
|0   -1| 
```

Las operaciones de reflexión horizontal y reflexión vertical se pueden combinar en una sola operación mediante la siguiente matriz de 2 por 2:

``` syntax
|-1    0| 
|0    -1| 
```

 

 



