---
title: Controladores de eventos
description: Controladores de eventos
ms.assetid: abb5f123-b838-46fb-ab11-cee70cc76a38
keywords:
- Aspectos de Windows Media Player, controladores de eventos en JScript
- máscaras, controladores de eventos en JScript
- eventos, JScript
- Archivos JScript para máscaras, controladores de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec4413ae3a2358b01685cd0edfe66de92810a64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695228"
---
# <a name="event-handlers"></a><span data-ttu-id="1e909-107">Controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="1e909-107">Event Handlers</span></span>

<span data-ttu-id="1e909-108">Microsoft JScript se usa para procesar eventos en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="1e909-108">Microsoft JScript is used to process events in the skin definition file.</span></span> <span data-ttu-id="1e909-109">Consulte [control de eventos](handling-events.md) para obtener más información sobre los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="1e909-109">See [Handling Events](handling-events.md) for more information about event handlers.</span></span>

<span data-ttu-id="1e909-110">Puede tener más de una línea de código en un controlador de eventos, pero debe tener cuidado de no superar la longitud de línea que JScript permite.</span><span class="sxs-lookup"><span data-stu-id="1e909-110">You can have more than one line of code in an event handler, but care must be taken not to exceed the line length that JScript permits.</span></span> <span data-ttu-id="1e909-111">Separe las líneas mediante punto y coma.</span><span class="sxs-lookup"><span data-stu-id="1e909-111">Separate the lines by semicolons.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a><span data-ttu-id="1e909-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e909-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e909-113">**Usar JScript**</span><span class="sxs-lookup"><span data-stu-id="1e909-113">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




