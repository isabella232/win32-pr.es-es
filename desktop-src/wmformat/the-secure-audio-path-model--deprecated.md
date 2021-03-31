---
title: Modelo de ruta de acceso de audio segura (desusado)
description: Modelo de ruta de acceso de audio segura (desusado)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- Administración de derechos digitales (DRM), Microsoft Secure audio Path (SAP)
- DRM (administración de derechos digitales), Microsoft Secure audio Path (SAP)
- SDK de Windows Media Format, ruta de acceso de audio segura (SAP)
- Administración de derechos digitales (DRM), ruta de acceso de audio segura (SAP)
- DRM (administración de derechos digitales), ruta de acceso de audio segura (SAP)
- Microsoft Secure audio Path (SAP), modelo
- Ruta de acceso de audio seguro (SAP), modelo
- SAP (ruta de acceso segura de audio), modelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee21d05113deb3c4e8d64141374c87da090f41c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418597"
---
# <a name="the-secure-audio-path-model-deprecated"></a><span data-ttu-id="77d87-112">Modelo de ruta de acceso de audio segura (desusado)</span><span class="sxs-lookup"><span data-stu-id="77d87-112">The Secure Audio Path Model (deprecated)</span></span>

<span data-ttu-id="77d87-113">En esta página se documenta una característica que se admitirá con una solución técnica diferente en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="77d87-113">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="77d87-114">Microsoft Secure audio Path (SAP) es una característica de Microsoft Windows® me y Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77d87-114">Microsoft Secure Audio Path (SAP) is a feature of Microsoft Windows® Me and Microsoft Windows XP.</span></span> <span data-ttu-id="77d87-115">El requisito de que se reproduzca un archivo de audio solo a través de una ruta de acceso de audio segura se especifica en la licencia de DRM y lo aplican los componentes de cliente DRM.</span><span class="sxs-lookup"><span data-stu-id="77d87-115">The requirement that an audio file be played only through a secure audio path is specified in the DRM license and enforced by the DRM client components.</span></span> <span data-ttu-id="77d87-116">No se agrega ningún cifrado adicional para los archivos solo de SAP cuando están protegidos inicialmente.</span><span class="sxs-lookup"><span data-stu-id="77d87-116">There is no extra encryption added for SAP-only files when they are initially protected.</span></span> <span data-ttu-id="77d87-117">Los componentes de DRM agregan automáticamente el cifrado de SAP en el momento de la reproducción, como es el proceso de autenticación para todos los componentes de software implicados en la reproducción.</span><span class="sxs-lookup"><span data-stu-id="77d87-117">The SAP encryption is added automatically by the DRM components at playback time, as is the authentication process for all software components involved in playback.</span></span> <span data-ttu-id="77d87-118">Por lo tanto, el funcionamiento de SAP es completamente transparente para las aplicaciones y, por eso, no hay ningún método o propiedad en el SDK de Windows Media Format para habilitar o deshabilitar SAP.</span><span class="sxs-lookup"><span data-stu-id="77d87-118">The workings of SAP are therefore completely transparent to applications, and that is why there is no method or property in the Windows Media Format SDK for enabling or disabling SAP.</span></span> <span data-ttu-id="77d87-119">Si lo desea, al crear un archivo protegido, el propietario del contenido puede Agregar un atributo de encabezado personalizado denominado algo como "DRMHeader. SAPRequired" para indicar a un servidor de licencias que agregue el requisito de SAP a la licencia.</span><span class="sxs-lookup"><span data-stu-id="77d87-119">If desired, when creating a protected file a content owner can add a custom header attribute called something like "DRMHeader.SAPRequired" in order to instruct a license server to add the SAP requirement to the license.</span></span> <span data-ttu-id="77d87-120">La implementación de este tipo de esquema depende del propietario del contenido y del servicio de licencias.</span><span class="sxs-lookup"><span data-stu-id="77d87-120">The implementation of such a scheme is up to the content owner and the license service.</span></span>

<span data-ttu-id="77d87-121">En el modelo DRM actual, si no se aplica SAP, cuando se reproduce la música digital protegida, el contenido cifrado pasa al componente cliente DRM.</span><span class="sxs-lookup"><span data-stu-id="77d87-121">In the current DRM model, if SAP is not applied, when protected digital music is played, the encrypted content passes to the DRM client component.</span></span> <span data-ttu-id="77d87-122">El cliente DRM comprueba que la aplicación y el componente DRM que incorpora el SDK de Windows Media Format son válidos.</span><span class="sxs-lookup"><span data-stu-id="77d87-122">The DRM client verifies that the application and the DRM component incorporating the Windows Media Format SDK are valid.</span></span> <span data-ttu-id="77d87-123">Si son válidos, el cliente DRM descifra el contenido y lo envía a la aplicación, que luego lo envía a los componentes de audio de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="77d87-123">If they are valid, the DRM client decrypts the content and sends it to the application, which then sends it to the lower-level audio components.</span></span> <span data-ttu-id="77d87-124">En este momento, la música descifrada está disponible para las aplicaciones en modo usuario y los complementos y controladores de modo kernel que pueden interceptar los bits de audio descifrados.</span><span class="sxs-lookup"><span data-stu-id="77d87-124">At this point, the decrypted music is available to user mode applications and plug-ins and kernel mode drivers that can intercept the decrypted audio bits.</span></span>

<span data-ttu-id="77d87-125">Cuando se aplica el requisito de la ruta de acceso de audio segura, la aplicación no descifra el contenido, sino que se pasa a un estado cifrado a los componentes de nivel inferior, que Microsoft ha autenticado como de confianza.</span><span class="sxs-lookup"><span data-stu-id="77d87-125">When the Secure Audio Path requirement is applied, the content is not decrypted by the application, but rather is passed in an encrypted state to lower level components, all of which have been authenticated by Microsoft as trustworthy.</span></span> <span data-ttu-id="77d87-126">Un componente de audio de confianza es aquél que no hace que el contenido de audio esté disponible para ningún componente del sistema, excepto otros componentes de confianza específicos.</span><span class="sxs-lookup"><span data-stu-id="77d87-126">A trusted audio component is one that does not make the audio content available to any system component except other specific trusted components.</span></span> <span data-ttu-id="77d87-127">De esta manera, el contenido digital permanece protegido hasta el nivel del controlador.</span><span class="sxs-lookup"><span data-stu-id="77d87-127">In this way, the digital content remains protected all the way down to the driver level.</span></span>

<span data-ttu-id="77d87-128">En el diagrama siguiente se muestra el modelo actual en comparación con el modelo de ruta de acceso de audio segura.</span><span class="sxs-lookup"><span data-stu-id="77d87-128">The following diagram displays the current model in comparison to the Secure Audio Path model.</span></span>

![diagrama del modelo de ruta de acceso de audio segura](images/sap.png)

 

 




