---
title: Arquitectura de Download Manager
description: Arquitectura de Download Manager
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
- arquitectura del administrador de descargas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774095"
---
# <a name="download-manager-architecture"></a><span data-ttu-id="5215a-110">Arquitectura de Download Manager</span><span class="sxs-lookup"><span data-stu-id="5215a-110">Download Manager Architecture</span></span>

<span data-ttu-id="5215a-111">El administrador de descargas de Windows Media Player usa la tecnología COM.</span><span class="sxs-lookup"><span data-stu-id="5215a-111">The Windows Media Player Download Manager uses COM technology.</span></span> <span data-ttu-id="5215a-112">La funcionalidad se divide en un conjunto de interfaces de programación; puede escribir código de programación que use estas interfaces mediante Microsoft JScript o C++.</span><span class="sxs-lookup"><span data-stu-id="5215a-112">The functionality is distilled into a set of programming interfaces; you can write programming code that uses these interfaces by using Microsoft JScript or C++.</span></span>

<span data-ttu-id="5215a-113">Los lenguajes de scripting usan el concepto de objetos para dividir la funcionalidad de programación.</span><span class="sxs-lookup"><span data-stu-id="5215a-113">The scripting languages use the concept of objects to divide programming functionality.</span></span> <span data-ttu-id="5215a-114">El modelo de objetos **Downloadmanager** utiliza varios objetos para dividir los métodos y las propiedades en una organización lógica que agrupa las funciones relacionadas semánticamente.</span><span class="sxs-lookup"><span data-stu-id="5215a-114">The **DownloadManager** object model uses several objects to divide the methods and properties into a logical organization that groups semantically related functions together.</span></span> <span data-ttu-id="5215a-115">Las secciones siguientes contienen información sobre los objetos del administrador de descargas.</span><span class="sxs-lookup"><span data-stu-id="5215a-115">The following sections contain information about the Download Manager objects.</span></span>



