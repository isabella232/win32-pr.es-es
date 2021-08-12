---
description: La propiedad CurrentVolume recupera el número de volumen del directorio raíz actual.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: CurrentVolume (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d07f9d82facc243654bad2e16e9a028e8cf920a51f15dd92cc879b0ea1340d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654622"
---
# <a name="currentvolume-property"></a>CurrentVolume (propiedad)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `CurrentVolume` propiedad recupera el número de volumen del directorio raíz actual.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el volumen de DVD actual. Si un disco forma parte de un conjunto de varios volúmenes, el valor entero debe ser mayor que cero.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura sin ningún valor predeterminado.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Volúmenes disponibles**](volumesavailable-property.md)
</dt> </dl>

 

 



