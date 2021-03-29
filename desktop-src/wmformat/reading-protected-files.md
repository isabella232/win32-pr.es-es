---
title: Leer archivos protegidos
description: Leer archivos protegidos
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- SDK de Windows Media Format, leer archivos protegidos
- SDK de Windows Media Format, archivos protegidos
- Advanced Systems Format (ASF), leer archivos protegidos
- ASF (formato de sistemas avanzados), lectura de archivos protegidos
- Advanced Systems Format (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Advanced Systems Format (ASF), WMStubDRM. lib
- ASF (formato de sistemas avanzados), WMStubDRM. lib
- WMStubDRM. lib, leer archivos protegidos
- WMStubDRM. lib, archivos protegidos
- Administración de derechos digitales (DRM), WMStubDRM. lib
- DRM (administración de derechos digitales), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788697"
---
# <a name="reading-protected-files"></a><span data-ttu-id="6aeeb-115">Leer archivos protegidos</span><span class="sxs-lookup"><span data-stu-id="6aeeb-115">Reading Protected Files</span></span>

<span data-ttu-id="6aeeb-116">La lectura de un archivo o una secuencia de red protegida con DRM implica básicamente intentar abrir el archivo (o conectarse a la secuencia) y, a continuación, controlar los eventos que puedan enviarse desde los componentes de DRM.</span><span class="sxs-lookup"><span data-stu-id="6aeeb-116">Reading a DRM-protected file or network stream basically involves attempting to open the file (or connect to the stream) and then handling any events that might be sent from the DRM components.</span></span>

<span data-ttu-id="6aeeb-117">Si un reproductor no es compatible con DRM (no se vincula a una biblioteca wmstubdrm. lib válida), se produce un error en la llamada a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) cuando intenta abrir un archivo protegido y devuelve el \_ contenido protegido de NS e \_ \_ o algún error relacionado.</span><span class="sxs-lookup"><span data-stu-id="6aeeb-117">If a player is not DRM-enabled (does not link to a valid wmstubdrm.lib library) the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) call fails when it tries to open a protected file and returns NS\_E\_PROTECTED\_CONTENT or some related error.</span></span>

<span data-ttu-id="6aeeb-118">Cuando una aplicación habilitada para DRM intenta abrir un archivo protegido con DRM, el componente DRM busca automáticamente una licencia válida en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="6aeeb-118">When a DRM-enabled application attempts to open a DRM-protected file, the DRM component automatically searches the local system for a valid license.</span></span> <span data-ttu-id="6aeeb-119">Si se encuentra uno, el componente DRM descifra automáticamente el archivo de forma que sea completamente transparente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6aeeb-119">If one is found, the DRM component automatically decrypts the file in a way that is completely transparent to the application.</span></span> <span data-ttu-id="6aeeb-120">La acción que puede realizar una aplicación en el archivo descifrado depende de los derechos especificados en la licencia.</span><span class="sxs-lookup"><span data-stu-id="6aeeb-120">The action that an application may perform on the decrypted file depends on the rights specified in the license.</span></span> <span data-ttu-id="6aeeb-121">Para obtener una descripción completa de los derechos posibles, consulte la documentación del SDK de Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="6aeeb-121">For a full description of possible rights, see the Windows Media Rights Manager SDK documentation.</span></span>

<span data-ttu-id="6aeeb-122">Si la aplicación no tiene una licencia válida para un archivo, el reproductor recibe una notificación de estado del componente DRM.</span><span class="sxs-lookup"><span data-stu-id="6aeeb-122">If the application does not have a valid license for a file, the player receives a status notification from the DRM component.</span></span> <span data-ttu-id="6aeeb-123">A continuación, la aplicación de reproducción puede iniciar el proceso de [*adquisición de licencias*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="6aeeb-123">The player application can then initiate the [*license acquisition*](wmformat-glossary.md) process.</span></span> <span data-ttu-id="6aeeb-124">Una vez recibida una licencia válida, se puede tener acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="6aeeb-124">After a valid license has been received, the file can be accessed.</span></span> <span data-ttu-id="6aeeb-125">En las secciones siguientes se describen las tareas básicas que una aplicación debe realizar para implementar el proceso de adquisición de licencias:</span><span class="sxs-lookup"><span data-stu-id="6aeeb-125">The following sections describe the basic tasks that an application must perform in implementing the license acquisition process:</span></span>

-   [<span data-ttu-id="6aeeb-126">Especificar las acciones que se van a realizar</span><span class="sxs-lookup"><span data-stu-id="6aeeb-126">Specifying the Actions To Be Performed</span></span>](specifying-the-actions-to-be-performed.md)
-   [<span data-ttu-id="6aeeb-127">Control de eventos de adquisición de licencias</span><span class="sxs-lookup"><span data-stu-id="6aeeb-127">Handling License Acquisition Events</span></span>](handling-license-acquisition-events.md)
-   [<span data-ttu-id="6aeeb-128">Individualización de aplicaciones DRM</span><span class="sxs-lookup"><span data-stu-id="6aeeb-128">Individualizing DRM Applications</span></span>](individualizing-drm-applications.md)
-   [<span data-ttu-id="6aeeb-129">Control de eventos de individualización</span><span class="sxs-lookup"><span data-stu-id="6aeeb-129">Handling Individualization Events</span></span>](handling-individualization-events.md)

> [!Note]  
> <span data-ttu-id="6aeeb-130">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="6aeeb-130">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6aeeb-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6aeeb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6aeeb-132">**Características de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="6aeeb-132">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="6aeeb-133">**Lista de atributos de DRM**</span><span class="sxs-lookup"><span data-stu-id="6aeeb-133">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="6aeeb-134">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="6aeeb-134">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="6aeeb-135">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="6aeeb-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




