---
description: Algunas aplicaciones proporcionan características que reflejan (o reflejan) objetos dibujados en el área de cliente.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Reflexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03d872273e7d0b9f23d9ffb31c6304c8b59b59eda80c7181802120f89c0d764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092705"
---
# <a name="reflection"></a>Reflexión

Algunas aplicaciones proporcionan características que reflejan (o reflejan) objetos dibujados en el área de cliente. Las aplicaciones que contienen funcionalidades de reflexión usan la [**función SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer los valores adecuados en la transformación espacio del mundo en espacio de página. Esta función recibe un puntero a una [**estructura XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados. Los miembros eM11 y eM22 de XFORM especifican los componentes de reflexión horizontal y vertical, respectivamente.

La *transformación de reflexión* crea una imagen reflejada de un objeto con respecto al eje x o y. En resumen, la reflexión es simplemente un escalado negativo. Para generar una reflexión horizontal, las coordenadas X se multiplican por 1. Para generar una reflexión vertical, las coordenadas Y se multiplican por 1.

La reflexión horizontal se puede representar mediante el algoritmo siguiente:

``` syntax
x' = -x 
```

donde x es la coordenada x y x' es el resultado de la reflexión.

La matriz 2 por 2 que produjo la reflexión horizontal contiene los valores siguientes:

``` syntax
|-1    0| 
|0     1| 
```

La reflexión vertical se puede representar mediante el algoritmo siguiente:

``` syntax
y' = -y 
```

donde y es la coordenada y y' es el resultado de la reflexión.

La matriz 2 por 2 que produjo la reflexión vertical contiene los valores siguientes:

``` syntax
|1    0| 
|0   -1| 
```

Las operaciones de reflexión horizontal y reflexión vertical se pueden combinar en una sola operación mediante la siguiente matriz 2 por 2:

``` syntax
|-1    0| 
|0    -1| 
```

 

 



