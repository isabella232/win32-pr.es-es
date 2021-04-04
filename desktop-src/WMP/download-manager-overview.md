---
title: Información general del administrador de descargas
description: Información general del administrador de descargas
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player tiendas en línea, descarga en tiempo real
- tiendas en línea, descarga en tiempo real
- tipo 2 tiendas en línea, descarga en tiempo real
- Windows Media Player tiendas en línea, descarga en segundo plano
- tiendas en línea, descarga en segundo plano
- tipo 2 tiendas en línea, descarga en segundo plano
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
- descarga en tiempo real
- descarga en segundo plano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076267"
---
# <a name="download-manager-overview"></a><span data-ttu-id="a220a-117">Información general del administrador de descargas</span><span class="sxs-lookup"><span data-stu-id="a220a-117">Download Manager Overview</span></span>

<span data-ttu-id="a220a-118">Microsoft Windows Media Player proporciona paneles de tareas de la tienda en línea que contienen una ventana de explorador hospedada.</span><span class="sxs-lookup"><span data-stu-id="a220a-118">Microsoft Windows Media Player provides online store task panes that contain a hosted browser window.</span></span> <span data-ttu-id="a220a-119">A través de las tiendas en línea, los usuarios pueden interactuar con las páginas web de la tienda en línea a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="a220a-119">Through the online stores, users can interact with online store webpages across the Internet.</span></span>

<span data-ttu-id="a220a-120">El administrador de descargas de Windows Media Player proporciona un modelo de objetos que puede usar para controlar las tareas asociadas a la descarga de contenido en el equipo del usuario desde Microsoft Internet Information Services (IIS) mediante el protocolo de transferencia de hipertexto (HTTP).</span><span class="sxs-lookup"><span data-stu-id="a220a-120">The Windows Media Player Download Manager provides an object model that you can use to handle the tasks associated with downloading content to the user's computer from Microsoft Internet Information Services (IIS) using Hypertext Transfer Protocol (HTTP).</span></span> <span data-ttu-id="a220a-121">Con Download Manager, puede:</span><span class="sxs-lookup"><span data-stu-id="a220a-121">With the Download Manager, you can:</span></span>

