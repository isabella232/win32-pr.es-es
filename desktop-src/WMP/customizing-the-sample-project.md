---
title: Personalización del proyecto de ejemplo
description: Personalización del proyecto de ejemplo
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player tiendas en línea, personalizar proyectos de ejemplo
- tiendas en línea, personalizar proyectos de ejemplo
- tipo 2 tiendas en línea, personalizar proyectos de ejemplo
- Windows Media Player tiendas en línea, proyectos de ejemplo
- tiendas en línea, proyectos de ejemplo
- tipo 2 tiendas en línea, proyectos de ejemplo
- personalizar proyectos de ejemplo
- ejemplos, tipo 2 tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeec3ebcb74304cd5181783e9c457d6a149b0cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994515"
---
# <a name="customizing-the-sample-project"></a><span data-ttu-id="b43a4-111">Personalización del proyecto de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b43a4-111">Customizing the Sample Project</span></span>

<span data-ttu-id="b43a4-112">Al crear su propia tienda en línea, querrá cambiar las implementaciones de los siguientes métodos en el archivo denominado YourProject. cpp:</span><span class="sxs-lookup"><span data-stu-id="b43a4-112">When creating your own online store, you will want to change the implementations of the following methods in the file named YourProject.cpp:</span></span>

-   <span data-ttu-id="b43a4-113">**CYourProject:: allowPlay**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-113">**CYourProject::allowPlay**.</span></span> <span data-ttu-id="b43a4-114">Utilice esta función para aplicar las reglas de negocios para permitir la reproducción de contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="b43a4-114">Use this function to apply your business rules for permitting playback of protected content.</span></span>
-   <span data-ttu-id="b43a4-115">**CYourProject:: allow CDBurn**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-115">**CYourProject::allow CDBurn**.</span></span> <span data-ttu-id="b43a4-116">Utilice esta función para aplicar las reglas de negocios para permitir que los usuarios copien contenido protegido en un CD.</span><span class="sxs-lookup"><span data-stu-id="b43a4-116">Use this function to apply your business rules for allowing users to copy protected content to a CD.</span></span>
-   <span data-ttu-id="b43a4-117">**CYourProject:: allowPDATransfer**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-117">**CYourProject::allowPDATransfer**.</span></span> <span data-ttu-id="b43a4-118">Utilice esta función para aplicar las reglas de negocios para permitir que los usuarios transfieran contenido protegido a un dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="b43a4-118">Use this function to apply your business rules for allowing users to transfer protected content to a portable device.</span></span>
-   <span data-ttu-id="b43a4-119">**CYourProject:: startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-119">**CYourProject::startBackgroundProcessing**.</span></span> <span data-ttu-id="b43a4-120">Utilice esta función para iniciar las tareas de procesamiento en segundo plano que necesite.</span><span class="sxs-lookup"><span data-stu-id="b43a4-120">Use this function to initiate any background processing tasks you require.</span></span> <span data-ttu-id="b43a4-121">Por ejemplo, podría usarlo como una oportunidad para comprobar las licencias caducadas.</span><span class="sxs-lookup"><span data-stu-id="b43a4-121">For example, you might use this as an opportunity to check for expired licenses.</span></span>
-   <span data-ttu-id="b43a4-122">**CYourProject::D eviceavailable**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-122">**CYourProject::deviceAvailable**.</span></span> <span data-ttu-id="b43a4-123">Use esta función para iniciar cualquier tarea relacionada con un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="b43a4-123">Use this function to initiate any tasks related to a connected device.</span></span>
-   <span data-ttu-id="b43a4-124">**CYourProject::P repareforsync**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-124">**CYourProject::prepareForSync**.</span></span> <span data-ttu-id="b43a4-125">Utilice esta función para realizar las tareas necesarias justo antes de sincronizar los medios digitales con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b43a4-125">Use this function to perform necessary tasks just before synchronizing digital media to the device.</span></span>
-   <span data-ttu-id="b43a4-126">**CYourProject:: serviceEvent**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-126">**CYourProject::serviceEvent**.</span></span> <span data-ttu-id="b43a4-127">Utilice esta función para iniciar y finalizar las tareas que desea ejecutar cuando la tienda en línea sea la activa.</span><span class="sxs-lookup"><span data-stu-id="b43a4-127">Use this function to begin and end tasks that you want to run when your online store is the active one.</span></span>
-   <span data-ttu-id="b43a4-128">**CYourProject:: stopBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-128">**CYourProject::stopBackgroundProcessing**.</span></span> <span data-ttu-id="b43a4-129">Use esta función para detener las tareas de procesamiento en segundo plano que se iniciaron cuando Windows Media Player llamó a **CYourProject:: startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-129">Use this function to stop any background processing tasks you started when Windows Media Player called **CYourProject::startBackgroundProcessing**.</span></span>

