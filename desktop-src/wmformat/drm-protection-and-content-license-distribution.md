---
title: Protección de DRM y distribución de licencias de contenido
description: Protección de DRM y distribución de licencias de contenido
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- SDK de Windows Media Format, protección de contenido DRM
- SDK de Windows Media Format, licencias de DRM
- Advanced Systems Format (ASF), protección de contenido DRM
- ASF (formato de sistemas avanzados), protección de contenido DRM
- Advanced Systems Format (ASF), distribución de licencias de DRM
- ASF (formato de sistemas avanzados), distribución de licencias de DRM
- Administración de derechos digitales (DRM), protección de contenido
- DRM (administración de derechos digitales), protección de contenido
- Administración de derechos digitales (DRM), distribución de licencias
- DRM (administración de derechos digitales), distribución de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af13947828885d70f3e0fd9fe8bf035eb8c5e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357744"
---
# <a name="drm-protection-and-content-license-distribution"></a><span data-ttu-id="4f1c6-113">Protección de DRM y distribución de licencias de contenido</span><span class="sxs-lookup"><span data-stu-id="4f1c6-113">DRM Protection and Content License Distribution</span></span>

<span data-ttu-id="4f1c6-114">En el lado de la creación, la tecnología de administración de derechos digitales implica dos procesos principales: (1) protección del contenido y (2) proporcionar licencias para el contenido.</span><span class="sxs-lookup"><span data-stu-id="4f1c6-114">On the creation side, digital rights management technology involves two main processes: (1) protecting the content and (2) providing licenses for the content.</span></span> <span data-ttu-id="4f1c6-115">La protección de un archivo básicamente implica el cifrado del contenido y la inclusión de una dirección URL en el encabezado del archivo que especifica dónde se puede obtener una licencia para el contenido.</span><span class="sxs-lookup"><span data-stu-id="4f1c6-115">Protecting a file basically involves encrypting the content, and including a URL in the file header that specifies where a license for the content may be obtained.</span></span> <span data-ttu-id="4f1c6-116">Si desea proteger los archivos con y, a continuación, distribuir los archivos a otros equipos o dispositivos, puede usar el SDK de Windows Media Format o el SDK de Windows Media Rights Manager para proteger el archivo.</span><span class="sxs-lookup"><span data-stu-id="4f1c6-116">If you want to protect files with and then distribute the files to other computers or devices, you can use either the Windows Media Format SDK or the Windows Media Rights Manager SDK to protect the file.</span></span> <span data-ttu-id="4f1c6-117">En escenarios Live-DRM, debe usar el SDK de Windows Media Format para proteger el contenido a medida que se codifica.</span><span class="sxs-lookup"><span data-stu-id="4f1c6-117">For live-DRM scenarios, you must use the Windows Media Format SDK to protect the content as it is being encoded.</span></span>

<span data-ttu-id="4f1c6-118">Para crear y emitir licencias para contenido protegido, puede crear su propia solución personalizada mediante los objetos del SDK de Windows Media Rights Manager, o puede usar un servicio ejecutado por terceros.</span><span class="sxs-lookup"><span data-stu-id="4f1c6-118">To create and issue licenses for protected content, you can create your own custom solution using the objects of the Windows Media Rights Manager SDK, or you can use a service run by a third party.</span></span>

<span data-ttu-id="4f1c6-119">Sea cual sea el método que use, los archivos protegidos que cree contendrán, en el objeto de encabezado DRM, una dirección URL que indica a las aplicaciones cliente dónde obtener una licencia para el contenido.</span><span class="sxs-lookup"><span data-stu-id="4f1c6-119">Whichever method you use, the protected files that you create will contain, in the DRM header object, a URL that tells client applications where to obtain a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="4f1c6-120">El SDK de Windows Media Format no proporciona compatibilidad para crear o emitir licencias.</span><span class="sxs-lookup"><span data-stu-id="4f1c6-120">The Windows Media Format SDK does not provide support for creating or issuing licenses.</span></span>

 

<span data-ttu-id="4f1c6-121">En el lado de reproducción, una aplicación habilitada para DRM debe poder obtener licencias para el contenido protegido, descifrar el contenido con la clave incluida en la licencia y aplicar las restricciones de licencia, como el número de veces que se puede reproducir un archivo, o si el archivo se puede copiar en otro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f1c6-121">On the playback side, a DRM-enabled application must be able to obtain licenses for protected content, to decrypt that content using the key contained in the license, and to enforce the license restrictions, such as the number of times a file may be played, or whether the file can be copied to another device.</span></span> <span data-ttu-id="4f1c6-122">El SDK de Windows Media Format proporciona toda la compatibilidad necesaria para crear una aplicación de reproducción DRM totalmente habilitada.</span><span class="sxs-lookup"><span data-stu-id="4f1c6-122">The Windows Media Format SDK provides all the support required to create a fully enabled DRM playback application.</span></span>

> [!Note]  
> <span data-ttu-id="4f1c6-123">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="4f1c6-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4f1c6-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f1c6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f1c6-125">**Características de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="4f1c6-125">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="4f1c6-126">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="4f1c6-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




