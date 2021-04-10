---
description: La propiedad PreferredSubpictureStream recupera la secuencia de subimagen preferida para la sesión de visualización actual.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Propiedad PreferredSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23377d74d3632c665b001ae415dc151ca73bd148
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906602"
---
# <a name="preferredsubpicturestream-property"></a>Propiedad PreferredSubpictureStream

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `PreferredSubpictureStream` propiedad recupera la secuencia de subimagen preferida para la sesión de visualización actual.

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa la secuencia de la subimagen preferida actual en el registro del sistema.

## <a name="remarks"></a>Observaciones

La secuencia de subimagen preferida se establece con [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)del objeto [MSDVDAdm](msdvdadm-object.md) .

 

 



