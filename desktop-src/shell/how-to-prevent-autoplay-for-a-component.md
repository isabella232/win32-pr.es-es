---
description: Ilustra qué clave del registro debe establecerse para evitar la reproducción automática.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Cómo evitar la reproducción automática de un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebe03473ce7c5eb441ec428cbe4d060dc62f042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985426"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a>Cómo evitar la reproducción automática de un componente

Ilustra qué clave del registro debe establecerse para evitar la reproducción automática.

## <a name="instructions"></a>Instrucciones


Para evitar que la reproducción automática se inicie en respuesta a un evento, agregue el siguiente valor **reg \_ SZ** , tal como se muestra en este ejemplo.

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

El valor es el identificador de clase (CLSID) en el que se conoce el componente que genera el evento en la tabla de objetos en ejecución (ROT). El valor no tiene datos.

> [!IMPORTANT]
> Bajo esta clave, los CLSID no se incluyen entre llaves ( {} ).

 

 

 



