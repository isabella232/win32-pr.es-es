---
description: Algunas aplicaciones proporcionan características que reflejan (o reflejan) objetos dibujados en el área de cliente.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Reflexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072467"
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

 

 



