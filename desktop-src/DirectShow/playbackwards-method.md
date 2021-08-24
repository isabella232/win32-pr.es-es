---
description: El método PlayBackwards inicia la reproducción hacia atrás desde la ubicación actual a la velocidad especificada.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Método PlayBackwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7236c225858d9508da0074ea64d104a50632b772302f42362dae373a987c352
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748365"
---
# <a name="playbackwards-method"></a>Método PlayBackwards

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `PlayBackwards` método inicia la reproducción hacia atrás desde la ubicación actual a la velocidad especificada.

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Especifica la velocidad a la que se va a reproducir como un número. Este número es un multiplicador: 1,0 es la velocidad de reproducción normal; 2.0 es de doble velocidad, 0.5 es de media velocidad, y así sucesivamente. Cuando **nSpeed** no es igual a 1,0, el audio se silencia y se apaga la subaspección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlayForwards**](playforwards-method.md)
</dt> </dl>

 

 



