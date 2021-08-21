---
description: La propiedad FullScreenMode establece o recupera un valor que indica si la pantalla está en modo de pantalla completa.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Propiedad FullScreenMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 103938afa6710b858329147eafadec4e06fd7d2ba244b896dd1ac39c74cd12c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015623"
---
# <a name="fullscreenmode-property"></a>Propiedad FullScreenMode

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `FullScreenMode` propiedad establece o recupera un valor que indica si la pantalla está en modo de pantalla completa.

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si se debe habilitar o deshabilitar la reproducción a pantalla completa.

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura con un valor predeterminado de false.



| Valor | Descripción                                            |
|-------|--------------------------------------------------------|
| true  | Habilite la reproducción a pantalla completa. Este es el valor predeterminado |
| false | Deshabilite la reproducción a pantalla completa.                          |



 

El modo de pantalla completa solo está disponible cuando el control MSWebDVD se ejecuta en modo de ventana.

 

 



