---
title: Para crear un lector y abrir un archivo
description: Para crear un lector y abrir un archivo
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- Advanced Systems Format (ASF), crear lectores
- ASF (formato de sistemas avanzados), creación de lectores
- Advanced Systems Format (ASF), abrir archivos
- ASF (formato de sistemas avanzados), abrir archivos
- lectores asincrónicos, crear
- lectores asincrónicos, abrir archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789214"
---
# <a name="to-create-a-reader-and-open-a-file"></a><span data-ttu-id="08e36-109">Para crear un lector y abrir un archivo</span><span class="sxs-lookup"><span data-stu-id="08e36-109">To Create a Reader and Open a File</span></span>

<span data-ttu-id="08e36-110">Para poder trabajar con el lector, debe crear un objeto de lector y cargar un archivo para leerlo.</span><span class="sxs-lookup"><span data-stu-id="08e36-110">Before you can do any work with the reader, you will need to create a reader object and load a file for reading.</span></span> <span data-ttu-id="08e36-111">Para inicializar el lector y abrir un archivo, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="08e36-111">To initialize the reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="08e36-112">Cree un objeto lector mediante una llamada a la función [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) .</span><span class="sxs-lookup"><span data-stu-id="08e36-112">Create a reader object by calling the [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) function.</span></span> <span data-ttu-id="08e36-113">Debe especificar el nivel deseado de Rights Management para el nuevo objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="08e36-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="08e36-114">Los modos disponibles se enumeran en el tipo de enumeración de [**\_ derechos WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .</span><span class="sxs-lookup"><span data-stu-id="08e36-114">The available modes are listed in the [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) enumeration type.</span></span>
2.  <span data-ttu-id="08e36-115">Especifique el archivo que se va a leer llamando a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span><span class="sxs-lookup"><span data-stu-id="08e36-115">Specify a file to read by calling [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span></span> <span data-ttu-id="08e36-116">Debe especificar una interfaz de devolución de llamada de lector para que la use el lector.</span><span class="sxs-lookup"><span data-stu-id="08e36-116">You must specify a reader callback interface for the reader to use.</span></span> <span data-ttu-id="08e36-117">Para obtener más información sobre la devolución de llamada del lector, vea [para implementar mensajes de lector en la devolución de llamada de estado](to-implement-reader-messages-in-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="08e36-117">For more information about the reader callback, see [To Implement Reader Messages in the OnStatus Callback](to-implement-reader-messages-in-the-onstatus-callback.md).</span></span>
3.  <span data-ttu-id="08e36-118">Espere a que el lector Abra el archivo.</span><span class="sxs-lookup"><span data-stu-id="08e36-118">Wait for the reader to open the file.</span></span> <span data-ttu-id="08e36-119">Cuando se llama a **Open** para cargar un archivo, devuelve casi inmediatamente y continúa el procesamiento en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="08e36-119">When you call **Open** to load a file, it returns almost immediately and continues processing on another thread.</span></span> <span data-ttu-id="08e36-120">Debe esperar a que se completen las operaciones, mediante la señalización de un evento cuando la devolución de llamada de **Estado** reciba el \_ mensaje de estado abierto de WMT.</span><span class="sxs-lookup"><span data-stu-id="08e36-120">You should wait for operations to complete, by signaling an event when the **OnStatus** callback receives the WMT\_OPENED status message.</span></span>

<span data-ttu-id="08e36-121">El lector también admite el uso de la interfaz com **IStream** para abrir archivos.</span><span class="sxs-lookup"><span data-stu-id="08e36-121">The reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="08e36-122">Puede implementar la interfaz **IStream** de la forma que elija.</span><span class="sxs-lookup"><span data-stu-id="08e36-122">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="08e36-123">Después de abrir el archivo deseado en **IStream**, puede seguir los pasos indicados anteriormente, salvo que debe llamar a [**IWMReaderAdvanced2:: OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) en lugar de **IWMReader:: Open** en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="08e36-123">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMReaderAdvanced2::OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) instead of **IWMReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08e36-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08e36-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e36-125">**Interfaz IWMReader**</span><span class="sxs-lookup"><span data-stu-id="08e36-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="08e36-126">**Interfaz IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="08e36-126">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="08e36-127">**Interfaz IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="08e36-127">**IWMStatusCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[<span data-ttu-id="08e36-128">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="08e36-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="08e36-129">**Usar los métodos de devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="08e36-129">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




