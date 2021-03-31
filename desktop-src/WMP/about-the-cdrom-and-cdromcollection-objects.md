---
title: Acerca de los objetos CDROM y CdromCollection
description: Acerca de los objetos CDROM y CdromCollection
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Media Player de Windows, objeto CDROM
- Modelo de objetos de Windows Media Player, objeto CDROM
- modelo de objetos, CDROM (objeto)
- Control ActiveX de Windows Media Player, objeto CDROM
- Control ActiveX, CDROM (objeto)
- Control ActiveX móvil de Windows Media Player, objeto CDROM
- Windows Media Player Mobile, objeto CDROM
- CDROM (objeto)
- Media Player de Windows, objeto CdromCollection
- Modelo de objetos de Media Player de Windows, objeto CdromCollection
- modelo de objetos, CdromCollection (objeto)
- Control ActiveX de Windows Media Player, objeto CdromCollection
- Control ActiveX, objeto CdromCollection
- Control ActiveX de Windows Media Player Mobile, objeto CdromCollection
- Windows Media Player Mobile, objeto CdromCollection
- Objeto CdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776938"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a><span data-ttu-id="52716-119">Acerca de los objetos CDROM y CdromCollection</span><span class="sxs-lookup"><span data-stu-id="52716-119">About the Cdrom and CdromCollection Objects</span></span>

<span data-ttu-id="52716-120">Los objetos **CDROM** y **CdromCollection** rigen la interfaz a las unidades de CD del equipo con el fin de leer y reproducir CDs.</span><span class="sxs-lookup"><span data-stu-id="52716-120">The **Cdrom** and **CdromCollection** objects govern the interface to the CD drives in your computer for purposes of reading and playing CDs.</span></span>

<span data-ttu-id="52716-121">Solo se tiene acceso al objeto **CdromCollection** a través de la propiedad **CdromCollection** del objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="52716-121">The **CdromCollection** object is accessed only through the **cdromCollection** property of the **Player** object.</span></span> <span data-ttu-id="52716-122">La propiedad **cdromCollection** devuelve el objeto **cdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="52716-122">The **cdromCollection** property returns the **CdromCollection** object.</span></span> <span data-ttu-id="52716-123">Solo puede acceder a las propiedades del objeto **CdromCollection** una vez creado.</span><span class="sxs-lookup"><span data-stu-id="52716-123">You can only access the properties of the **CdromCollection** object after you have created it.</span></span> <span data-ttu-id="52716-124">Por ejemplo, para utilizar la propiedad **Count** , debe usar el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="52716-124">For example, to use the **count** property, you must use the following code:</span></span>


```C++
mycount = player.cdromcollection.count;
```



<span data-ttu-id="52716-125">Solo puede acceder al objeto **CDROM** a través del objeto **CdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="52716-125">You can only access the **Cdrom** object through the **CdromCollection** object.</span></span> <span data-ttu-id="52716-126">Por ejemplo, para expulsar el CD con el método **EJECT** , primero debe crear el objeto de colección y, a continuación, un elemento en el objeto.</span><span class="sxs-lookup"><span data-stu-id="52716-126">For example, to eject the CD by using the **Eject** method, you must first create the collection object and then an item in the object.</span></span> <span data-ttu-id="52716-127">Para expulsar el CD, use el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="52716-127">To eject the CD, use the following code:</span></span>


```C++
player.cdromcollection.item(0).eject();
```



<span data-ttu-id="52716-128">En ambos casos, primero se crea el objeto de colección (**CdromCollection**) y, a continuación, se obtiene un objeto específico de esa colección.</span><span class="sxs-lookup"><span data-stu-id="52716-128">In both cases, you are first creating the collection object (**CdromCollection**) and then getting a specific object of that collection.</span></span> <span data-ttu-id="52716-129">El objeto es el primer elemento de la colección, **Item**(0), que corresponde a la primera unidad de CD.</span><span class="sxs-lookup"><span data-stu-id="52716-129">The object is the first item in the collection, **Item**(0), which corresponds to the first CD drive.</span></span> <span data-ttu-id="52716-130">A continuación, llame a un método, **EJECT**, en ese elemento.</span><span class="sxs-lookup"><span data-stu-id="52716-130">You then call a method, **Eject**, on that item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52716-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52716-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52716-132">**CDROM (objeto)**</span><span class="sxs-lookup"><span data-stu-id="52716-132">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="52716-133">**Objeto CdromCollection**</span><span class="sxs-lookup"><span data-stu-id="52716-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="52716-134">**Modelo de objetos del reproductor para lenguajes de scripting**</span><span class="sxs-lookup"><span data-stu-id="52716-134">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




