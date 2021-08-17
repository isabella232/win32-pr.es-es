---
description: El método PlayAtTimeInTitle inicia la reproducción a la hora especificada dentro del título especificado.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: Método PlayAtTimeInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33640733f7333395a4affc4dedc0ae8db3e3558bf066584cb603dfc5f906f73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119291275"
---
# <a name="playattimeintitle-method"></a>Método PlayAtTimeInTitle

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `PlayAtTimeInTitle` método inicia la reproducción a la hora especificada dentro del título especificado.

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*Stime*
</dt> <dd>

Especifica la hora a la que se inicia la reproducción como una cadena. La cadena debe tener el formato "hh:mm:ss:ff" (especificando horas, minutos, segundos, fotogramas).

</dd> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica el índice del título como entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CurrentTitle**](currenttitle-property.md)
</dt> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**TitlesAvailable**](titlesavailable-property.md)
</dt> </dl>

 

 



