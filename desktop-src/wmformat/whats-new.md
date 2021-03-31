---
title: Novedades (Windows Media Format 11 SDK)
description: What's New
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- SDK de Windows Media Format, novedades
- Windows Media Format SDK, características
- SDK de Windows Media Format, nuevas características
- SDK de Windows Media Format, API extendidas de cliente
- SDK de Windows Media Format, actualizaciones de DRM
- SDK de Windows Media Format, actualizaciones de códecs
- SDK de Windows Media Format, imágenes en miniatura
- Administración de derechos digitales (DRM), nuevas características
- DRM (administración de derechos digitales), nuevas características
- imágenes en miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800776"
---
# <a name="whats-new-windows-media-format-11-sdk"></a><span data-ttu-id="55ba3-113">Novedades (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="55ba3-113">What's New (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="55ba3-114">El SDK de Windows Media Format 11 presenta nuevas características de administración de derechos digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="55ba3-114">The Windows Media Format 11 SDK introduces new digital rights management (DRM) features.</span></span> <span data-ttu-id="55ba3-115">Se han realizado los siguientes cambios en el SDK desde la versión 9,5.</span><span class="sxs-lookup"><span data-stu-id="55ba3-115">The following changes have been made to the SDK since the 9.5 release.</span></span>

## <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="55ba3-116">API extendidas del cliente DRM de Windows Media</span><span class="sxs-lookup"><span data-stu-id="55ba3-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="55ba3-117">El SDK de Windows Media Format 11 incluye un nuevo conjunto de API de DRM.</span><span class="sxs-lookup"><span data-stu-id="55ba3-117">The Windows Media Format 11 SDK ships with a new set of DRM APIs.</span></span> <span data-ttu-id="55ba3-118">Estas API se implementan en su propia biblioteca.</span><span class="sxs-lookup"><span data-stu-id="55ba3-118">These APIs are implemented in their own library.</span></span> <span data-ttu-id="55ba3-119">Muchas de las características DRM admitidas por los objetos del SDK de Windows Media Format también se admiten en las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="55ba3-119">Many of the DRM features supported by the objects of the Windows Media Format SDK are also supported by the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="55ba3-120">La principal diferencia en las nuevas API es que no confían en que un archivo ASF funcione.</span><span class="sxs-lookup"><span data-stu-id="55ba3-120">The primary difference in the new APIs is that they do not rely on having an ASF file to work.</span></span> <span data-ttu-id="55ba3-121">En su lugar, las nuevas API tratan directamente con el almacén de licencias local, a menudo con el identificador de clave para identificar las licencias.</span><span class="sxs-lookup"><span data-stu-id="55ba3-121">Instead, the new APIs deal with the local license store directly, often using the key ID to identify licenses.</span></span>

<span data-ttu-id="55ba3-122">Para obtener más información, consulte la documentación sobre las [API extendidas del cliente DRM de Windows Media](windows-media-drm-client-extended-apis.md) .</span><span class="sxs-lookup"><span data-stu-id="55ba3-122">For more information, see the [Windows Media DRM Client Extended APIs](windows-media-drm-client-extended-apis.md) documentation.</span></span>

## <a name="updated-codecs"></a><span data-ttu-id="55ba3-123">Códecs actualizados</span><span class="sxs-lookup"><span data-stu-id="55ba3-123">Updated Codecs</span></span>

<span data-ttu-id="55ba3-124">El códec de perfil avanzado de Windows Media Video 9 se ha actualizado para generar un flujo de bits comprimido que es compatible con el estándar SMPTE VC-1 publicado.</span><span class="sxs-lookup"><span data-stu-id="55ba3-124">The Windows Media Video 9 Advanced Profile codec has been updated to produce a compressed bit stream that is compliant with the published SMPTE VC-1 standard.</span></span>

<span data-ttu-id="55ba3-125">El códec Windows Media Audio 10 Professional también se incluye en esta versión del SDK.</span><span class="sxs-lookup"><span data-stu-id="55ba3-125">The Windows Media Audio 10 Professional codec is also included in this release of the SDK.</span></span> <span data-ttu-id="55ba3-126">El nuevo códec de audio presenta una calidad mejorada a velocidades de bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="55ba3-126">The new audio codec features improved quality at lower bit rates.</span></span>

## <a name="thumbnail-right"></a><span data-ttu-id="55ba3-127">Miniatura derecha</span><span class="sxs-lookup"><span data-stu-id="55ba3-127">Thumbnail Right</span></span>

<span data-ttu-id="55ba3-128">Las aplicaciones pueden solicitar una nueva acción DRM para leer el vídeo y crear una imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="55ba3-128">Applications can request a new DRM action to read from video to create a thumbnail image.</span></span> <span data-ttu-id="55ba3-129">Esto permite que las aplicaciones creen y muestren imágenes en miniatura de archivos de vídeo sin abrir el archivo para su reproducción.</span><span class="sxs-lookup"><span data-stu-id="55ba3-129">This enables applications to create and display thumbnail images for video files without opening the file for playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55ba3-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55ba3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55ba3-131">**Acerca del SDK de Windows Media Format**</span><span class="sxs-lookup"><span data-stu-id="55ba3-131">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




