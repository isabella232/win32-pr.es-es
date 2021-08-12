---
description: La propiedad VolumesAvailable recupera el número de volúmenes de un conjunto multivolume.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Propiedad VolumesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0ab5b07f30e49f1bbe7655a2d66d9aaa683099df64cadf94b5dfffdd3b3af0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650942"
---
# <a name="volumesavailable-property"></a>Propiedad VolumesAvailable

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `VolumesAvailable` propiedad recupera el número de volúmenes de un conjunto multivolume.

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a>Valor devuelto

Devuelve el número de volúmenes del conjunto como entero.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura sin ningún valor predeterminado. Algunos títulos de DVD se pueden publicar como un conjunto o serie multidiscos. Use este método para determinar el número de volumen del disco actual.

 

 



