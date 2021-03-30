---
title: Propiedades, métodos y eventos
description: Propiedades, métodos y eventos
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Media Player de Windows, propiedades para el modelo de objetos
- Windows Media Player, métodos para el modelo de objetos
- Windows Media Player, eventos para el modelo de objetos
- Modelo de objetos de Windows Media Player, propiedades
- Modelo de objetos de Windows Media Player, métodos
- Modelo de objetos de Windows Media Player, eventos
- modelo de objetos, propiedades
- modelo de objetos, métodos
- modelo de objetos, eventos
- Control ActiveX de Windows Media Player, propiedades para el modelo de objetos
- Control ActiveX, propiedades del modelo de objetos
- Control ActiveX móvil de Windows Media Player, propiedades para el modelo de objetos
- Windows Media Player Mobile, propiedades para el modelo de objetos
- Control ActiveX de Windows Media Player, métodos para el modelo de objetos
- Control ActiveX, métodos para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, métodos para el modelo de objetos
- Windows Media Player Mobile, métodos para el modelo de objetos
- Control ActiveX de Windows Media Player, eventos para el modelo de objetos
- Control ActiveX, eventos para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, eventos para el modelo de objetos
- Windows Media Player Mobile, eventos para el modelo de objetos
- propiedades, modelo de objetos de Windows Media Player
- métodos, modelo de objetos de Windows Media Player
- eventos, modelo de objetos de Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148817"
---
# <a name="properties-methods-and-events"></a><span data-ttu-id="c27b3-127">Propiedades, métodos y eventos</span><span class="sxs-lookup"><span data-stu-id="c27b3-127">Properties, Methods and Events</span></span>

<span data-ttu-id="c27b3-128">Cada objeto tiene métodos y propiedades a través de los cuales puede programar el control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="c27b3-128">Each object has methods and properties through which you can program the Windows Media Player control.</span></span> <span data-ttu-id="c27b3-129">Un método es una acción que el objeto puede llevar A cabo.</span><span class="sxs-lookup"><span data-stu-id="c27b3-129">A method is an action that the object can take.</span></span> <span data-ttu-id="c27b3-130">Una propiedad es un valor de datos que puede leer o cambiar.</span><span class="sxs-lookup"><span data-stu-id="c27b3-130">A property is a data value that you can read or change.</span></span> <span data-ttu-id="c27b3-131">Por ejemplo, el método **Play** inicia el contenido que se reproduce y la propiedad de **velocidad** de fotogramas indica la velocidad de fotogramas actual del contenido que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="c27b3-131">For example, the **Play** method starts the content playing, and the **frameRate** property indicates the current frame rate of the content that is playing.</span></span>

<span data-ttu-id="c27b3-132">Además, el objeto **Player** genera eventos que le ofrecen la oportunidad de llevar a cabo acciones en momentos concretos.</span><span class="sxs-lookup"><span data-stu-id="c27b3-132">In addition, the **Player** object raises events that give you the opportunity to carry out actions at specific times.</span></span> <span data-ttu-id="c27b3-133">El código se escribe en un controlador de eventos que se ejecutará cuando Windows Media Player genere el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c27b3-133">You write code in an event handler that will execute when Windows Media Player raises the corresponding event.</span></span> <span data-ttu-id="c27b3-134">Por ejemplo, puede escribir código en un controlador de eventos **PlayStateChange** que determine si el cambio de estado es que el medio ha finalizado y, si es así, muestra un cuadro de diálogo preguntando a los usuarios si quieren reproducir el medio de nuevo.</span><span class="sxs-lookup"><span data-stu-id="c27b3-134">For example, you can write code in a **PlayStateChange** event handler that determines whether the change in state is that the media ended and if so display a dialog box asking users if they want to play the media again.</span></span>

> [!Note]  
> <span data-ttu-id="c27b3-135">Todos los métodos del modelo de objetos de Windows Media Player son asíncronos.</span><span class="sxs-lookup"><span data-stu-id="c27b3-135">All of the methods in the Windows Media Player object model are asynchronous.</span></span> <span data-ttu-id="c27b3-136">Si llama a dos métodos en el mismo procedimiento, el segundo método no puede confiar en el primer método que ha completado su acción.</span><span class="sxs-lookup"><span data-stu-id="c27b3-136">If you call two methods in the same procedure, the second method cannot rely on the first method having completed its action.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c27b3-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c27b3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c27b3-138">**Acerca del modelo de objetos de Player**</span><span class="sxs-lookup"><span data-stu-id="c27b3-138">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




