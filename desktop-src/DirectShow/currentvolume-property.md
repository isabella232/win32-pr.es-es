---
description: La propiedad CurrentVolume recupera el número de volumen del directorio raíz actual.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Propiedad CurrentVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677055"
---
# <a name="currentvolume-property"></a>Propiedad CurrentVolume

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `CurrentVolume` propiedad recupera el número de volumen del directorio raíz actual.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el volumen de DVD actual. Si un disco forma parte de un conjunto de varios volúmenes, el valor entero debe ser mayor que cero.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**VolumesAvailable**](volumesavailable-property.md)
</dt> </dl>

 

 



