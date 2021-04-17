---
description: El método StillOff reanuda la reproducción y cancela el modo todavía.
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: Método StillOff
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687868"
---
# <a name="stilloff-method"></a>Método StillOff

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `StillOff` método reanuda la reproducción y cancela el modo todavía.

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El [navegador de DVD](dvd-navigator-filter.md) entra en modo todavía cuando encuentra un marco fijo creado en el disco. Notifica a la aplicación mediante el envío de un \_ DVD \_ de EC todavía \_ en el evento. El modo todavía es diferente del explorador de DVD que se encuentra en un estado de pausa debido a una operación de usuario. La llamada a `StillOff` reanuda la reproducción del modo todavía, pero no reinicia el navegador de DVD cuando está en un estado de pausa.

 

 



