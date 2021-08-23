---
description: La propiedad ColorKey establece o recupera la clave de color usada en los subtítulos.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Propiedad ColorKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abca1dabbdb67f4380dbe32acbf2948862695b7c424dfd08629ec16237bb88c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073748"
---
# <a name="colorkey-property"></a>Propiedad ColorKey

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `ColorKey` propiedad establece o recupera la clave de color utilizada en los subtítulos.

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el color que se usará como fondo transparente para el texto con subtítulos. El valor predeterminado en 256 colores es el color rojo y el negro en cualquier otra profundidad de color.

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura. Esta propiedad solo se aplica a los subtítulos, si existen, no a la secuencia de subimagen.

 

 



