---
description: La propiedad SubpictureOn establece o recupera el estado de subimagen actual (on o off).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Propiedad SubpictureOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692df6b69bc960562e9acd223a0e4e156fe00de2206146f609ba15d550b7a961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951774"
---
# <a name="subpictureon-property"></a>Propiedad SubpictureOn

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `SubpictureOn` propiedad establece o recupera el estado de subaspección actual (on o off).

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si se muestra la subaspección.

## <a name="remarks"></a>Comentarios

Esta propiedad no afecta a la presentación de subtítulos. Los títulos cerrados se insertan en la secuencia de vídeo. Las subapicuras de DVD se transportan en una secuencia independiente.

Cuando se cambia la secuencia de subimagen mediante [**CurrentSubpictureStream**](currentsubpicturestream-property.md), la `SubpictureOn` propiedad alterna a **True.**

Esta propiedad es de lectura y escritura con un valor predeterminado de false.

 

 



