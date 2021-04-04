---
title: Componente de kernel de DRM (desusado)
description: Componente de kernel de DRM (desusado)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- Administración de derechos digitales (DRM), Microsoft Secure audio Path (SAP)
- DRM (administración de derechos digitales), Microsoft Secure audio Path (SAP)
- SDK de Windows Media Format, ruta de acceso de audio segura (SAP)
- Administración de derechos digitales (DRM), ruta de acceso de audio segura (SAP)
- DRM (administración de derechos digitales), ruta de acceso de audio segura (SAP)
- SDK de Windows Media Format, componente de kernel DRM
- Administración de derechos digitales (DRM), componente de kernel
- DRM (administración de derechos digitales), componente de kernel
- Microsoft Secure audio Path (SAP), componente de kernel de DRM
- Ruta de acceso de audio seguro (SAP), componente de kernel DRM
- SAP (ruta de acceso de audio seguro), componente de kernel DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacc0074fdf390ca478ed41b59188ad42ec193c1
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078584"
---
# <a name="the-drm-kernel-component-deprecated"></a><span data-ttu-id="80538-115">Componente de kernel de DRM (desusado)</span><span class="sxs-lookup"><span data-stu-id="80538-115">The DRM Kernel Component (deprecated)</span></span>

<span data-ttu-id="80538-116">En esta página se documenta una característica que se admitirá con una solución técnica diferente en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="80538-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="80538-117">En el modelo de Microsoft Secure audio Path (SAP), el componente kernel de DRM proporciona dos características básicas que protegen la integridad de la música cifrada.</span><span class="sxs-lookup"><span data-stu-id="80538-117">In the Microsoft Secure Audio Path (SAP) model, the DRM kernel component provides two basic features that protect the integrity of encrypted music.</span></span>

<span data-ttu-id="80538-118">En primer lugar, el componente cliente DRM y el componente kernel DRM están en comunicación cuando se reproduce un archivo de música.</span><span class="sxs-lookup"><span data-stu-id="80538-118">First, the DRM client component and the DRM kernel component are in communication when a music file is played.</span></span> <span data-ttu-id="80538-119">Esta comunicación entre componentes impide que cualquier persona manipule la señal cifrada o inserte información falsa.</span><span class="sxs-lookup"><span data-stu-id="80538-119">This communication between components prevents anyone from tampering with the encrypted signal or from inserting false information.</span></span>

<span data-ttu-id="80538-120">En segundo lugar, el componente de kernel DRM no descifra la señal de música hasta que se autentiquen todos los componentes restantes.</span><span class="sxs-lookup"><span data-stu-id="80538-120">Second, the DRM kernel component does not decrypt the music signal until all remaining components are authenticated.</span></span> <span data-ttu-id="80538-121">Es decir, antes de descifrar el contenido y pasarlo al siguiente componente del sistema, el componente kernel de DRM comprueba cada componente que permanece en la ruta de acceso a la tarjeta de sonido (cada componente que puede tener acceso al contenido) y comprueba que estos componentes están firmados con un certificado de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="80538-121">That is, before decrypting content and passing it to the next system component, the DRM kernel component checks each component that remains in the path to the sound card (each component that can access the content) and verifies that these components are signed with a certificate from Microsoft.</span></span> <span data-ttu-id="80538-122">Un componente sin firmar podría indicar un componente sospechoso o un controlador malintencionado.</span><span class="sxs-lookup"><span data-stu-id="80538-122">An unsigned component might indicate a suspicious component or a malicious driver.</span></span> <span data-ttu-id="80538-123">Por lo tanto, cuando el componente de kernel DRM valida los componentes restantes, si alguno de los componentes produce un error en esta prueba, la señal se detiene y no se puede reproducir.</span><span class="sxs-lookup"><span data-stu-id="80538-123">So, when the DRM kernel component validates remaining components, if any component fails this test, the signal is halted and cannot be played.</span></span> <span data-ttu-id="80538-124">De lo contrario, si todos los componentes pasan la validación, el componente kernel de DRM descifra la música y la pasa al componente siguiente.</span><span class="sxs-lookup"><span data-stu-id="80538-124">Otherwise, if all components pass validation, the DRM kernel component decrypts the music and passes it to the next component.</span></span>

<span data-ttu-id="80538-125">Microsoft firma digitalmente los controladores que pasan las pruebas del laboratorio de calidad de hardware (WHQL) de Windows® para garantizar a los usuarios que usan los controladores de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="80538-125">Microsoft digitally signs drivers that pass the Windows® Hardware Quality Lab (WHQL) tests to assure users that they are using the highest-quality drivers.</span></span> <span data-ttu-id="80538-126">Esta práctica es estándar y garantiza la autenticidad de los componentes, ya que no se puede falsificar la firma ni se puede modificar el código sin destruir la firma.</span><span class="sxs-lookup"><span data-stu-id="80538-126">This practice is standard and guarantees the authenticity of components because the signature cannot be forged, nor can the code be modified without destroying the signature.</span></span> <span data-ttu-id="80538-127">Los controladores que están certificados para la ruta de acceso de audio segura deben proteger los datos de audio que procesan desde los componentes que no son de confianza.</span><span class="sxs-lookup"><span data-stu-id="80538-127">Drivers that are certified for Secure Audio Path must protect the audio data they process from access by untrusted components.</span></span> 

<span data-ttu-id="80538-128">Los controladores incluidos con Windows Millennium Edition y Windows XP se actualizan para la ruta de acceso de audio segura y con la firma.</span><span class="sxs-lookup"><span data-stu-id="80538-128">Drivers included with Windows Millennium Edition and Windows XP are updated for Secure Audio Path and signed.</span></span> <span data-ttu-id="80538-129">Los controladores que no están firmados para su uso con Windows me o Windows XP no pueden reproducir música protegida.</span><span class="sxs-lookup"><span data-stu-id="80538-129">Drivers that are not signed for use with Windows Me or Windows XP cannot play protected music.</span></span> <span data-ttu-id="80538-130">Los fabricantes de controladores pueden volver a emitir versiones actualizadas de sus controladores firmados por WHQL y publicarlos en Internet para que los consumidores lo descarguen.</span><span class="sxs-lookup"><span data-stu-id="80538-130">Driver manufacturers can reissue updated versions of their drivers that are signed by WHQL, and publish them on the Internet for consumers to download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80538-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80538-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80538-132">**Ruta de acceso de audio seguro de Microsoft**</span><span class="sxs-lookup"><span data-stu-id="80538-132">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




