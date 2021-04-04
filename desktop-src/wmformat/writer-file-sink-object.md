---
title: Objeto receptor de archivos de Writer
description: Objeto receptor de archivos de Writer
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- SDK de Windows Media Format, objetos de receptor de archivos de escritura
- Advanced Systems Format (ASF), objetos de receptor de archivos de escritor
- ASF (formato de sistemas avanzados), objetos de receptor de archivos de escritor
- objetos, objetos de receptor de archivos de escritor
- objetos de receptor de archivo de escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077450"
---
# <a name="writer-file-sink-object"></a><span data-ttu-id="37eae-108">Objeto receptor de archivos de Writer</span><span class="sxs-lookup"><span data-stu-id="37eae-108">Writer File Sink Object</span></span>

<span data-ttu-id="37eae-109">El objeto de receptor del archivo de escritura se utiliza al escribir la salida de Windows Media en un archivo.</span><span class="sxs-lookup"><span data-stu-id="37eae-109">The writer file sink object is used when writing Windows Media output to a file.</span></span>

<span data-ttu-id="37eae-110">La función [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)crea el objeto de receptor del archivo de escritura, que establece un puntero a una interfaz **IWMWriterFileSink** .</span><span class="sxs-lookup"><span data-stu-id="37eae-110">The writer file sink object is created by the function [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), which sets a pointer to an **IWMWriterFileSink** interface.</span></span> <span data-ttu-id="37eae-111">Las demás interfaces del objeto de receptor del archivo de escritor se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="37eae-111">The other interfaces of the writer file sink object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="37eae-112">El objeto de receptor del archivo de escritor admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="37eae-112">The following interfaces are supported by the writer file sink object.</span></span>



| <span data-ttu-id="37eae-113">Interfaz</span><span class="sxs-lookup"><span data-stu-id="37eae-113">Interface</span></span>                                          | <span data-ttu-id="37eae-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="37eae-114">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37eae-115">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="37eae-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="37eae-116">Permite que la aplicación obtenga mensajes de estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="37eae-116">Enables the application to get status messages from the object.</span></span>                                                                 |
| [<span data-ttu-id="37eae-117">**IWMWriterFileSink**</span><span class="sxs-lookup"><span data-stu-id="37eae-117">**IWMWriterFileSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | <span data-ttu-id="37eae-118">Abre un archivo en el que el objeto de escritura puede escribir datos.</span><span class="sxs-lookup"><span data-stu-id="37eae-118">Opens a file to which the writer object can write data.</span></span>                                                                         |
| [<span data-ttu-id="37eae-119">**IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="37eae-119">**IWMWriterFileSink2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | <span data-ttu-id="37eae-120">Proporciona administración extendida de un objeto de receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="37eae-120">Provides extended management of a file sink object.</span></span> <span data-ttu-id="37eae-121">Hereda todos los métodos de **IWMWriterFileSink**.</span><span class="sxs-lookup"><span data-stu-id="37eae-121">Inherits all of the methods of **IWMWriterFileSink**.</span></span>                       |
| [<span data-ttu-id="37eae-122">**IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="37eae-122">**IWMWriterFileSink3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | <span data-ttu-id="37eae-123">Proporciona opciones adicionales para escribir archivos.</span><span class="sxs-lookup"><span data-stu-id="37eae-123">Provides additional options for writing files.</span></span> <span data-ttu-id="37eae-124">Hereda todos los métodos de **IWMWriterFileSink** y **IWMWriterFileSink2**.</span><span class="sxs-lookup"><span data-stu-id="37eae-124">Inherits all of the methods of **IWMWriterFileSink** and **IWMWriterFileSink2**.</span></span> |
| [<span data-ttu-id="37eae-125">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="37eae-125">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="37eae-126">Asigna memoria, determina si el receptor está funcionando en tiempo real y controla varias funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="37eae-126">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                |



 

<span data-ttu-id="37eae-127">La aplicación debe implementar la siguiente interfaz de devolución de llamada para realizar el seguimiento del progreso de un objeto de receptor del archivo de escritura.</span><span class="sxs-lookup"><span data-stu-id="37eae-127">The following callback interface should be implemented by the application to track the progress of a writer file sink object.</span></span>



| <span data-ttu-id="37eae-128">Interfaz</span><span class="sxs-lookup"><span data-stu-id="37eae-128">Interface</span></span>                                      | <span data-ttu-id="37eae-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="37eae-129">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="37eae-130">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="37eae-130">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="37eae-131">Obligatorio cuando la información de estado se debe comunicar a la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="37eae-131">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="37eae-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37eae-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37eae-133">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="37eae-133">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="37eae-134">**Trabajar con receptores de escritor**</span><span class="sxs-lookup"><span data-stu-id="37eae-134">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




