---
description: El método PlayForwards inicia la reproducción hacia delante desde la ubicación actual a la velocidad especificada.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Método PlayForwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806247"
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

Especifica la velocidad a la que se reproducirá como valor entero. Este valor es un multiplicador: 1,0 es la velocidad de reproducción normal; 2,0 es la velocidad doble, 0,5 es la velocidad media, etc. Cuando **nSpeed** no es igual a 1,0, el audio se silencia y la subimagen se desactiva.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlayBackwards**](playbackwards-method.md)
</dt> </dl>

 

 



