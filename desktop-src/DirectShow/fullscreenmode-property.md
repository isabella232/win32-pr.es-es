---
description: La propiedad FullScreenMode establece o recupera un valor que indica si la presentación está en modo de pantalla completa.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Propiedad FullScreenMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152014"
---
# <a name="fullscreenmode-property"></a>Propiedad FullScreenMode

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `FullScreenMode` propiedad establece o recupera un valor que indica si la presentación está en modo de pantalla completa.

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si se va a habilitar o deshabilitar la reproducción de pantalla completa.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura/escritura y su valor predeterminado es false.



| Value | Descripción                                            |
|-------|--------------------------------------------------------|
| true  | Habilitar la reproducción a pantalla completa. Este es el valor predeterminado |
| false | Deshabilite la reproducción de pantalla completa.                          |



 

El modo de pantalla completa solo está disponible cuando el control MSWebDVD se está ejecutando en modo de ventana.

 

 



