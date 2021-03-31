---
description: La propiedad TotalTitleTime recupera el tiempo total de reproducción del título actual.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Propiedad TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910406"
---
# <a name="totaltitletime-property"></a>Propiedad TotalTitleTime

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `TotalTitleTime` propiedad recupera el tiempo total de reproducción del título actual.

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a>Valor devuelto

Devuelve el tiempo total de reproducción del título actual como una cadena con el formato "HH: mm: SS: FF".

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado. La cadena devuelta tendrá 11 caracteres de longitud en el formato "HH: mm: SS: FF" (horas, minutos, segundos, fotogramas).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**PlayAtTimeInTitle**](playattimeintitle-method.md)
</dt> </dl>

 

 



