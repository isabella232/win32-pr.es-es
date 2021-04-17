---
title: Buffer (objeto)
description: Buffer (objeto)
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- SDK de Windows Media Format, objetos de búfer
- Advanced Systems Format (ASF), objetos de búfer
- ASF (formato de sistemas avanzados), objetos de búfer
- objetos, objetos de búfer
- objetos de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "105704911"
---
# <a name="buffer-object"></a><span data-ttu-id="74664-108">Buffer (objeto)</span><span class="sxs-lookup"><span data-stu-id="74664-108">Buffer Object</span></span>

<span data-ttu-id="74664-109">Un objeto de búfer se usa para contener ejemplos y entregarlos entre los objetos del SDK de Windows Media Format y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74664-109">A buffer object is used to hold samples and deliver them between the objects of the Windows Media Format SDK and your application.</span></span> <span data-ttu-id="74664-110">Cuando se escribe un archivo, se pasan los ejemplos de entrada al escritor mediante objetos de búfer.</span><span class="sxs-lookup"><span data-stu-id="74664-110">When you write a file, you pass your input samples to the writer using buffer objects.</span></span> <span data-ttu-id="74664-111">Al leer un archivo, el objeto lector o el objeto lector sincrónico proporciona ejemplos a la aplicación en objetos de búfer.</span><span class="sxs-lookup"><span data-stu-id="74664-111">When you read a file, the reader object or synchronous reader object provides samples to your application in buffer objects.</span></span>

<span data-ttu-id="74664-112">Para escribir ejemplos en un archivo, puede crear un objeto de búfer mediante el método [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) .</span><span class="sxs-lookup"><span data-stu-id="74664-112">For writing samples to a file, you can create a buffer object using the [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) method.</span></span> <span data-ttu-id="74664-113">Para leer ejemplos, el objeto lector y el objeto lector sincrónico crean internamente los objetos de búfer.</span><span class="sxs-lookup"><span data-stu-id="74664-113">For reading samples, the reader object and synchronous reader object both create buffer objects internally.</span></span> <span data-ttu-id="74664-114">Si lo desea, puede asignar sus propios objetos de búfer para la lectura de archivos mediante [**IWMReaderAllocatorEx:: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) o [**IWMReaderAllocatorEx:: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span><span class="sxs-lookup"><span data-stu-id="74664-114">If you choose to, you can allocate your own buffer objects for file reading by using [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) or [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span>

<span data-ttu-id="74664-115">Cada objeto de búfer admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="74664-115">The following interfaces are supported by every buffer object.</span></span>



| <span data-ttu-id="74664-116">Interfaz</span><span class="sxs-lookup"><span data-stu-id="74664-116">Interface</span></span>                          | <span data-ttu-id="74664-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="74664-117">Description</span></span>                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="74664-118">**INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="74664-118">**INSSBuffer**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | <span data-ttu-id="74664-119">Controla y proporciona acceso al búfer.</span><span class="sxs-lookup"><span data-stu-id="74664-119">Controls and provides access to the buffer.</span></span>                          |
| [<span data-ttu-id="74664-120">**INSSBuffer2**</span><span class="sxs-lookup"><span data-stu-id="74664-120">**INSSBuffer2**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | <span data-ttu-id="74664-121">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="74664-121">Not implemented.</span></span>                                                     |
| [<span data-ttu-id="74664-122">**INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="74664-122">**INSSBuffer3**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | <span data-ttu-id="74664-123">Admite propiedades de búfer, que se usan para las extensiones de unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="74664-123">Supports buffer properties, which are used for data unit extensions.</span></span> |
| [<span data-ttu-id="74664-124">**INSSBuffer4**</span><span class="sxs-lookup"><span data-stu-id="74664-124">**INSSBuffer4**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | <span data-ttu-id="74664-125">Enumera las propiedades de búfer.</span><span class="sxs-lookup"><span data-stu-id="74664-125">Enumerates buffer properties.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="74664-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74664-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74664-127">**Objects**</span><span class="sxs-lookup"><span data-stu-id="74664-127">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




