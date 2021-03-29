---
title: Individualización de aplicaciones DRM
description: Individualización de aplicaciones DRM
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- SDK de Windows Media Format, individualización de aplicaciones DRM
- SDK de Windows Media Format, aplicación en persona
- Advanced Systems Format (ASF), individualización de aplicaciones DRM
- ASF (formato de sistemas avanzados), individualización de aplicaciones DRM
- Advanced Systems Format (ASF), aplicación en persona
- ASF (formato de sistemas avanzados), aplicación en persona
- Administración de derechos digitales (DRM), individualización de aplicaciones
- DRM (administración de derechos digitales), individualización de aplicaciones
- Administración de derechos digitales (DRM), aplicación en persona
- DRM (administración de derechos digitales), aplicación en persona
- aplicación en persona
- individualización de aplicaciones DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "103995016"
---
# <a name="individualizing-drm-applications"></a><span data-ttu-id="fb3fb-115">Individualización de aplicaciones DRM</span><span class="sxs-lookup"><span data-stu-id="fb3fb-115">Individualizing DRM Applications</span></span>

<span data-ttu-id="fb3fb-116">Para aumentar la seguridad, se puede *individualizar* el componente DRM de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-116">To increase security, the DRM component of applications can be *individualized*.</span></span> <span data-ttu-id="fb3fb-117">Una aplicación individualizada es aquella que ha recibido una actualización a sus componentes de DRM que la diferencia de todas las demás copias de la misma aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-117">An individualized application is one that has received an upgrade to its DRM components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="fb3fb-118">Los propietarios de contenido pueden exigir que sus archivos protegidos se reproduzcan solo en una aplicación que se ha individualizado.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-118">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

<span data-ttu-id="fb3fb-119">El proceso de individualización se inicia cuando la aplicación se pone en contacto con el servicio de Microsoft individualización y, a continuación, instala una actualización de seguridad en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-119">The individualization process starts when the application contacts the Microsoft Individualization Service, which then installs a security upgrade on the user's computer.</span></span> <span data-ttu-id="fb3fb-120">Dado que el servicio de individualización controla la información del usuario, debe mostrar la Directiva de privacidad de Microsoft o proporcionar un vínculo a esa página en el sitio web de Microsoft: <https://privacy.microsoft.com/privacystatement> .</span><span class="sxs-lookup"><span data-stu-id="fb3fb-120">Because the Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft Web site: <https://privacy.microsoft.com/privacystatement>.</span></span>

<span data-ttu-id="fb3fb-121">La individualización puede realizarse de diferentes maneras.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-121">Individualization can be accomplished in different ways.</span></span> <span data-ttu-id="fb3fb-122">Por ejemplo, la individualización puede tener lugar cuando un usuario reproduce un archivo protegido.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-122">For example, individualization can take place when a user plays a protected file.</span></span> <span data-ttu-id="fb3fb-123">La solicitud de licencia se envía al [*servicio de licencias de Windows Media*](wmformat-glossary.md), que inspecciona el certificado de la aplicación que solicita la [*licencia*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fb3fb-123">The license request is sent to the [*Windows Media License Service*](wmformat-glossary.md), which inspects the certificate of the application requesting the [*license*](wmformat-glossary.md).</span></span> <span data-ttu-id="fb3fb-124">Si el componente DRM de la aplicación no se ha individualizado, el servicio de licencias de Windows Media rechaza emitir la licencia, ya que es la Directiva del servicio de licencias de Windows Media para emitir licencias solo a reproductores individualizados.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-124">If the DRM component of the application has not been individualized, Windows Media License Service refuses to issue the license, because it is the policy of Windows Media License Service to issue licenses only to individualized players.</span></span> <span data-ttu-id="fb3fb-125">A continuación, la aplicación puede notificar al usuario que la aplicación debe actualizarse.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-125">The application can then notify the user that the application must be upgraded.</span></span> <span data-ttu-id="fb3fb-126">Si el usuario acepta, se proporciona una actualización de seguridad para individualizar el componente DRM de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-126">If the user agrees, a security upgrade is provided to individualize the DRM component of the application.</span></span>

<span data-ttu-id="fb3fb-127">Para mejorar la experiencia del usuario, puede iniciar el proceso de individualización como un paso de actualización de seguridad durante la instalación. no se interrumpe al usuario para obtener una actualización de seguridad al intentar reproducir un archivo protegido.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-127">For a better user experience, you can initiate the individualization process as a security upgrade step during setup; then the user is not interrupted to get a security upgrade while trying to play a protected file.</span></span> <span data-ttu-id="fb3fb-128">También puede promover activamente la individualización agregando un comando de menú o un botón de **actualización de seguridad** a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-128">You can also actively encourage individualization by adding a **Security Upgrade** menu command or button to the application.</span></span>

> [!Note]  
> <span data-ttu-id="fb3fb-129">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="fb3fb-129">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fb3fb-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb3fb-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb3fb-131">**Características de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="fb3fb-131">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="fb3fb-132">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="fb3fb-132">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




