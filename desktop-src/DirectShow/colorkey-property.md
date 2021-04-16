---
description: La propiedad ColorKey establece o recupera la clave de color utilizada en los subtítulos (CC).
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Propiedad ColorKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494638"
---
# <a name="colorkey-property"></a>Propiedad ColorKey

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `ColorKey` propiedad establece o recupera la clave de color utilizada en los subtítulos (CC).

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el color que se va a usar como fondo transparente para el texto con título cerrado. El valor predeterminado en 256 colores es magenta y está fuera de negro en cualquier otra profundidad de color.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura y escritura. Esta propiedad solo se aplica a los subtítulos (CC), si existen, no a la secuencia de la subimagen.

 

 



