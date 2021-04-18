---
description: El evento UpdateOverlay se envía cuando se mueve o se cambia el tamaño de la superficie superpuesto, o cuando su clave de color ha cambiado.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (ddraw. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671723"
---
# <a name="updateoverlay"></a>UpdateOverlay

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El evento **UpdateOverlay** se envía cuando se mueve o se cambia el tamaño de la superficie superpuesto, o cuando su clave de color ha cambiado.

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a>Observaciones

Las aplicaciones nunca deben preocuparse por la superficie de superposición cuyo tamaño se ha cambiado o que se ha cambiado. Todo esto se controla internamente. Pero este evento también se envía cuando cambia la clave de color. Esto significa que si una aplicación hospeda MSWebDVD como un control sin ventana y muestra botones flotantes en la parte superior de la superficie de vídeo en el modo de pantalla completa, debe responder a este evento obteniendo el nuevo valor de la propiedad **ColorKey** para que pueda dibujar los botones correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Ddraw. h</dt> </dl> |



 

 




