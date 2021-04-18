---
description: Trabajar con búferes de medios DMO
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Trabajar con búferes de medios DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707539"
---
# <a name="working-with-dmo-media-buffers"></a><span data-ttu-id="71c9c-103">Trabajar con búferes de medios DMO</span><span class="sxs-lookup"><span data-stu-id="71c9c-103">Working with DMO Media Buffers</span></span>

<span data-ttu-id="71c9c-104">Los datos de entrada se pasan al códec DMOs con búferes de medios.</span><span class="sxs-lookup"><span data-stu-id="71c9c-104">Input data is passed to the codec DMOs using media buffers.</span></span> <span data-ttu-id="71c9c-105">Un búfer multimedia es un objeto que implementa la interfaz [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="71c9c-105">A media buffer is an object that implements the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface.</span></span> <span data-ttu-id="71c9c-106">Puede implementar una clase para este propósito o, si usa el SDK de Windows Media Format en la aplicación, puede usar los objetos de búfer definidos en ese SDK.</span><span class="sxs-lookup"><span data-stu-id="71c9c-106">You can implement a class for this purpose or, if you are using the Windows Media Format SDK in your application, you can use the buffer objects that are defined in that SDK.</span></span>

<span data-ttu-id="71c9c-107">Si implementa su propia clase de búfer, tenga cuidado sobre cómo se controla la memoria del búfer.</span><span class="sxs-lookup"><span data-stu-id="71c9c-107">If you implement your own buffer class, be careful about how the buffer memory is handled.</span></span> <span data-ttu-id="71c9c-108">Cuando se pasa una muestra de entrada, DMO mantiene una referencia al búfer hasta que termina con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="71c9c-108">When you pass an input sample, the DMO keeps a reference to the buffer until it is finished with the sample.</span></span> <span data-ttu-id="71c9c-109">Puede liberar inmediatamente la referencia a la interfaz [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) , pero no tiene ninguna manera de saber cuándo el códec ya no necesita su referencia.</span><span class="sxs-lookup"><span data-stu-id="71c9c-109">You can immediately release your reference to the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface, but you have no way of knowing when the codec no longer needs its reference.</span></span> <span data-ttu-id="71c9c-110">Para asegurarse de que la memoria se libera cuando el objeto se elimina, debe implementar la clase para que asigne y libere internamente la memoria para el búfer.</span><span class="sxs-lookup"><span data-stu-id="71c9c-110">To be certain that the memory is freed when the object deletes itself, you should implement your class so that it allocates and frees the memory for the buffer internally.</span></span>

<span data-ttu-id="71c9c-111">Dado que DMOs mantiene referencias a los búferes durante un período de tiempo desconocido, no es una cuestión trivial usar un grupo limitado de búferes.</span><span class="sxs-lookup"><span data-stu-id="71c9c-111">Because the DMOs keep references to buffers for an unknown period of time, it is not a trivial matter to use a limited pool of buffers.</span></span> <span data-ttu-id="71c9c-112">La solución más sencilla consiste en asignar un nuevo búfer para cada ejemplo, aunque esto es ineficaz.</span><span class="sxs-lookup"><span data-stu-id="71c9c-112">The simplest solution is to allocate a new buffer for each sample, although doing so is inefficient.</span></span>

<span data-ttu-id="71c9c-113">Una solución mejor consiste en implementar un objeto para administrar un grupo de búferes.</span><span class="sxs-lookup"><span data-stu-id="71c9c-113">A better solution is to implement an object to manage a pool of buffers.</span></span> <span data-ttu-id="71c9c-114">Para ello, escriba el código en el método de **versión** de la implementación de [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) que llama a un método del administrador de búfer (en lugar de eliminarlo) cuando el recuento de referencias desciende a cero.</span><span class="sxs-lookup"><span data-stu-id="71c9c-114">To do this, write code in the **Release** method of your [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) implementation that calls a method of your buffer manager (instead of deleting itself) when the reference count drops to zero.</span></span> <span data-ttu-id="71c9c-115">Después, el administrador de búfer puede mantener una lista de punteros a los objetos de búfer asignados.</span><span class="sxs-lookup"><span data-stu-id="71c9c-115">The buffer manager can then maintain a list of pointers to allocated buffer objects.</span></span> <span data-ttu-id="71c9c-116">Cree un método en el administrador de búfer para comprobar la lista de búferes disponibles y devolver un puntero para que la aplicación pueda tener acceso a los búferes cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="71c9c-116">Create a method in your buffer manager to check the list of free buffers and return a pointer so that your application can access buffers when needed.</span></span> <span data-ttu-id="71c9c-117">Este método debe crear nuevos búferes según sea necesario y agregarlos a la lista.</span><span class="sxs-lookup"><span data-stu-id="71c9c-117">This method should create new buffers as needed and add them to the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71c9c-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71c9c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71c9c-119">Trabajar con códec DMOs</span><span class="sxs-lookup"><span data-stu-id="71c9c-119">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
