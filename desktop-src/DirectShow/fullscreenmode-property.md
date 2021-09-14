---
description: La propiedad FullScreenMode establece o recupera un valor que indica si la pantalla está en modo de pantalla completa.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Propiedad FullScreenMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061160"
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

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura y escritura con un valor predeterminado de false.



| Value | Descripción                                            |
|-------|--------------------------------------------------------|
| true  | Habilite la reproducción a pantalla completa. Este es el valor predeterminado |
| false | Deshabilite la reproducción a pantalla completa.                          |



 

El modo de pantalla completa solo está disponible cuando el control MSWebDVD se ejecuta en modo de ventana.

 

 



