---
description: La propiedad TotalTitleTime recupera el tiempo total de reproducción del título actual.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Propiedad TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd809391394dc661745717ce7d173ad548dfd4d01206c07293024dc8e44a478
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650855"
---
# <a name="totaltitletime-property"></a>Propiedad TotalTitleTime

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `TotalTitleTime` propiedad recupera el tiempo total de reproducción del título actual.

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a>Valor devuelto

Devuelve el tiempo de reproducción total del título actual como una cadena con el formato "hh:mm:ss:ff".

## <a name="remarks"></a>Comentarios

Esta propiedad es de solo lectura sin ningún valor predeterminado. La cadena devuelta tendrá 11 caracteres con el formato "hh:mm:ss:ff" (horas, minutos, segundos, fotogramas).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**PlayAtTimeInTitle**](playattimeintitle-method.md)
</dt> </dl>

 

 



