---
description: La propiedad WindowlessActivation inicializa el objeto MSWebDVD en tiempo de diseño para el modo sin ventanas o sin ventanas.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Propiedad WindowlessActivation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6915dbf2ddcfe1b8925ccc1dc3c163799563d137e39e6d6260ad75f5496a0b1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982255"
---
# <a name="windowlessactivation-property"></a>Propiedad WindowlessActivation

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `WindowlessActivation` propiedad inicializa el objeto **MSWebDVD** en tiempo de diseño para el modo sin ventanas o sin ventanas.

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a>Valor devuelto

Devuelve si el objeto está en modo de ventana como un valor booleano.

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura con un valor predeterminado de true. Por lo tanto, solo tiene que establecer esta propiedad si ejecuta el objeto **MSWebDVD** en un contenedor con ventanas. Cuando se encuentra en una página web de Microsoft® Internet Explorer **MSWebDVD** siempre está en modo sin ventanas y no es necesario establecer esta propiedad.

 

 