## <a name="working-with-media-and-playlist-objects"></a><span data-ttu-id="b43a4-130">Trabajar con objetos multimedia y de lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="b43a4-130">Working with Media and Playlist Objects</span></span>

<span data-ttu-id="b43a4-131">El método **allowPlay** proporciona un puntero a la interfaz **IWMPMedia** como parámetro.</span><span class="sxs-lookup"><span data-stu-id="b43a4-131">The **allowPlay** method provides a pointer to the **IWMPMedia** interface as a parameter.</span></span> <span data-ttu-id="b43a4-132">Esta interfaz es la interfaz de Media Player de Windows que representa los objetos multimedia.</span><span class="sxs-lookup"><span data-stu-id="b43a4-132">This interface is the Windows Media Player interface that represents media objects.</span></span> <span data-ttu-id="b43a4-133">Al llamar a los métodos en esta interfaz, puede trabajar con los atributos y las propiedades de un elemento multimedia individual.</span><span class="sxs-lookup"><span data-stu-id="b43a4-133">By calling the methods on this interface, you can work with the attributes and properties of an individual media item.</span></span>

<span data-ttu-id="b43a4-134">Los métodos **allowCDBurn** y **allowPDATransfer** proporcionan un puntero a la interfaz **IWMPPlaylist** como parámetro.</span><span class="sxs-lookup"><span data-stu-id="b43a4-134">The **allowCDBurn** and **allowPDATransfer** methods provide a pointer to the **IWMPPlaylist** interface as a parameter.</span></span> <span data-ttu-id="b43a4-135">Esta interfaz es la interfaz de Media Player de Windows que representa los objetos de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b43a4-135">This interface is the Windows Media Player interface that represents playlist objects.</span></span> <span data-ttu-id="b43a4-136">Al llamar a los métodos en esta interfaz, puede trabajar con los atributos y las propiedades de una lista de reproducción, agregar elementos a una lista de reproducción o quitar elementos de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b43a4-136">By calling the methods on this interface, you can work with the attributes and properties of a playlist, add items to a playlist, or remove items from a playlist.</span></span>

<span data-ttu-id="b43a4-137">Para obtener información sobre cómo quitar un elemento de una lista de reproducción mediante programación, vea la implementación de **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-137">To learn how to remove an item from a playlist programmatically, see the implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span> <span data-ttu-id="b43a4-138">Para obtener más información sobre cómo trabajar con objetos multimedia y de lista de reproducción, vea [modelo de objetos de reproductor para lenguajes de scripting](player-object-model-for-scripting-languages.md).</span><span class="sxs-lookup"><span data-stu-id="b43a4-138">To learn more about working with media and playlist objects, see [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).</span></span>

## <a name="code-that-can-be-removed"></a><span data-ttu-id="b43a4-139">Código que se puede quitar</span><span class="sxs-lookup"><span data-stu-id="b43a4-139">Code That Can Be Removed</span></span>

<span data-ttu-id="b43a4-140">Probablemente querrá quitar el código que abre los cuadros de diálogo porque es improbable que quiera que los usuarios decidan qué elementos multimedia se pueden reproducir o copiar.</span><span class="sxs-lookup"><span data-stu-id="b43a4-140">You will probably want to remove the code that opens dialog boxes because it is unlikely that you will want users deciding which media items can be played or copied.</span></span> <span data-ttu-id="b43a4-141">En YourProject. h, quite el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="b43a4-141">From YourProject.h, remove the following code:</span></span>

-   <span data-ttu-id="b43a4-142">La declaración de **CAllowBaseDialog**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-142">The declaration of **CAllowBaseDialog**.</span></span>
-   <span data-ttu-id="b43a4-143">La declaración de **CAllowBurnDialog**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-143">The declaration of **CAllowBurnDialog**.</span></span>
-   <span data-ttu-id="b43a4-144">La declaración de **CAllowTransferDialog**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-144">The declaration of **CAllowTransferDialog**.</span></span>

<span data-ttu-id="b43a4-145">En YourProject. cpp, quite el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="b43a4-145">From YourProject.cpp, remove the following code:</span></span>

-   <span data-ttu-id="b43a4-146">Implementación de **CAllowBaseDialog <T> :: OnInitDialog**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-146">The implementation of **CAllowBaseDialog<T>::OnInitDialog**.</span></span>
-   <span data-ttu-id="b43a4-147">Implementación de **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="b43a4-147">The implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b43a4-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b43a4-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b43a4-149">**Compilar el complemento para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="b43a4-149">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




