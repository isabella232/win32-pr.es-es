---
description: La propiedad VolumesAvailable recupera el número de volúmenes de un conjunto multivolume.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Propiedad VolumesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccdcf32ba8b7bea3958ef469bc0f90f9d41ecc14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272751"
---
# <a name="volumesavailable-property"></a>Propiedad VolumesAvailable

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `VolumesAvailable` propiedad recupera el número de volúmenes de un conjunto multivolume.

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a>Valor devuelto

Devuelve el número de volúmenes del conjunto como un entero.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura sin ningún valor predeterminado. Algunos títulos de DVD se pueden publicar como un conjunto o serie multidisco. Use este método para determinar el número de volumen del disco actual.

 

 



