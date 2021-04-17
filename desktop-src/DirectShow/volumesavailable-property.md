---
description: La propiedad VolumesAvailable recupera el número de volúmenes de un conjunto de varios volúmenes.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Propiedad VolumesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccdcf32ba8b7bea3958ef469bc0f90f9d41ecc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687860"
---
# <a name="volumesavailable-property"></a>Propiedad VolumesAvailable

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `VolumesAvailable` propiedad recupera el número de volúmenes de un conjunto de varios volúmenes.

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a>Valor devuelto

Devuelve el número de volúmenes del conjunto como un entero.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado. Algunos títulos de DVD se pueden publicar como una serie o conjunto de varios discos. Utilice este método para determinar el número de volumen del disco actual.

 

 