-   <span data-ttu-id="a220a-122">Administrar varias descargas simultáneamente como una colección.</span><span class="sxs-lookup"><span data-stu-id="a220a-122">Manage multiple downloads simultaneously as a collection.</span></span>
-   <span data-ttu-id="a220a-123">Especifique una dirección URL para un archivo e inicie su descarga mediante HTTP.</span><span class="sxs-lookup"><span data-stu-id="a220a-123">Specify a URL for a file and start it downloading using HTTP.</span></span>
-   <span data-ttu-id="a220a-124">Consulte el estado y el progreso de la descarga.</span><span class="sxs-lookup"><span data-stu-id="a220a-124">Query for the download state and progress.</span></span>
-   <span data-ttu-id="a220a-125">Pausar, reanudar o cancelar una descarga.</span><span class="sxs-lookup"><span data-stu-id="a220a-125">Pause, resume, or cancel a download.</span></span>
-   <span data-ttu-id="a220a-126">Especifique si se produce una descarga en segundo plano o en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="a220a-126">Specify whether a download occurs in the background or in real time.</span></span> <span data-ttu-id="a220a-127">(La descarga en segundo plano solo está disponible en el sistema operativo Microsoft Windows XP). Vea [acerca de la descarga en segundo plano y en tiempo real](#about-background-and-real-time-downloading).</span><span class="sxs-lookup"><span data-stu-id="a220a-127">(Background downloading is only available on the Microsoft Windows XP operating system.) See [About Background and Real-time Downloading](#about-background-and-real-time-downloading).</span></span>
-   <span data-ttu-id="a220a-128">Especifique cómo se muestra el contenido en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a220a-128">Specify how content is displayed in the library.</span></span> <span data-ttu-id="a220a-129">Vea [acerca de la integración de bibliotecas](#about-library-integration).</span><span class="sxs-lookup"><span data-stu-id="a220a-129">See [About Library Integration](#about-library-integration).</span></span>

<span data-ttu-id="a220a-130">Download Manager es la solución para descargar contenido del código de script en páginas web hospedadas.</span><span class="sxs-lookup"><span data-stu-id="a220a-130">The Download Manager is the solution for downloading content from script code in hosted webpages.</span></span> <span data-ttu-id="a220a-131">Para descargar contenido con código de C++, use el Servicio de transferencia inteligente en segundo plano de Windows XP (BITS).</span><span class="sxs-lookup"><span data-stu-id="a220a-131">To download content using C++ code, use the Windows XP Background Intelligent Transfer Service (BITS).</span></span> <span data-ttu-id="a220a-132">Para obtener más información, vea [bits](bits.md).</span><span class="sxs-lookup"><span data-stu-id="a220a-132">For more information, see [BITS](bits.md).</span></span>

## <a name="about-background-and-real-time-downloading"></a><span data-ttu-id="a220a-133">Acerca de la descarga en segundo plano y en tiempo real</span><span class="sxs-lookup"><span data-stu-id="a220a-133">About Background and Real-time Downloading</span></span>

<span data-ttu-id="a220a-134">Download Manager ofrece dos tipos de descarga: en segundo plano y en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="a220a-134">The Download Manager offers two types of downloading: background and real-time.</span></span> <span data-ttu-id="a220a-135">El tipo que use depende de usted, y es posible permitir que el usuario seleccione también el tipo de descarga.</span><span class="sxs-lookup"><span data-stu-id="a220a-135">Which type you use is up to you, and it is possible to allow the user to select the download type as well.</span></span> <span data-ttu-id="a220a-136">Si decide permitir al usuario seleccionar el tipo de descarga, asegúrese de explicar las diferencias entre los dos tipos disponibles.</span><span class="sxs-lookup"><span data-stu-id="a220a-136">If you choose to allow the user to select the download type, be sure to explain the differences between the two available types.</span></span>

<span data-ttu-id="a220a-137">La descarga en tiempo real se produce a la vez.</span><span class="sxs-lookup"><span data-stu-id="a220a-137">Real-time downloading occurs all at once.</span></span> <span data-ttu-id="a220a-138">Cuando el usuario inicia una descarga de archivos, todo el archivo se transfiere al equipo del usuario en un flujo único y continuo.</span><span class="sxs-lookup"><span data-stu-id="a220a-138">When the user starts a file download, the entire file is transferred to the user's computer in a single, continuous stream.</span></span> <span data-ttu-id="a220a-139">El usuario no puede pausar ni interrumpir la descarga.</span><span class="sxs-lookup"><span data-stu-id="a220a-139">The user cannot pause or otherwise interrupt the download.</span></span> <span data-ttu-id="a220a-140">Si el usuario elige cerrar Windows Media Player antes de que finalice la descarga, pierde todos los archivos incompletos y debe descargarlos desde el principio para adquirir el contenido.</span><span class="sxs-lookup"><span data-stu-id="a220a-140">If the user chooses to close Windows Media Player before the download is finished, he or she loses any incomplete files and must download them from the beginning to acquire the content.</span></span>

<span data-ttu-id="a220a-141">La principal ventaja de la descarga en tiempo real es que permite al usuario adquirir el contenido más rápido que la descarga en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a220a-141">The main advantage of real-time downloading is that it allows the user to acquire the content faster than background downloading.</span></span> <span data-ttu-id="a220a-142">La descarga en tiempo real está disponible para los usuarios de Windows XP, pero es el único tipo de descarga disponible en las versiones del sistema operativo Windows anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a220a-142">Real-time downloading is available to users of Windows XP, but it is the only type of downloading available on versions of the Windows operating system prior to Windows XP.</span></span>

<span data-ttu-id="a220a-143">La descarga en segundo plano se produce de manera escalonada.</span><span class="sxs-lookup"><span data-stu-id="a220a-143">Background downloading happens in a piecemeal fashion.</span></span> <span data-ttu-id="a220a-144">Cuando el usuario inicia una descarga en segundo plano, las partes del archivo se transfieren al equipo del usuario cuando está disponible el tiempo de procesador.</span><span class="sxs-lookup"><span data-stu-id="a220a-144">When the user starts a background download, parts of the file are transferred to the user's computer when processor time is available.</span></span> <span data-ttu-id="a220a-145">Es posible pausar y reanudar una descarga en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a220a-145">It is possible to pause and resume a background download.</span></span> <span data-ttu-id="a220a-146">Si el usuario elige cerrar Windows Media Player antes de que finalice la descarga en segundo plano, se guarda la condición de los archivos incompletos y la descarga puede continuar en segundo plano, incluso después de reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="a220a-146">If the user chooses to close Windows Media Player before background downloading is finished, the condition of any incomplete files is saved and the downloading can continue in the background, even after restarting the computer.</span></span>

<span data-ttu-id="a220a-147">La descarga en segundo plano puede tardar más que la descarga en tiempo real, ya que el proceso de descarga solo se produce cuando el procesador no realiza otras tareas.</span><span class="sxs-lookup"><span data-stu-id="a220a-147">Background downloading can take longer than real-time downloading because the download process only happens when the processor is not performing other tasks.</span></span>

<span data-ttu-id="a220a-148">La descarga en segundo plano solo está disponible cuando se usa Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a220a-148">Background downloading is only available when using Windows XP.</span></span>

## <a name="about-library-integration"></a><span data-ttu-id="a220a-149">Acerca de la integración de bibliotecas</span><span class="sxs-lookup"><span data-stu-id="a220a-149">About Library Integration</span></span>

<span data-ttu-id="a220a-150">Windows Media Player puede organizar automáticamente el contenido de la tienda en línea en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a220a-150">Windows Media Player can automatically organize online store content in the library.</span></span> <span data-ttu-id="a220a-151">Para ello, debe especificar un valor para el atributo **WM/ContentDistributor** para cada archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="a220a-151">To enable this, you must specify a value for the **WM/ContentDistributor** attribute for each digital media file.</span></span> <span data-ttu-id="a220a-152">Cuando se agrega un archivo multimedia digital a la biblioteca, que se produce automáticamente al usar el administrador de descargas, el archivo aparece automáticamente en el nodo **música comprada** o **vídeos comprados** .</span><span class="sxs-lookup"><span data-stu-id="a220a-152">When a digital media file is added to the library, which happens automatically when using the Download Manager, the file is listed in the **Purchased Music** or **Purchased Videos** node automatically.</span></span> <span data-ttu-id="a220a-153">Por ejemplo, si el valor de **WM/ContentDistributor** es "Proseware" y el archivo multimedia digital contiene música, el contenido aparecerá en la biblioteca en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="a220a-153">For example, if the value for **WM/ContentDistributor** is "Proseware" and the digital media file contains music, the content would appear in the library in the following location:</span></span>

<span data-ttu-id="a220a-154">Toda la música/música comprada/Proseware</span><span class="sxs-lookup"><span data-stu-id="a220a-154">All Music/Purchased Music/Proseware</span></span>

## <a name="related-topics"></a><span data-ttu-id="a220a-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a220a-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a220a-156">**Administrador de descargas**</span><span class="sxs-lookup"><span data-stu-id="a220a-156">**Download Manager**</span></span>](download-manager.md)
</dt> <dt>

[<span data-ttu-id="a220a-157">**DownloadCollection.startDownload**</span><span class="sxs-lookup"><span data-stu-id="a220a-157">**DownloadCollection.startDownload**</span></span>](downloadcollection-startdownload.md)
</dt> </dl>

 

 




