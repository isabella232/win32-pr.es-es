---
description: Muestra qué clave del Registro debe establecerse para evitar la reproducción automática.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Cómo evitar la reproducción automática de un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b44817f6803c25bbf506a5f76c8b068c683af4b5d4c7536482c30cd3aee2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859692"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a>Cómo evitar la reproducción automática de un componente

Muestra qué clave del Registro debe establecerse para evitar la reproducción automática.

## <a name="instructions"></a>Instructions


Para evitar que la reproducción automática se inicie en respuesta a un evento, agregue el siguiente **valor REG \_ SZ,** como se muestra en este ejemplo.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

El valor es el identificador de clase (CLSID) que conoce el componente que genera el evento en la tabla de objetos en ejecución (ROT). El valor no tiene datos.

> [!IMPORTANT]
> En esta clave, los CLID no se incluyen entre llaves ( {} ).

 

 

 



