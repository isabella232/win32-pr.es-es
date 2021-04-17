---
description: La propiedad subpictureon establece o recupera el estado actual de la subimagen (activada o desactivada).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Subimagenon (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688489"
---
# <a name="subpictureon-property"></a>Subimagenon (propiedad)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `SubpictureOn` propiedad establece o recupera el estado actual de la subimagen (activada o desactivada).

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si se muestra la subimagen.

## <a name="remarks"></a>Observaciones

Esta propiedad no afecta a la presentación de subtítulos cerrados. Los subtítulos están insertados en el flujo de vídeo. Las subimágenes de DVD se transportan en una secuencia independiente.

Cuando se cambia la secuencia de subimagen mediante [**CurrentSubpictureStream**](currentsubpicturestream-property.md), la `SubpictureOn` propiedad cambia a **true**.

Esta propiedad es de lectura/escritura y su valor predeterminado es false.

 

 



