---
title: Para agregar datos de script al encabezado
description: Para agregar datos de script al encabezado
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- SDK de Windows Media Format, agregar datos de script a encabezados
- Advanced Systems Format (ASF), agregar datos de script a encabezados
- ASF (formato de sistemas avanzados), agregar datos de script a encabezados
- scripts, agregar datos a encabezados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105704921"
---
# <a name="to-add-script-data-to-the-header"></a><span data-ttu-id="3a399-107">Para agregar datos de script al encabezado</span><span class="sxs-lookup"><span data-stu-id="3a399-107">To Add Script Data to the Header</span></span>

<span data-ttu-id="3a399-108">Puede incluir comandos de script en el encabezado de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="3a399-108">You can include script commands in the header of an ASF file.</span></span> <span data-ttu-id="3a399-109">Para escribir comandos de script en el encabezado en el momento de la codificación, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="3a399-109">To write script commands to the header at the time of encoding, perform the following steps.</span></span> <span data-ttu-id="3a399-110">Siga estos pasos antes de llamar a [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="3a399-110">Perform these steps prior to calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

1.  <span data-ttu-id="3a399-111">Obtenga un puntero a la interfaz **IWMHeaderInfo** llamando a **IWMWriter:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="3a399-111">Obtain a pointer to the **IWMHeaderInfo** interface by calling **IWMWriter::QueryInterface**.</span></span>
2.  <span data-ttu-id="3a399-112">Agregue cada comando de script deseado llamando a [**IWMHeaderInfo:: AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span><span class="sxs-lookup"><span data-stu-id="3a399-112">Add each desired script command by calling [**IWMHeaderInfo::AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span></span> <span data-ttu-id="3a399-113">Cada llamada toma las dos cadenas por separado y el tiempo de presentación que se va a usar para el comando como parámetros.</span><span class="sxs-lookup"><span data-stu-id="3a399-113">Each call takes the two strings separately and the presentation time to be used for the command as parameters.</span></span>

<span data-ttu-id="3a399-114">Cuando una aplicación Lea el archivo, tendrá que recuperar todos los comandos de script.</span><span class="sxs-lookup"><span data-stu-id="3a399-114">When an application reads the file, it will need to retrieve all of the script commands.</span></span> <span data-ttu-id="3a399-115">Para buscar todos los comandos de script en el encabezado de un archivo, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="3a399-115">To find all script commands in the header of a file, perform the following steps.</span></span> <span data-ttu-id="3a399-116">Esto debe realizarse antes de iniciar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="3a399-116">This should be done before starting playback.</span></span>

1.  <span data-ttu-id="3a399-117">Obtenga un puntero a la interfaz **IWMHeaderInfo** del objeto lector (o del objeto lector sincrónico) mediante una llamada al método **QueryInterface** de otra interfaz en el objeto.</span><span class="sxs-lookup"><span data-stu-id="3a399-117">Obtain a pointer to the **IWMHeaderInfo** interface of the reader object (or synchronous reader object) by calling the **QueryInterface** method of another interface in the object.</span></span>
2.  <span data-ttu-id="3a399-118">Obtenga el número total de scripts en el encabezado mediante una llamada a [**IWMHeaderInfo:: GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span><span class="sxs-lookup"><span data-stu-id="3a399-118">Get the total number of scripts in the header by calling [**IWMHeaderInfo::GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span></span>
3.  <span data-ttu-id="3a399-119">Recorra en bucle todos los scripts del encabezado de uno en uno mediante llamadas a [**IWMHeaderInfo:: GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span><span class="sxs-lookup"><span data-stu-id="3a399-119">Loop through all of the scripts in the header one at a time using calls to [**IWMHeaderInfo::GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span></span>
4.  <span data-ttu-id="3a399-120">Cree una lista de los tiempos de presentación para que la aplicación pueda reaccionar a los comandos en el momento adecuado.</span><span class="sxs-lookup"><span data-stu-id="3a399-120">Create a list of the presentation times so that your application can react to the commands at the appropriate time.</span></span>

> [!Note]  
> <span data-ttu-id="3a399-121">Al usar DRM para cifrar un archivo, ningún comando de script puede tener un tiempo de presentación de 0.</span><span class="sxs-lookup"><span data-stu-id="3a399-121">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3a399-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a399-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a399-123">**Interfaz IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="3a399-123">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="3a399-124">**Interfaz IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="3a399-124">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="3a399-125">**Usar comandos de script**</span><span class="sxs-lookup"><span data-stu-id="3a399-125">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




