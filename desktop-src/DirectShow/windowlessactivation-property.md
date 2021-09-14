---
description: La propiedad WindowlessActivation inicializa el objeto MSWebDVD en tiempo de diseño para el modo sin ventanas o sin ventanas.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Propiedad WindowlessActivation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272644"
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

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura y escritura con un valor predeterminado de true. Por lo tanto, solo tiene que establecer esta propiedad si ejecuta el objeto **MSWebDVD** en un contenedor con ventanas. Cuando se encuentra en una página web de Microsoft® Internet Explorer, **MSWebDVD** siempre está en modo sin ventanas y no es necesario establecer esta propiedad.

 

 



