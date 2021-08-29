---
description: El método StillOff reanuda la reproducción y cancela el modo still.
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: StillOff (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf63409cb435e0e72cb9ebcb856df7956270dc92931366f575c1fb02df9315a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050216"
---
# <a name="stilloff-method"></a>StillOff (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `StillOff` método reanuda la reproducción y cancela el modo still.

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El [navegador de DVD](dvd-navigator-filter.md) entra en modo "still" cuando encuentra un fotograma todavía escrito en el disco. Notifica a la aplicación mediante el envío de un evento \_ EC DVD \_ STILL \_ ON. El modo still es diferente del navegador de DVD que está en estado pausado debido a una operación del usuario. Al llamar a , se reanuda la reproducción desde el modo todavía, pero no se reinicia el navegador de DVD cuando está `StillOff` en estado en pausa.

 

 



