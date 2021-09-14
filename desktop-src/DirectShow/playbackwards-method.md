---
description: El método PlayBackwards inicia la reproducción hacia atrás desde la ubicación actual a la velocidad especificada.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Método PlayBackwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b396c3829569d3f3ad25f0c0e8718dfd23f268
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061001"
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

Especifica la velocidad a la que se va a reproducir como un número. Este número es un multiplicador: 1,0 es la velocidad de reproducción normal; 2.0 es de doble velocidad, 0.5 es de media velocidad, y así sucesivamente. Cuando **nSpeed** no es igual a 1,0, el audio se silencia y la subaspección se apaga.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PlayForwards**](playforwards-method.md)
</dt> </dl>

 

 



