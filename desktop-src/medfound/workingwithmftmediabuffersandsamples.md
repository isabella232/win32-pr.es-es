---
description: Trabajar con ejemplos y búferes de medios de MFT
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Trabajar con ejemplos y búferes de medios de MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6373f6d75b4122409b54649eed6f90e95c2f50c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361866"
---
# <a name="working-with-mft-media-buffers-and-samples"></a><span data-ttu-id="3b07d-103">Trabajar con ejemplos y búferes de medios de MFT</span><span class="sxs-lookup"><span data-stu-id="3b07d-103">Working with MFT Media Buffers and Samples</span></span>

<span data-ttu-id="3b07d-104">Los MFTs de códec pasan datos multimedia hacia atrás y hacia delante mediante los búferes multimedia y ejemplos.</span><span class="sxs-lookup"><span data-stu-id="3b07d-104">Codec MFTs pass media data back and forth by using media buffers and samples.</span></span>

<span data-ttu-id="3b07d-105">Un búfer multimedia es un objeto COM que administra un bloque de memoria, normalmente para contener datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="3b07d-105">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="3b07d-106">Cuando los datos se pasan a o desde una MFT, siempre se pasan en forma de un búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="3b07d-106">When data is passed to or from an MFT, it is always passed in the form of a media buffer.</span></span>

<span data-ttu-id="3b07d-107">Todos los búferes multimedia exponen la interfaz **IMFMediaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="3b07d-107">All media buffers expose the **IMFMediaBuffer** interface.</span></span> <span data-ttu-id="3b07d-108">Esta interfaz está diseñada para cualquier tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3b07d-108">This interface is designed for any type of data.</span></span> <span data-ttu-id="3b07d-109">Los búferes que contienen datos de vídeo a menudo también exponen **IMF2DBuffer**.</span><span class="sxs-lookup"><span data-stu-id="3b07d-109">Buffers containing video data often also expose **IMF2DBuffer**.</span></span>

<span data-ttu-id="3b07d-110">Un búfer multimedia tiene un tamaño máximo, que es la cantidad de memoria asignada para el búfer.</span><span class="sxs-lookup"><span data-stu-id="3b07d-110">A media buffer has a maximum size, which is the amount of memory allocated for the buffer.</span></span> <span data-ttu-id="3b07d-111">Para encontrar el tamaño máximo, llame a **IMFMediaBuffer:: GetMaxLength**.</span><span class="sxs-lookup"><span data-stu-id="3b07d-111">To find the maximum size, call **IMFMediaBuffer::GetMaxLength**.</span></span> <span data-ttu-id="3b07d-112">En cualquier momento, un búfer multimedia también tiene una longitud actual, que es la cantidad de datos válidos en el búfer, que van desde cero bytes hasta el tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="3b07d-112">At any point in time, a media buffer also has a current length, which is the amount of valid data in the buffer, ranging from zero bytes up to the maximum size.</span></span> <span data-ttu-id="3b07d-113">Para obtener la longitud actual, llame a **IMFMediaBuffer:: GetCurrentLength**.</span><span class="sxs-lookup"><span data-stu-id="3b07d-113">To get the current length, call **IMFMediaBuffer::GetCurrentLength**.</span></span> <span data-ttu-id="3b07d-114">Cuando se crea el búfer, la longitud actual es cero.</span><span class="sxs-lookup"><span data-stu-id="3b07d-114">When the buffer is created, the current length is zero.</span></span> <span data-ttu-id="3b07d-115">Si escribe datos en el búfer, llame a **IMFMediaBuffer:: SetCurrentLength** para actualizar la longitud actual.</span><span class="sxs-lookup"><span data-stu-id="3b07d-115">If you write data to the buffer, call **IMFMediaBuffer::SetCurrentLength** to update the current length.</span></span>

<span data-ttu-id="3b07d-116">Para tener acceso a la memoria del búfer, llame a **IMFMediaBuffer:: Lock**.</span><span class="sxs-lookup"><span data-stu-id="3b07d-116">To access the memory in the buffer, call **IMFMediaBuffer::Lock**.</span></span> <span data-ttu-id="3b07d-117">Este método devuelve un puntero al principio del bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="3b07d-117">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="3b07d-118">Cuando haya terminado de usar el puntero, llame a **IMFMediaBuffer:: Unlock**.</span><span class="sxs-lookup"><span data-stu-id="3b07d-118">When you are done using the pointer, call **IMFMediaBuffer::Unlock**.</span></span> <span data-ttu-id="3b07d-119">El método **Lock** no es un mecanismo de sincronización de subprocesos; no garantiza que otros subprocesos no puedan tener acceso al búfer.</span><span class="sxs-lookup"><span data-stu-id="3b07d-119">The **Lock** method is not a thread synchronization mechanism; it does not guarantee that other threads cannot access the buffer.</span></span> <span data-ttu-id="3b07d-120">El método **Lock** se usa para garantizar que la memoria a la que se obtiene acceso permanecerá válida hasta que se llame al método **Unlock** .</span><span class="sxs-lookup"><span data-stu-id="3b07d-120">The **Lock** method is used to assure that the memory accessed will remain valid until you call the **Unlock** method.</span></span>

<span data-ttu-id="3b07d-121">Un objeto de ejemplo multimedia (en el contexto del SDK de Media Foundation) es un objeto que contiene una lista ordenada de cero o más búferes.</span><span class="sxs-lookup"><span data-stu-id="3b07d-121">A media sample object (in the context of the Media Foundation SDK) is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="3b07d-122">Los ejemplos de medios exponen la interfaz **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="3b07d-122">Media samples expose the **IMFSample** interface.</span></span>

<span data-ttu-id="3b07d-123">Para crear un nuevo ejemplo, llame a la función **MFCreateSample** .</span><span class="sxs-lookup"><span data-stu-id="3b07d-123">To create a new sample, call the **MFCreateSample** function.</span></span> <span data-ttu-id="3b07d-124">Inicialmente, la lista de búferes del ejemplo está vacía.</span><span class="sxs-lookup"><span data-stu-id="3b07d-124">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="3b07d-125">Para agregar un búfer al final de la lista, llame a **IMFSample:: AddBuffer**.</span><span class="sxs-lookup"><span data-stu-id="3b07d-125">To add a buffer to the end of the list, call **IMFSample::AddBuffer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b07d-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b07d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b07d-127">Trabajar con códec DMOs</span><span class="sxs-lookup"><span data-stu-id="3b07d-127">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> <dt>

[<span data-ttu-id="3b07d-128">Trabajar con códec MFTs</span><span class="sxs-lookup"><span data-stu-id="3b07d-128">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



