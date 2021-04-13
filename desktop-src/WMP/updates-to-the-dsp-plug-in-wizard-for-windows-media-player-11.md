---
title: Actualizaciones del Asistente para complementos de DSP para Windows Media Player 11
description: Actualizaciones del Asistente para complementos de DSP para Windows Media Player 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Complementos de Windows Media Player, Asistente para complementos
- complementos, Asistente para complementos
- Complementos de procesamiento de señal digital, Asistente para complementos
- Complementos DSP, Asistente para complementos
- Asistente para complementos
- Visual Studio, Asistente para complementos de DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420272"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a><span data-ttu-id="1f9a8-109">Actualizaciones del Asistente para complementos de DSP para Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="1f9a8-109">Updates to the DSP Plug-in Wizard for Windows Media Player 11</span></span>

<span data-ttu-id="1f9a8-110">El SDK de Windows Media Player 11 presenta los siguientes cambios en el Asistente para complementos de DSP:</span><span class="sxs-lookup"><span data-stu-id="1f9a8-110">The Windows Media Player 11 SDK introduces the following changes to the DSP plug-in wizard:</span></span>

-   <span data-ttu-id="1f9a8-111">Los complementos registran el modelo de subprocesos como "ambos".</span><span class="sxs-lookup"><span data-stu-id="1f9a8-111">Plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="1f9a8-112">Esto permite que el complemento se ejecute en la canalización de Media Foundation en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1f9a8-112">This enables the plug-in to run in the Media Foundation pipeline on Windows Vista.</span></span> <span data-ttu-id="1f9a8-113">Vea el archivo *projectname*. RGS.</span><span class="sxs-lookup"><span data-stu-id="1f9a8-113">See the *projectname*.rgs file.</span></span>

    -   <span data-ttu-id="1f9a8-114">Los complementos de DSP de audio tienen compatibilidad con los dos formatos adicionales siguientes:</span><span class="sxs-lookup"><span data-stu-id="1f9a8-114">Audio DSP plug-ins have support for the following two additional formats:</span></span>

    <!-- -->

    -   <span data-ttu-id="1f9a8-115">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="1f9a8-115">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
    -   <span data-ttu-id="1f9a8-116">\_Formato \_ de onda extensible con SUBformato KSDATAFORMAT \_ SubType \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="1f9a8-116">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

    <span data-ttu-id="1f9a8-117">Vea el archivo *projectname*. cpp.</span><span class="sxs-lookup"><span data-stu-id="1f9a8-117">See the *projectname*.cpp file.</span></span>

    1.  <span data-ttu-id="1f9a8-118">Los complementos de DSP de vídeo admiten el formato de vídeo NV12.</span><span class="sxs-lookup"><span data-stu-id="1f9a8-118">Video DSP plug-ins have support for the NV12 video format.</span></span>
    2.  <span data-ttu-id="1f9a8-119">Los complementos realizan llamadas adicionales a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) y [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuevo tipo de complemento: wmp \_ PLUGINTYPE \_ DSP \_ OUTOFPROC.</span><span class="sxs-lookup"><span data-stu-id="1f9a8-119">Plug-ins make additional calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC.</span></span> <span data-ttu-id="1f9a8-120">Vea el archivo *projectnamedll*. cpp del proyecto.</span><span class="sxs-lookup"><span data-stu-id="1f9a8-120">See the project's *projectnamedll*.cpp file.</span></span>
    3.  <span data-ttu-id="1f9a8-121">Un proyecto adicional en cada solución crea un archivo DLL de proxy/stub para la interfaz personalizada de configuración de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="1f9a8-121">An additional project in each solution creates a proxy/stub DLL for the property page settings custom interface.</span></span> <span data-ttu-id="1f9a8-122">Vea el proyecto *projectnamePS* .</span><span class="sxs-lookup"><span data-stu-id="1f9a8-122">See the *projectnamePS* project.</span></span>
    4.  <span data-ttu-id="1f9a8-123">Las llamadas a métodos en desuso se han cambiado para usar las versiones más recientes.</span><span class="sxs-lookup"><span data-stu-id="1f9a8-123">Calls to deprecated methods have been changed to use the newest versions.</span></span>
    5.  <span data-ttu-id="1f9a8-124">El asistente puede generar un complemento de modo dual que funcione como DMO, implementando **IMediaObject** y como MFT, implementando **IMFTransform**.</span><span class="sxs-lookup"><span data-stu-id="1f9a8-124">The wizard can generate a dual-mode plug-in that functions both as a DMO, by implementing **IMediaObject**, and as an MFT, by implementing **IMFTransform**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f9a8-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f9a8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f9a8-126">**Asistente para complementos de DSP**</span><span class="sxs-lookup"><span data-stu-id="1f9a8-126">**DSP Plug-in Wizard**</span></span>](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




