---
title: Para crear un lector sincrónico y abrir un archivo
description: Para crear un lector sincrónico y abrir un archivo
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- Advanced Systems Format (ASF), crear lectores
- ASF (formato de sistemas avanzados), creación de lectores
- Advanced Systems Format (ASF), abrir archivos
- ASF (formato de sistemas avanzados), abrir archivos
- lectores sincrónicos, crear
- lectores sincrónicos, abrir archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105704917"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a><span data-ttu-id="ac2ac-109">Para crear un lector sincrónico y abrir un archivo</span><span class="sxs-lookup"><span data-stu-id="ac2ac-109">To Create a Synchronous Reader and Open a File</span></span>

<span data-ttu-id="ac2ac-110">Antes de poder realizar cualquier trabajo con el lector sincrónico, debe crear un objeto de lector sincrónico y cargar un archivo para leerlo.</span><span class="sxs-lookup"><span data-stu-id="ac2ac-110">Before you can do any work with the synchronous reader, you will need to create a synchronous reader object and load a file for reading.</span></span> <span data-ttu-id="ac2ac-111">Para inicializar el lector sincrónico y abrir un archivo, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ac2ac-111">To initialize the synchronous reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="ac2ac-112">Cree un objeto de lector sincrónico llamando a la función [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) .</span><span class="sxs-lookup"><span data-stu-id="ac2ac-112">Create a synchronous reader object by calling the [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) function.</span></span> <span data-ttu-id="ac2ac-113">Debe especificar el nivel deseado de Rights Management para el nuevo objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="ac2ac-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="ac2ac-114">Los modos disponibles se enumeran en el tipo de enumeración de **\_ derechos WMT** .</span><span class="sxs-lookup"><span data-stu-id="ac2ac-114">The available modes are listed in the **WMT\_RIGHTS** enumeration type.</span></span>
2.  <span data-ttu-id="ac2ac-115">Especifique el archivo que se va a leer llamando a [**IWMSyncReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span><span class="sxs-lookup"><span data-stu-id="ac2ac-115">Specify a file to read by calling [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span></span>

<span data-ttu-id="ac2ac-116">El lector sincrónico también admite el uso de la interfaz com **IStream** para abrir archivos.</span><span class="sxs-lookup"><span data-stu-id="ac2ac-116">The synchronous reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="ac2ac-117">Puede implementar la interfaz **IStream** de la forma que elija.</span><span class="sxs-lookup"><span data-stu-id="ac2ac-117">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="ac2ac-118">Después de abrir el archivo deseado en **IStream**, puede seguir los pasos indicados anteriormente, salvo que debe llamar a [**IWMSyncReader:: OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) en lugar de **IWMSyncReader:: Open** en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="ac2ac-118">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMSyncReader::OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) instead of **IWMSyncReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac2ac-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac2ac-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac2ac-120">**Interfaz IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="ac2ac-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="ac2ac-121">**Leer archivos con el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="ac2ac-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




