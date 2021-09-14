---
description: La propiedad AnglesAvailable recupera el número de ángulos disponibles actualmente.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Propiedad AnglesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162265"
---
# <a name="anglesavailable-property"></a>Propiedad AnglesAvailable

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `AnglesAvailable` propiedad recupera el número de ángulos disponibles actualmente.

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero comprendido entre 1 y 9 que representa el número de ángulos disponibles actualmente. Si


```
iAngles
```



= 1, no hay ningún bloque angular en la ubicación actual.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura sin ningún valor predeterminado. Un *bloque angular* es un segmento de vídeo que se rodó desde más de un ángulo de cámara. Puede haber hasta nueve ángulos en un bloque angular, numerados de 1 a 9. Cuando el navegador de DVD entra por primera vez en un bloque angular, envía a la aplicación una notificación de eventos EC DVD ANGLES AVAILABLE con el número de \_ \_ \_ ángulos *en lParam1*. Se puede crear un disco para mostrar automáticamente un menú para los ángulos disponibles cuando entra en un bloque angular, pero generalmente una aplicación debe determinar el número de ángulos disponibles y ofrecer al usuario una manera de seleccionar uno.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CurrentAngle**](currentangle-property.md)
</dt> </dl>

 

 



