---
description: La propiedad AnglesAvailable recupera el número de ángulos disponibles actualmente.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Propiedad AnglesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659281"
---
# <a name="anglesavailable-property"></a>Propiedad AnglesAvailable

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `AnglesAvailable` propiedad recupera el número de ángulos disponibles actualmente.

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero comprendido entre 1 y 9 que representa el número de ángulos actualmente disponibles. Si


```
iAngles
```



= 1, no hay ningún bloque de ángulo en la ubicación actual.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado. Un *bloque de ángulo* es un segmento de vídeo que se ha captado desde más de un ángulo de cámara. Puede haber hasta nueve ángulos en un bloque de ángulo, numerados del 1 al 9. Cuando el navegador de DVD entra por primera vez en un bloque de ángulo, envía a la aplicación una \_ \_ notificación de eventos de los ángulos de DVD de EC \_ disponibles con el número de ángulos de *lParam1*. Se puede crear un disco para mostrar automáticamente un menú para los ángulos disponibles cuando entra en un bloque de ángulo, pero normalmente una aplicación debe determinar el número de ángulos disponibles y ofrecer al usuario una manera de seleccionar uno.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CurrentAngle**](currentangle-property.md)
</dt> </dl>

 

 



