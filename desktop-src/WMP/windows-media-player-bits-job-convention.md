---
title: Convención de trabajo de Windows Media Player BITS
description: Windows Media Player puede descargar y agregar elementos multimedia digitales a la biblioteca automáticamente si utiliza Servicio de transferencia inteligente en segundo plano (BITS).
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Windows Media Player tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tipo 2 tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- Servicio de transferencia inteligente en segundo plano (BITS)
- BITS (Servicio de transferencia inteligente en segundo plano)
- Windows Media Player tiendas en línea, Convención de trabajo de BITS
- tiendas en línea, Convención de trabajos de BITS
- tipo 2 tiendas en línea, Convención de trabajos de BITS
- Convención de trabajos de BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271337"
---
# <a name="windows-media-player-bits-job-convention"></a><span data-ttu-id="1d83f-112">Convención de trabajo de Windows Media Player BITS</span><span class="sxs-lookup"><span data-stu-id="1d83f-112">Windows Media Player BITS Job Convention</span></span>

<span data-ttu-id="1d83f-113">Windows Media Player puede descargar y agregar elementos multimedia digitales a la biblioteca automáticamente si utiliza [servicio de transferencia inteligente en segundo plano (bits)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span><span class="sxs-lookup"><span data-stu-id="1d83f-113">Windows Media Player can automatically download and add digital media items to the library if you use [Background Intelligent Transfer Service (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span></span> <span data-ttu-id="1d83f-114">Para aprovechar esta característica, debe agregar el trabajo a la cola de transferencia de BITS y llamar a **IBackgroundCopyJob:: SetDescription**, proporcionando una cadena de descripción que use el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="1d83f-114">To take advantage of this feature, you must add your job to the BITS transfer queue and call **IBackgroundCopyJob::SetDescription**, providing a description string that uses the correct format.</span></span>

> [!Note]  
> <span data-ttu-id="1d83f-115">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="1d83f-115">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1d83f-116">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="1d83f-116">Use of this functionality outside the context of an online store is not supported.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1d83f-117">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d83f-117">Syntax</span></span>

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a><span data-ttu-id="1d83f-118">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d83f-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d83f-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span><span class="sxs-lookup"><span data-stu-id="1d83f-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span></span>
</dt> <dd>

<span data-ttu-id="1d83f-120">Valor de bit 32 generado aleatoriamente que Windows Media Player usa para identificar el servicio.</span><span class="sxs-lookup"><span data-stu-id="1d83f-120">A randomly generated 32-bit value that Windows Media Player uses to identify the service.</span></span>

</dd> <dt>

<span data-ttu-id="1d83f-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Presta*</span><span class="sxs-lookup"><span data-stu-id="1d83f-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Provider*</span></span>
</dt> <dd>

<span data-ttu-id="1d83f-122">Nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="1d83f-122">The provider name.</span></span> <span data-ttu-id="1d83f-123">Este valor debe coincidir con un nombre de clave de almacén en línea válido.</span><span class="sxs-lookup"><span data-stu-id="1d83f-123">This value must match a valid online store key name.</span></span>

</dd> <dt>

<span data-ttu-id="1d83f-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span><span class="sxs-lookup"><span data-stu-id="1d83f-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span></span>
</dt> <dd>

<span data-ttu-id="1d83f-125">Nombre del intérprete principal del álbum.</span><span class="sxs-lookup"><span data-stu-id="1d83f-125">The name of the primary artist for the album.</span></span>

</dd> <dt>

<span data-ttu-id="1d83f-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*Álbum*</span><span class="sxs-lookup"><span data-stu-id="1d83f-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*</span></span>
</dt> <dd>

<span data-ttu-id="1d83f-127">Título del álbum.</span><span class="sxs-lookup"><span data-stu-id="1d83f-127">The title of the album.</span></span>

</dd> <dt>

<span data-ttu-id="1d83f-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*</span><span class="sxs-lookup"><span data-stu-id="1d83f-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*</span></span>
</dt> <dd>

<span data-ttu-id="1d83f-129">Número de pista del CD.</span><span class="sxs-lookup"><span data-stu-id="1d83f-129">The CD track number.</span></span>

</dd> <dt>

<span data-ttu-id="1d83f-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Titulo*</span><span class="sxs-lookup"><span data-stu-id="1d83f-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Title*</span></span>
</dt> <dd>

<span data-ttu-id="1d83f-131">Título del contenido.</span><span class="sxs-lookup"><span data-stu-id="1d83f-131">The title of the content.</span></span>

</dd> <dt>

<span data-ttu-id="1d83f-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Duration*</span><span class="sxs-lookup"><span data-stu-id="1d83f-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Duration*</span></span>
</dt> <dd>

<span data-ttu-id="1d83f-133">La duración del contenido.</span><span class="sxs-lookup"><span data-stu-id="1d83f-133">The duration of the content.</span></span>

</dd> <dt>

<span data-ttu-id="1d83f-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Clasific*</span><span class="sxs-lookup"><span data-stu-id="1d83f-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Rating*</span></span>
</dt> <dd>

<span data-ttu-id="1d83f-135">Clasificación del contenido.</span><span class="sxs-lookup"><span data-stu-id="1d83f-135">The rating for the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d83f-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d83f-136">Remarks</span></span>

<span data-ttu-id="1d83f-137">Cuando Windows Media Player 10 o una versión posterior usa BITS para descargar contenido, enumera los trabajos de la cola de transferencia e inspecciona la cadena de descripción de cada trabajo.</span><span class="sxs-lookup"><span data-stu-id="1d83f-137">When Windows Media Player 10 or later uses BITS to download content, it enumerates the jobs in the transfer queue and inspects the description string for each job.</span></span> <span data-ttu-id="1d83f-138">Si la cadena de Descripción coincide con la Convención esperada, Windows Media Player descarga el contenido.</span><span class="sxs-lookup"><span data-stu-id="1d83f-138">If the description string matches the expected convention, Windows Media Player downloads the content.</span></span>

<span data-ttu-id="1d83f-139">Solo debe agregar un archivo multimedia digital para su descarga en cada trabajo de BITS.</span><span class="sxs-lookup"><span data-stu-id="1d83f-139">You must add only one digital media file for download to each BITS job.</span></span>

<span data-ttu-id="1d83f-140">Después de iniciar un trabajo de BITS con esta Convención, debe permitir que Windows Media Player complete el trabajo.</span><span class="sxs-lookup"><span data-stu-id="1d83f-140">After you start a BITS job using this convention, you must let Windows Media Player complete the job.</span></span> <span data-ttu-id="1d83f-141">Windows Media Player también quitará el trabajo de la cola de BITS, moverá el archivo descargado a la ubicación donde se guarda la música copiada y agregará el archivo descargado a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="1d83f-141">Windows Media Player will also remove the job from the BITS queue, move the downloaded file to the location where ripped music is saved, and add the downloaded file to the library.</span></span>

<span data-ttu-id="1d83f-142">El parámetro *serviceId* debe contener un valor de bit 32 distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="1d83f-142">The *serviceId* parameter must contain a nonzero 32-bit value.</span></span> <span data-ttu-id="1d83f-143">Se recomienda usar la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para crear este valor.</span><span class="sxs-lookup"><span data-stu-id="1d83f-143">We recommend that you use the function [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) to create this value.</span></span>

<span data-ttu-id="1d83f-144">El nombre de archivo que especifique mediante el parámetro *localname* de **IBackgroundCopyJob:: AddFile** debe tener una extensión de nombre de archivo. WMA,. wmv,. mp3 o. ASF.</span><span class="sxs-lookup"><span data-stu-id="1d83f-144">The file name you specify using the *localName* parameter of **IBackgroundCopyJob::AddFile** must have a .wma, .wmv, .mp3, or .asf file name extension.</span></span>

<span data-ttu-id="1d83f-145">Los parámetros restantes están diseñados para contener valores de metadatos relacionados con el contenido.</span><span class="sxs-lookup"><span data-stu-id="1d83f-145">The remaining parameters are designed to contain metadata values related to the content.</span></span> <span data-ttu-id="1d83f-146">Puede recuperar estos valores de la Página Web de la tienda en línea mediante **DownloadItem. getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="1d83f-146">You can retrieve these values from your online store webpage by using **DownloadItem.getItemInfo**.</span></span> <span data-ttu-id="1d83f-147">Puede recuperar la colección de descargas correcta llamando a **Downloadmanager. getDownloadCollection** y proporcionando *ServiceId* como parámetro *collectionId* .</span><span class="sxs-lookup"><span data-stu-id="1d83f-147">You can retrieve the correct download collection by calling **DownloadManager.getDownloadCollection** and providing *serviceId* as the *collectionId* parameter.</span></span>

<span data-ttu-id="1d83f-148">Windows Media Player inspecciona la cola de BITS periódicamente mientras el reproductor se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="1d83f-148">Windows Media Player inspects the BITS queue periodically while the Player is running.</span></span> <span data-ttu-id="1d83f-149">Para asegurarse de que Windows Media Player comprueba la cola de BITS para los trabajos de descarga, debe crear un valor en la subclave del Registro siguiente:</span><span class="sxs-lookup"><span data-stu-id="1d83f-149">To ensure that Windows Media Player checks the BITS queue for download jobs, you should create a value in the following registry subkey:</span></span>

<span data-ttu-id="1d83f-150">**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Services**</span><span class="sxs-lookup"><span data-stu-id="1d83f-150">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Services**</span></span>

<span data-ttu-id="1d83f-151">El valor debe crearse como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="1d83f-151">The value should be created as follows.</span></span>



| <span data-ttu-id="1d83f-152">Nombre</span><span class="sxs-lookup"><span data-stu-id="1d83f-152">Name</span></span>                | <span data-ttu-id="1d83f-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d83f-153">Type</span></span>      | <span data-ttu-id="1d83f-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d83f-154">Description</span></span>                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d83f-155">**RefreshDownload**</span><span class="sxs-lookup"><span data-stu-id="1d83f-155">**RefreshDownload**</span></span> | <span data-ttu-id="1d83f-156">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="1d83f-156">**DWORD**</span></span> | <span data-ttu-id="1d83f-157">Especifica si Windows Media Player debe inspeccionar la cola de BITS para los trabajos de descarga.</span><span class="sxs-lookup"><span data-stu-id="1d83f-157">Specifies whether Windows Media Player should inspect the BITS queue for download jobs.</span></span> <span data-ttu-id="1d83f-158">Si el valor es cero, el reproductor no inspeccionará la cola de BITS.</span><span class="sxs-lookup"><span data-stu-id="1d83f-158">If the value is zero, the Player will not inspect the BITS queue.</span></span> <span data-ttu-id="1d83f-159">El reproductor debe inspeccionar la cola si el valor es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="1d83f-159">The Player must inspect the queue if the value is nonzero.</span></span> |



 

<span data-ttu-id="1d83f-160">Puede usar la siguiente sintaxis alternativa para agregar trabajos de BITS que Windows Media Player no complete, pero para los que simplemente muestra información de estado:</span><span class="sxs-lookup"><span data-stu-id="1d83f-160">You can use the following alternate syntax to add BITS jobs that Windows Media Player does not complete, but for which it simply shows status information:</span></span>

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

<span data-ttu-id="1d83f-161">Cuando use la sintaxis anterior, debe escribir código para completar la descarga de BITS, organizar el contenido en el equipo del usuario y agregar el contenido a la biblioteca, si lo desea.</span><span class="sxs-lookup"><span data-stu-id="1d83f-161">When you use the preceding syntax, you must write code to complete the BITS download, organize the content on the user's computer, and add the content to the library, if desired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d83f-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d83f-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d83f-163">CryptGenRandom</span><span class="sxs-lookup"><span data-stu-id="1d83f-163">CryptGenRandom</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[<span data-ttu-id="1d83f-164">**DownloadItem. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="1d83f-164">**DownloadItem.getItemInfo**</span></span>](downloaditem-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="1d83f-165">**DownloadManager.getDownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="1d83f-165">**DownloadManager.getDownloadCollection**</span></span>](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="1d83f-166">**Referencia de las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="1d83f-166">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 