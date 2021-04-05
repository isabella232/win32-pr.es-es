---
title: Para editar los metadatos con el escritor
description: Para editar los metadatos con el escritor
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- SDK de Windows Media Format, edición de metadatos con el escritor
- SDK de Windows Media Format, edición de metadatos
- Advanced Systems Format (ASF), edición de metadatos con el sistema de escritura
- ASF (formato de sistemas avanzados), edición de metadatos con el sistema de escritura
- Advanced Systems Format (ASF), edición de metadatos
- ASF (formato de sistemas avanzados), edición de metadatos
- metadatos, editar con el escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420455"
---
# <a name="to-edit-metadata-with-the-writer"></a><span data-ttu-id="e5860-110">Para editar los metadatos con el escritor</span><span class="sxs-lookup"><span data-stu-id="e5860-110">To Edit Metadata with the Writer</span></span>

<span data-ttu-id="e5860-111">Puede tener acceso a, directamente desde el escritor, los metadatos que entrarán en el encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="e5860-111">You can access, directly from the writer, the metadata that will go into the header of the file.</span></span> <span data-ttu-id="e5860-112">Llame al método **QueryInterface** de cualquier interfaz del objeto Writer para obtener un puntero a la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) .</span><span class="sxs-lookup"><span data-stu-id="e5860-112">Call the **QueryInterface** method of any interface in the writer object to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interface.</span></span> <span data-ttu-id="e5860-113">Después de tener un puntero a la interfaz adecuada, puede manipular los metadatos tal como lo haría si hubiera cargado el archivo en el objeto del editor de metadatos.</span><span class="sxs-lookup"><span data-stu-id="e5860-113">After you have a pointer to the appropriate interface, you can manipulate the metadata just as you would if you had loaded the file in the metadata editor object.</span></span> <span data-ttu-id="e5860-114">Para obtener más información sobre la edición de metadatos, vea [trabajar con metadatos](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="e5860-114">For more information about editing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

<span data-ttu-id="e5860-115">Debe realizar todos los cambios en los metadatos antes de llamar a [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="e5860-115">You must make all changes to the metadata before calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

> [!Note]  
> <span data-ttu-id="e5860-116">Si establece los metadatos de un archivo, escribe el archivo y, a continuación, prepara para escribir un archivo nuevo sin liberar el escritor, algunos metadatos que se establecieron para el primer archivo permanecerán establecidos y se incluirán con los archivos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e5860-116">If you set metadata for a file, write the file, and then prepare to write a new file without releasing the writer, some metadata that was set for the first file will remain set and will be included with subsequent files.</span></span> <span data-ttu-id="e5860-117">Al escribir varios archivos con la misma instancia del objeto escritor, tiene dos opciones: comprobar todos los metadatos antes de escribir cada archivo o solo escribir en los metadatos del escritor que se aplican a todos los archivos que está escribiendo.</span><span class="sxs-lookup"><span data-stu-id="e5860-117">When writing several files with the same instance of the writer object, you have two options: check all the metadata before writing each file, or only write in the writer metadata that applies to all of the files you are writing.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e5860-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5860-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5860-119">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="e5860-119">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




