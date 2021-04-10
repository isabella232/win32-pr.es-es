---
title: Objeto de transcifrador DRM
description: Objeto de transcifrador DRM
ms.assetid: 50c041b3-6621-4618-843f-6ef9b8e741ab
keywords:
- SDK de Windows Media Format, objetos de transcifrador de DRM
- Advanced Systems Format (ASF), objetos de transcifrador de DRM
- ASF (formato de sistemas avanzados), objetos de transcifrador DRM
- objetos, objetos de transcifrador DRM
- Objetos de transcifrador de DRM
- SDK de formato de Windows Media, objetos de transcifrador
- Advanced Systems Format (ASF), objetos de transcifrador
- ASF (formato de sistemas avanzados), objetos de transcifrador
- objetos, objetos de transcifrador
- objetos de transcifrador
- Administración de derechos digitales (DRM), objetos de transcifrador
- DRM (administración de derechos digitales), objetos de transcifrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46213dd7ebfbe48ff22039c201dbff3aab462f5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149088"
---
# <a name="drm-transcryptor-object"></a><span data-ttu-id="b6816-115">Objeto de transcifrador DRM</span><span class="sxs-lookup"><span data-stu-id="b6816-115">DRM Transcryptor Object</span></span>

<span data-ttu-id="b6816-116">El objeto de transcifrador DRM convierte los archivos ASF protegidos con DRM en flujos de datos listos para ser enviados a dispositivos de red que utilizan Windows Media DRM 10 para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="b6816-116">The DRM transcryptor object converts DRM-protected ASF files into data streams ready to be sent to network devices that use Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="b6816-117">La función [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) crea el objeto de transcifrador DRM, que establece un puntero a la interfaz [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) .</span><span class="sxs-lookup"><span data-stu-id="b6816-117">The DRM transcryptor object is created by the [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) function, which sets a pointer to the [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) interface.</span></span> <span data-ttu-id="b6816-118">**IUnknown** y **IWMDRMTranscryptor** son las únicas interfaces que admite este objeto.</span><span class="sxs-lookup"><span data-stu-id="b6816-118">**IUnknown** and **IWMDRMTranscryptor** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6816-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6816-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6816-120">**Objects**</span><span class="sxs-lookup"><span data-stu-id="b6816-120">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