| <span data-ttu-id="5215a-116">Sección</span><span class="sxs-lookup"><span data-stu-id="5215a-116">Section</span></span>                                                                     | <span data-ttu-id="5215a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5215a-117">Description</span></span>                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5215a-118">Acerca del objeto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="5215a-118">About the DownloadManager Object</span></span>](#about-the-downloadmanager-object)       | <span data-ttu-id="5215a-119">El objeto **Downloadmanager** representa el objeto raíz para el administrador de descargas de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5215a-119">The **DownloadManager** object represents the root object for the Windows Media Player Download Manager.</span></span> |
| [<span data-ttu-id="5215a-120">Acerca del objeto DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="5215a-120">About the DownloadCollection Object</span></span>](#about-the-downloadcollection-object) | <span data-ttu-id="5215a-121">El objeto **DownloadCollection** representa una colección de elementos de descarga.</span><span class="sxs-lookup"><span data-stu-id="5215a-121">The **DownloadCollection** object represents a collection of download items.</span></span>                             |
| [<span data-ttu-id="5215a-122">Acerca del objeto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="5215a-122">About the DownloadItem Object</span></span>](#about-the-downloaditem-object)             | <span data-ttu-id="5215a-123">El objeto **DownloadItem** representa una solicitud de descarga individual.</span><span class="sxs-lookup"><span data-stu-id="5215a-123">The **DownloadItem** object represents an individual download request.</span></span>                                   |



 

## <a name="about-the-downloadmanager-object"></a><span data-ttu-id="5215a-124">Acerca del objeto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="5215a-124">About the DownloadManager Object</span></span>

<span data-ttu-id="5215a-125">**Downloadmanager** es el objeto raíz para el administrador de descargas de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5215a-125">**DownloadManager** is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="5215a-126">Se tiene acceso a todos los demás objetos a través de este objeto.</span><span class="sxs-lookup"><span data-stu-id="5215a-126">All other objects are accessed through this object.</span></span> <span data-ttu-id="5215a-127">Para obtener acceso al objeto **Downloadmanager** , use la siguiente sintaxis de JScript:</span><span class="sxs-lookup"><span data-stu-id="5215a-127">To gain access to the **DownloadManager** object, use the following JScript syntax:</span></span>


```C++
var DownloadManager = external.DownloadManager;
```



<span data-ttu-id="5215a-128">Esto crea una instancia del objeto **Downloadmanager** , que se puede usar para recuperar los objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="5215a-128">This creates an instance of the **DownloadManager** object, which can then be used to retrieve the child objects.</span></span> <span data-ttu-id="5215a-129">Por ejemplo, la siguiente sintaxis recupera el primer elemento de la colección de descarga que tiene el identificador número 253675:</span><span class="sxs-lookup"><span data-stu-id="5215a-129">For example, the following syntax retrieves the first item from the download collection that has id number 253675:</span></span>


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a><span data-ttu-id="5215a-130">Acerca del objeto DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="5215a-130">About the DownloadCollection Object</span></span>

<span data-ttu-id="5215a-131">El objeto **DownloadCollection** representa una colección de archivos que se van a descargar.</span><span class="sxs-lookup"><span data-stu-id="5215a-131">The **DownloadCollection** object represents a collection of files to be downloaded.</span></span> <span data-ttu-id="5215a-132">Puede utilizar este objeto para determinar el número de descargas que hay en la colección, quitar elementos de la colección, recuperar un elemento de descarga específico e iniciar una nueva descarga.</span><span class="sxs-lookup"><span data-stu-id="5215a-132">You can use this object to determine how many downloads are in the collection, remove items from the collection, retrieve a specific download item, and to start a new download.</span></span> <span data-ttu-id="5215a-133">Al iniciar una nueva descarga, se agrega automáticamente la descarga a la colección.</span><span class="sxs-lookup"><span data-stu-id="5215a-133">Starting a new download automatically adds the download to the collection.</span></span>

## <a name="about-the-downloaditem-object"></a><span data-ttu-id="5215a-134">Acerca del objeto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="5215a-134">About the DownloadItem Object</span></span>

<span data-ttu-id="5215a-135">El objeto **DownloadItem** representa una descarga individual.</span><span class="sxs-lookup"><span data-stu-id="5215a-135">The **DownloadItem** object represents an individual download.</span></span> <span data-ttu-id="5215a-136">Los elementos de descarga siempre existen como parte de una colección de descargas.</span><span class="sxs-lookup"><span data-stu-id="5215a-136">Download items always exist as part of a download collection.</span></span> <span data-ttu-id="5215a-137">Utilice este objeto para recuperar información sobre el elemento de descarga y para pausar, reanudar o cancelar la descarga en curso.</span><span class="sxs-lookup"><span data-stu-id="5215a-137">Use this object to retrieve information about the download item and to pause, resume, or cancel the download in progress.</span></span>

<span data-ttu-id="5215a-138">Al cancelar una descarga, el elemento de descarga permanece en su lugar en la colección de descargas.</span><span class="sxs-lookup"><span data-stu-id="5215a-138">When you cancel a download, the download item remains in place in its download collection.</span></span> <span data-ttu-id="5215a-139">En este caso, **downloadCollection**. **downloadState** recupera un valor de 4, lo que significa que se canceló.</span><span class="sxs-lookup"><span data-stu-id="5215a-139">In this case, **downloadCollection**.**downloadState** retrieves a value of 4, meaning canceled.</span></span>

<span data-ttu-id="5215a-140">Puede usar **downloadItem**. **progreso** para informar al usuario sobre la cantidad del archivo que se ha transferido o la cantidad de tiempo que se va a descargar.</span><span class="sxs-lookup"><span data-stu-id="5215a-140">You can use **downloadItem**.**progress** to inform the user about how much of the file has been transferred or how much remains to be downloaded.</span></span> <span data-ttu-id="5215a-141">Puede usar este valor para calcular también el tiempo restante.</span><span class="sxs-lookup"><span data-stu-id="5215a-141">You might use this value to estimate the time remaining as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5215a-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5215a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5215a-143">**Administrador de descargas**</span><span class="sxs-lookup"><span data-stu-id="5215a-143">**Download Manager**</span></span>](download-manager.md)
</dt> </dl>

 

 




