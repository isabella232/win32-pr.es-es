---
title: Deshabilitar la salida digital (desusado)
description: Deshabilitar la salida digital (desusado)
ms.assetid: 208ceb23-e0a0-4dee-aeba-e9d640248f75
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- Administración de derechos digitales (DRM), Microsoft Secure audio Path (SAP)
- DRM (administración de derechos digitales), Microsoft Secure audio Path (SAP)
- SDK de Windows Media Format, ruta de acceso de audio segura (SAP)
- Administración de derechos digitales (DRM), ruta de acceso de audio segura (SAP)
- DRM (administración de derechos digitales), ruta de acceso de audio segura (SAP)
- Microsoft Secure audio Path (SAP), deshabilitar la salida digital
- Ruta de acceso de audio segura (SAP), deshabilitar la salida digital
- SAP (ruta de acceso segura de audio), deshabilitar la salida digital
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a667034d6b56a3f764865205681847b195eaaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419140"
---
# <a name="disabling-digital-output-deprecated"></a><span data-ttu-id="bbba4-112">Deshabilitar la salida digital (desusado)</span><span class="sxs-lookup"><span data-stu-id="bbba4-112">Disabling Digital Output (deprecated)</span></span>

<span data-ttu-id="bbba4-113">En esta página se documenta una característica que se admitirá con una solución técnica diferente en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="bbba4-113">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="bbba4-114">Otra característica de la ruta de acceso de audio seguro de Microsoft es la posibilidad de deshabilitar la salida digital.</span><span class="sxs-lookup"><span data-stu-id="bbba4-114">Another feature of Microsoft Secure Audio Path is the ability to disable digital output.</span></span> <span data-ttu-id="bbba4-115">Ciertas tarjetas de sonido proporcionan una manera de enviar salidas digitales desde un dispositivo de hardware. Estos dispositivos pueden estar certificados y pasarán la autorización del componente kernel de DRM.</span><span class="sxs-lookup"><span data-stu-id="bbba4-115">Certain sound cards provide a way to send digital output from a hardware device; these devices might be certified and will pass authorization from the DRM kernel component.</span></span> <span data-ttu-id="bbba4-116">Por lo tanto, si una tarjeta de sonido legítima tiene habilitada la salida digital, los usuarios aún podrán capturar una grabación digital perfecta de música protegida.</span><span class="sxs-lookup"><span data-stu-id="bbba4-116">So, if a legitimate sound card has digital output enabled, people can still capture a perfect digital recording of protected music.</span></span>

<span data-ttu-id="bbba4-117">Esta característica permite a los propietarios de contenido o a los emisores de licencias deshabilitar la salida digital estableciendo un parámetro en las licencias para su música.</span><span class="sxs-lookup"><span data-stu-id="bbba4-117">This feature lets content owners or license issuers disable digital output by setting a parameter in licenses for their music.</span></span> <span data-ttu-id="bbba4-118">Si se establece este parámetro, la tarjeta de sonido deshabilita su capacidad de salida digital al reproducir música protegida.</span><span class="sxs-lookup"><span data-stu-id="bbba4-118">If this parameter is set, the sound card disables its digital output capability when playing protected music.</span></span> <span data-ttu-id="bbba4-119">Los usuarios pueden escuchar música descifrada, pero no pueden realizar copias.</span><span class="sxs-lookup"><span data-stu-id="bbba4-119">Users can listen to decrypted music, but they cannot make copies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbba4-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bbba4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbba4-121">**Ruta de acceso de audio seguro de Microsoft**</span><span class="sxs-lookup"><span data-stu-id="bbba4-121">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




