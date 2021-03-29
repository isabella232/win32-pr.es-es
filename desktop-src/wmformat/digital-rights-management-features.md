---
title: Características de Rights Management digital
description: Características de Rights Management digital
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- SDK de Windows Media Format, características DRM
- Administración de derechos digitales (DRM), características
- DRM (administración de derechos digitales), características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd9c30b350fdf430d5b20bbe112c5309ac9da4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792159"
---
# <a name="digital-rights-management-features"></a><span data-ttu-id="cd64f-106">Características de Rights Management digital</span><span class="sxs-lookup"><span data-stu-id="cd64f-106">Digital Rights Management Features</span></span>

<span data-ttu-id="cd64f-107">\[La característica Windows Media DRM está en desuso y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="cd64f-107">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="cd64f-108">En su lugar, use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="cd64f-108">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="cd64f-109">La administración de derechos digitales (DRM) es una tecnología que los propietarios de contenido pueden utilizar para proteger los archivos multimedia digitales mediante su cifrado con una clave (un fragmento de datos que bloquea y desbloquea el contenido).</span><span class="sxs-lookup"><span data-stu-id="cd64f-109">Digital rights management (DRM) is a technology that content owners can use to protect digital media files by encrypting them with a key (a piece of data that locks and unlocks the content).</span></span> <span data-ttu-id="cd64f-110">Para reproducir un archivo ASF protegido, el consumidor debe obtener una licencia independiente que contenga la clave.</span><span class="sxs-lookup"><span data-stu-id="cd64f-110">To play a protected ASF file, a consumer must obtain a separate license containing the key.</span></span> <span data-ttu-id="cd64f-111">Cada licencia también contiene derechos, determinados por el propietario del contenido o el emisor de la licencia, que especifican cómo el consumidor puede utilizar el archivo.</span><span class="sxs-lookup"><span data-stu-id="cd64f-111">Each license also contains rights, determined by the content owner or license issuer, which specify how the consumer can use the file.</span></span> <span data-ttu-id="cd64f-112">Con la tecnología DRM, los propietarios de contenido pueden ofrecer canciones, vídeos y otros archivos multimedia digitales a través de Internet en un formato de archivo protegido y controlar el uso de su contenido digital.</span><span class="sxs-lookup"><span data-stu-id="cd64f-112">Using DRM technology, content owners can deliver songs, videos, and other digital media files over the Internet in a protected file format and control the use of their digital content.</span></span> <span data-ttu-id="cd64f-113">La tecnología DRM de Microsoft también es compatible con Windows Media Rights Manager, Windows Media Encoder y Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="cd64f-113">Microsoft DRM technology is also supported by the Windows Media Rights Manager, the Windows Media Encoder, and Windows Media Player.</span></span> <span data-ttu-id="cd64f-114">Para obtener más información general sobre la tecnología DRM de Microsoft, vea el [sitio web de Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).</span><span class="sxs-lookup"><span data-stu-id="cd64f-114">For more background information on Microsoft's DRM technology, see the [Microsoft Windows Media Web site](https://support.microsoft.com/help/17946/windows-media).</span></span>

> [!Note]  
> <span data-ttu-id="cd64f-115">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="cd64f-115">DRM is not supported by the x64-based version of this SDK.</span></span>

 

<span data-ttu-id="cd64f-116">En las secciones siguientes se describen las características principales relacionadas con DRM del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="cd64f-116">The following sections discuss the main DRM-related features of the Windows Media Format SDK.</span></span>



| <span data-ttu-id="cd64f-117">Sección</span><span class="sxs-lookup"><span data-stu-id="cd64f-117">Section</span></span>                                                                                            | <span data-ttu-id="cd64f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd64f-118">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd64f-119">Aspectos básicos de DRM</span><span class="sxs-lookup"><span data-stu-id="cd64f-119">DRM Basics</span></span>](drm-basics.md)                                                                       | <span data-ttu-id="cd64f-120">Proporciona una breve introducción a la funcionalidad DRM proporcionada por el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="cd64f-120">Provides a brief overview of the DRM functionality provided by the Windows Media Format SDK.</span></span>                                         |
| [<span data-ttu-id="cd64f-121">Versiones de DRM</span><span class="sxs-lookup"><span data-stu-id="cd64f-121">DRM Versions</span></span>](drm-versions.md)                                                                   | <span data-ttu-id="cd64f-122">Describe las principales diferencias entre las versiones de la protección DRM disponible para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="cd64f-122">Describes the main differences between the versions of DRM protection available to applications.</span></span>                                     |
| [<span data-ttu-id="cd64f-123">DRM en vivo</span><span class="sxs-lookup"><span data-stu-id="cd64f-123">Live DRM</span></span>](live-drm.md)                                                                           | <span data-ttu-id="cd64f-124">Describe los escenarios que se pueden realizar mediante la protección DRM "sobre la marcha".</span><span class="sxs-lookup"><span data-stu-id="cd64f-124">Describes the scenarios made possible by "on the fly" DRM protection.</span></span>                                                                |
| [<span data-ttu-id="cd64f-125">Individualización de DRM</span><span class="sxs-lookup"><span data-stu-id="cd64f-125">DRM Individualization</span></span>](drm-individualization.md)                                                 | <span data-ttu-id="cd64f-126">Describe la actualización de seguridad de la aplicación que pueden requerir los propietarios de contenido o los emisores de licencias de DRM.</span><span class="sxs-lookup"><span data-stu-id="cd64f-126">Describes the application security upgrade that DRM content owners or license issuers can require.</span></span>                                   |
| [<span data-ttu-id="cd64f-127">Copia de seguridad y restauración de licencias de DRM</span><span class="sxs-lookup"><span data-stu-id="cd64f-127">Backing Up and Restoring of DRM Licenses</span></span>](backing-up-and-restoring-of-drm-licenses.md)           | <span data-ttu-id="cd64f-128">Describe las ventajas y desventajas de permitir que los usuarios realicen copias de seguridad de sus licencias de contenido y las restauren.</span><span class="sxs-lookup"><span data-stu-id="cd64f-128">Describes the pros and cons of permitting users to back up and restore their content licenses.</span></span>                                       |
| [<span data-ttu-id="cd64f-129">Ver atributos DRM en el editor de metadatos</span><span class="sxs-lookup"><span data-stu-id="cd64f-129">Viewing DRM Attributes in the Metadata Editor</span></span>](viewing-drm-attributes-in-the-metadata-editor.md) | <span data-ttu-id="cd64f-130">Describe las capacidades de este objeto auxiliar DRM y los escenarios para los que se diseñó la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="cd64f-130">Describes the capabilities of this DRM helper object and the scenarios it was designed to support.</span></span>                                   |
| [<span data-ttu-id="cd64f-131">Niveles de protección de salida</span><span class="sxs-lookup"><span data-stu-id="cd64f-131">Output Protection Levels</span></span>](output-protection-levels.md)                                           | <span data-ttu-id="cd64f-132">Describe cómo los niveles de protección de salida hacen que las licencias de la versión 10 de DRM sean más flexibles.</span><span class="sxs-lookup"><span data-stu-id="cd64f-132">Describes how Output Protection Levels make DRM version 10 licenses more flexible.</span></span>                                                   |
| [<span data-ttu-id="cd64f-133">Revocación de licencia</span><span class="sxs-lookup"><span data-stu-id="cd64f-133">License Revocation</span></span>](license-revocation.md)                                                       | <span data-ttu-id="cd64f-134">Describe la revocación de licencias.</span><span class="sxs-lookup"><span data-stu-id="cd64f-134">Describes license revocation.</span></span>                                                                                                        |
| [<span data-ttu-id="cd64f-135">Windows Media DRM 10 para dispositivos de red</span><span class="sxs-lookup"><span data-stu-id="cd64f-135">Windows Media DRM 10 for Network Devices</span></span>](windows-media-drm-10-for-network-devices.md)           | <span data-ttu-id="cd64f-136">Presenta Windows Media DRM 10 para dispositivos de red y su implementación en este SDK.</span><span class="sxs-lookup"><span data-stu-id="cd64f-136">Introduces Windows Media DRM 10 for Network Devices and its implementation in this SDK.</span></span>                                              |
| [<span data-ttu-id="cd64f-137">Ruta de acceso de audio seguro de Microsoft</span><span class="sxs-lookup"><span data-stu-id="cd64f-137">Microsoft Secure Audio Path</span></span>](microsoft-secure-audio-path--deprecated.md)                         | <span data-ttu-id="cd64f-138">Describe la arquitectura de la ruta de acceso de audio seguro de Microsoft, que proporciona el mayor grado de protección para el contenido de audio protegido.</span><span class="sxs-lookup"><span data-stu-id="cd64f-138">Describes the Microsoft Secure Audio Path architecture, which provides the highest degree of protection for protected audio content.</span></span> |
| [<span data-ttu-id="cd64f-139">Grabación de listas de reproducción</span><span class="sxs-lookup"><span data-stu-id="cd64f-139">Playlist Burning</span></span>](playlist-burning.md)                                                           | <span data-ttu-id="cd64f-140">Describe la característica de grabación de listas de reproducción de DRM y cómo se admite en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="cd64f-140">Describes the playlist-burning feature of DRM and how it is supported in the Windows Media Format SDK.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="cd64f-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd64f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd64f-142">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="cd64f-142">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="cd64f-143">**Características**</span><span class="sxs-lookup"><span data-stu-id="cd64f-143">**Features**</span></span>](features.md)
</dt> </dl>

 

 