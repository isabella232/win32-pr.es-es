---
description: El método PlayForwards inicia la reproducción hacia delante desde la ubicación actual a la velocidad especificada.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Método PlayForwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e607779147ba057b9cfd747ebfe827a25e294e2b04cdfa7e61a0691ecf293c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830635"
---
# <a name="playforwards-method"></a>Método PlayForwards

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `PlayForwards` método inicia la reproducción hacia delante desde la ubicación actual a la velocidad especificada.

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Especifica la velocidad a la que se va a reproducir como un valor entero. Este valor es un multiplicador: 1,0 es la velocidad de reproducción normal; 2.0 es doble velocidad, 0.5 es de media velocidad, y así sucesivamente. Cuando **nSpeed** no es igual a 1.0, el audio se muted y la subpicture está desactivada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlayBackwards**](playbackwards-method.md)
</dt> </dl>

 

 



