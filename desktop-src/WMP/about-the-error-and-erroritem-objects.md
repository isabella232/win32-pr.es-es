---
title: Acerca de los objetos error y ErrorItem
description: Acerca de los objetos error y ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Media Player de Windows, objeto error
- Modelo de objetos de Windows Media Player, objeto error
- modelo de objetos, error (objeto)
- Control ActiveX de Windows Media Player, objeto error
- Control ActiveX, error (objeto)
- Control ActiveX móvil de Windows Media Player, objeto error
- Windows Media Player Mobile, error (objeto)
- Objeto de error
- Media Player de Windows, objeto ErrorItem
- Modelo de objetos de Media Player de Windows, objeto ErrorItem
- modelo de objetos, ErrorItem (objeto)
- Control ActiveX de Windows Media Player, objeto ErrorItem
- Control ActiveX, objeto ErrorItem
- Control ActiveX de Windows Media Player Mobile, objeto ErrorItem
- Windows Media Player Mobile, objeto ErrorItem
- Objeto ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357213"
---
# <a name="about-the-error-and-erroritem-objects"></a><span data-ttu-id="ebd73-119">Acerca de los objetos error y ErrorItem</span><span class="sxs-lookup"><span data-stu-id="ebd73-119">About the Error and ErrorItem Objects</span></span>

<span data-ttu-id="ebd73-120">Los objetos **error** y **ErrorItem** rigen las capacidades de control de errores de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ebd73-120">The **Error** and **ErrorItem** objects govern the error-handling capabilities of Windows Media Player.</span></span> <span data-ttu-id="ebd73-121">El objeto de **error** se obtiene del objeto **Player** a través de la propiedad **error** .</span><span class="sxs-lookup"><span data-stu-id="ebd73-121">The **Error** object is obtained from the **Player** object through the **error** property.</span></span> <span data-ttu-id="ebd73-122">Puede obtener un código específico del objeto de **error** mediante la propiedad **Item** del objeto **error** para crear el objeto **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="ebd73-122">You can get a specific code from the **Error** object by using the **item** property of the **Error** object to create the **ErrorItem** object.</span></span> <span data-ttu-id="ebd73-123">Por ejemplo, para obtener el código de error del primer elemento de error, escriba:</span><span class="sxs-lookup"><span data-stu-id="ebd73-123">For example, to get the error code of the first error item, type:</span></span>


```C++
myerrorcode = player.error.item(0).errorCode;

```



<span data-ttu-id="ebd73-124">También puede invocar la ayuda web con el objeto de **error** mediante el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="ebd73-124">You can also invoke Web Help with the **Error** object by using the following code:</span></span>


```C++
player.error.webHelp();

```



## <a name="related-topics"></a><span data-ttu-id="ebd73-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebd73-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebd73-126">**Objeto de error**</span><span class="sxs-lookup"><span data-stu-id="ebd73-126">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="ebd73-127">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="ebd73-127">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="ebd73-128">**Modelo de objetos del reproductor para lenguajes de scripting**</span><span class="sxs-lookup"><span data-stu-id="ebd73-128">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




