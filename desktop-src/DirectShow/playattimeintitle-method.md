---
description: El método PlayAtTimeInTitle inicia la reproducción en el momento especificado dentro del título especificado.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: Método PlayAtTimeInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c40373b4327b6df5fc341ca392c223d464a70a8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061005"
---
# <a name="playattimeintitle-method"></a>Método PlayAtTimeInTitle

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `PlayAtTimeInTitle` método inicia la reproducción en el momento especificado dentro del título especificado.

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*Stime*
</dt> <dd>

Especifica la hora a la que se va a iniciar la reproducción como una cadena. La cadena debe tener el formato "hh:mm:ss:ff" (especificando horas, minutos, segundos, fotogramas).

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

 

 



