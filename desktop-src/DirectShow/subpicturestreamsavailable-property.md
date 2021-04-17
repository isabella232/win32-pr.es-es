---
description: La propiedad SubpictureStreamsAvailable recupera el número de secuencias de subimagen disponibles en el título actual.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Propiedad SubpictureStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688488"
---
# <a name="subpicturestreamsavailable-property"></a>Propiedad SubpictureStreamsAvailable

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `SubpictureStreamsAvailable` propiedad recupera el número de secuencias de subimagen disponibles en el título actual.

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>Valor devuelto

Devuelve el número de flujos disponibles como un entero.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado. Para consultar cada secuencia para su atributo Language, llame primero a este método para obtener el límite superior.

La numeración de secuencias es de base cero.

 

 



