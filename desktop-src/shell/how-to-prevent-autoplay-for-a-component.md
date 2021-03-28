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
# <a name="how-to-prevent-autoplay-for-a-component"></a><span data-ttu-id="b1b04-103">Cómo evitar la reproducción automática de un componente</span><span class="sxs-lookup"><span data-stu-id="b1b04-103">How to Prevent AutoPlay for a Component</span></span>

<span data-ttu-id="b1b04-104">Ilustra qué clave del registro debe establecerse para evitar la reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="b1b04-104">Illustrates which registry key must be set to prevent AutoPlay.</span></span>

## <a name="instructions"></a><span data-ttu-id="b1b04-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="b1b04-105">Instructions</span></span>


<span data-ttu-id="b1b04-106">Para evitar que la reproducción automática se inicie en respuesta a un evento, agregue el siguiente valor **reg \_ SZ** , tal como se muestra en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b1b04-106">To prevent AutoPlay from launching in response to an event, add the following **REG\_SZ** value, as shown in this example.</span></span>

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

<span data-ttu-id="b1b04-107">El valor es el identificador de clase (CLSID) en el que se conoce el componente que genera el evento en la tabla de objetos en ejecución (ROT).</span><span class="sxs-lookup"><span data-stu-id="b1b04-107">The value is the class identifier (CLSID) that the component that is generating the event is known by in the running object table (ROT).</span></span> <span data-ttu-id="b1b04-108">El valor no tiene datos.</span><span class="sxs-lookup"><span data-stu-id="b1b04-108">The value has no data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1b04-109">Bajo esta clave, los CLSID no se incluyen entre llaves ( {} ).</span><span class="sxs-lookup"><span data-stu-id="b1b04-109">Under this key, the CLSIDs are not enclosed in braces ( {} ).</span></span>

 

 

 



