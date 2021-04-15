---
title: Ver o modificar la señal de música (desusado)
description: Ver o modificar la señal de música (desusado)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- Administración de derechos digitales (DRM), Microsoft Secure audio Path (SAP)
- DRM (administración de derechos digitales), Microsoft Secure audio Path (SAP)
- SDK de Windows Media Format, ruta de acceso de audio segura (SAP)
- Administración de derechos digitales (DRM), ruta de acceso de audio segura (SAP)
- DRM (administración de derechos digitales), ruta de acceso de audio segura (SAP)
- SDK de Windows Media Format, visualización o modificación de la señal de música
- Administración de derechos digitales (DRM), visualización o modificación de la señal de música
- DRM (administración de derechos digitales), visualización o modificación de la señal de música
- Microsoft Secure audio Path (SAP), visualización o modificación de la señal de música
- Ruta de acceso de audio seguro (SAP), visualización o modificación de la señal de música
- SAP (ruta de audio segura), visualización o modificación de la señal de música
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695452"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a><span data-ttu-id="cad10-115">Ver o modificar la señal de música (desusado)</span><span class="sxs-lookup"><span data-stu-id="cad10-115">Viewing or Modifying the Music Signal (deprecated)</span></span>

<span data-ttu-id="cad10-116">En esta página se documenta una característica que se admitirá con una solución técnica diferente en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="cad10-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="cad10-117">En el modelo de Microsoft Secure audio Path (SAP), las aplicaciones no pueden modificar la música protegida de ningún modo.</span><span class="sxs-lookup"><span data-stu-id="cad10-117">In the Microsoft Secure Audio Path (SAP) model, applications cannot modify protected music in any way.</span></span> <span data-ttu-id="cad10-118">Por ejemplo, cuando una aplicación intenta interceptar una señal de música, la señal suena como ruido aleatorio.</span><span class="sxs-lookup"><span data-stu-id="cad10-118">For example, when an application attempts to intercept a music signal, the signal sounds like random noise.</span></span> <span data-ttu-id="cad10-119">Como resultado, las aplicaciones que normalmente modifican señales (como un ecualizador) no pueden cambiar el sonido de la música.</span><span class="sxs-lookup"><span data-stu-id="cad10-119">As a result, applications that normally modify signals (such as an equalizer) cannot change the sound of the music.</span></span>

<span data-ttu-id="cad10-120">Algunas aplicaciones simplemente ven una señal de música.</span><span class="sxs-lookup"><span data-stu-id="cad10-120">Some applications merely view a music signal.</span></span> <span data-ttu-id="cad10-121">Por ejemplo, algunas aplicaciones muestran luces intermitentes en el tiempo con la señal de música, pero no la modifican.</span><span class="sxs-lookup"><span data-stu-id="cad10-121">For example, some applications display flashing lights in time with the music signal, but do not modify it.</span></span> <span data-ttu-id="cad10-122">Para dar cabida a las aplicaciones que ven las señales, una pequeña parte de la música se descifra y se pasa sin cifrar con el contenido cifrado.</span><span class="sxs-lookup"><span data-stu-id="cad10-122">To accommodate applications that view signals, a small part of the music is decrypted and passed in clear form with the encrypted content.</span></span> <span data-ttu-id="cad10-123">La señal resultante es muy deficiente (peor que la calidad de teléfono), pero puede ser suficiente para las aplicaciones que ven señales.</span><span class="sxs-lookup"><span data-stu-id="cad10-123">The resulting signal is very poor (worse than telephone quality) but can suffice for applications that view signals.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cad10-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cad10-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cad10-125">**Ruta de acceso de audio seguro de Microsoft**</span><span class="sxs-lookup"><span data-stu-id="cad10-125">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




