---
description: El evento UpdateOverlay se envía cuando se ha movido o cambiado el tamaño de la superficie de superposición o si su clave de color ha cambiado.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (Ddraw.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 205b4ca002ec06862b006dc3e3b6facec2f5cb7f0ffb92f3e5a65bc2bb0a161c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650834"
---
# <a name="updateoverlay"></a>UpdateOverlay

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El **evento UpdateOverlay** se envía cuando se ha movido o cambiado el tamaño de la superficie de superposición o si su clave de color ha cambiado.

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a>Comentarios

Las aplicaciones nunca deben preocuparse por el cambio de tamaño o el cambio de tamaño de la superficie superpuesta. Todo esto se controla internamente. Pero este evento también se envía cuando cambia la clave de color. Esto significa que si una aplicación hospeda MSWebDVD como control sin ventanas y muestra botones flotantes en la parte superior de la superficie de vídeo en modo de pantalla completa, debe responder a este evento obteniendo el nuevo valor de la **propiedad ColorKey** para que pueda dibujar los botones correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Ddraw.h</dt> </dl> |



 

 




