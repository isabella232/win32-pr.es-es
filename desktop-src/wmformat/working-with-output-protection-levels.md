---
title: Trabajar con niveles de protección de salida
description: Trabajar con niveles de protección de salida
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows Media Format SDK, niveles de protección de salida (OPL)
- Windows Media Format SDK, niveles de protección
- Advanced Systems Format (ASF), niveles de protección de salida (OPL)
- ASF (formato de sistemas avanzados), niveles de protección de salida (OPL)
- Advanced Systems Format (ASF), niveles de protección
- ASF (formato de sistemas avanzados), niveles de protección
- Advanced Systems Format (ASF), varias licencias
- ASF (formato de sistemas avanzados), varias licencias
- Administración de derechos digitales (DRM), niveles de protección de salida (OPL)
- DRM (administración de derechos digitales), niveles de protección de salida (OPL)
- Administración de derechos digitales (DRM), niveles de protección
- DRM (administración de derechos digitales), niveles de protección
- Administración de derechos digitales (DRM), evaluación de los niveles de protección de salida (OPL)
- DRM (administración de derechos digitales), evaluación de los niveles de protección de salida (OPL)
- Administración de derechos digitales (DRM), varias licencias
- DRM (administración de derechos digitales), varias licencias
- niveles de protección de salida (OPL)
- OPL (niveles de protección de salida)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358668"
---
# <a name="working-with-output-protection-levels"></a><span data-ttu-id="602ea-121">Trabajar con niveles de protección de salida</span><span class="sxs-lookup"><span data-stu-id="602ea-121">Working with Output Protection Levels</span></span>

<span data-ttu-id="602ea-122">Las licencias creadas con el SDK de Windows Media Rights Manager 10 pueden especificar restricciones de acción mediante los niveles de protección de salida (OPLs).</span><span class="sxs-lookup"><span data-stu-id="602ea-122">Licenses created by using the Windows Media Rights Manager 10 SDK can specify action restrictions using output protection levels (OPLs).</span></span> <span data-ttu-id="602ea-123">OPLs permite a un creador de licencias permitir algunas acciones solo en dispositivos con tecnologías específicas.</span><span class="sxs-lookup"><span data-stu-id="602ea-123">OPLs enable a license creator to allow some actions only on devices with specific technologies.</span></span> <span data-ttu-id="602ea-124">Las ventajas de usar OPLs es que obtiene más flexibilidad a la hora de crear restricciones de licencia que las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="602ea-124">The benefits of using OPLs is that you get more flexibility in creating license restrictions than previous versions.</span></span> <span data-ttu-id="602ea-125">Además, los OPLs se pueden expandir para adaptarse a las tecnologías futuras.</span><span class="sxs-lookup"><span data-stu-id="602ea-125">In addition, OPLs are expandable to accommodate future technologies.</span></span> <span data-ttu-id="602ea-126">Puede admitir tales licencias en sus aplicaciones mediante los métodos de la interfaz [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) .</span><span class="sxs-lookup"><span data-stu-id="602ea-126">You can support such licenses in your applications by using the methods of the [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) interface.</span></span>

<span data-ttu-id="602ea-127">Para leer los archivos que están protegidos por una licencia que especifica OPLs, debe comprobar el OPL para la acción deseada.</span><span class="sxs-lookup"><span data-stu-id="602ea-127">To read files that are protected by a license that specifies OPLs, you must check the OPL for the desired action.</span></span> <span data-ttu-id="602ea-128">La tecnología de salida que usa la aplicación debe ser permitida por el OPL de la licencia.</span><span class="sxs-lookup"><span data-stu-id="602ea-128">The output technology your application is using must be allowed by the OPL in the license.</span></span> <span data-ttu-id="602ea-129">Por ejemplo, algunas licencias de audio protegido pueden requerir que use la ruta de acceso de audio segura para reproducirla.</span><span class="sxs-lookup"><span data-stu-id="602ea-129">For example, some licenses for protected audio may require that you use secure audio path to play it.</span></span>

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a><span data-ttu-id="602ea-130">Configuración del lector para evaluar los niveles de protección de los resultados</span><span class="sxs-lookup"><span data-stu-id="602ea-130">Configuring the Reader to Evaluate Output Protection Levels</span></span>

<span data-ttu-id="602ea-131">Antes de poder comprobar OPLs para los archivos cargados en el lector, debe llamar al método [**IWMDRMReader2:: SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) , pasando **true** para el parámetro *fEvaluate* .</span><span class="sxs-lookup"><span data-stu-id="602ea-131">Before you can check OPLs for files loaded in the reader, you must call the [**IWMDRMReader2::SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) method, passing **TRUE** for the *fEvaluate* parameter.</span></span> <span data-ttu-id="602ea-132">Si no llama a este método, las licencias que requieren OPLs no son visibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="602ea-132">If you do not call this method, licenses that require OPLs are not visible to your application.</span></span>

## <a name="evaluating-copy-output-protection-levels"></a><span data-ttu-id="602ea-133">Evaluación de los niveles de protección de la salida de copia</span><span class="sxs-lookup"><span data-stu-id="602ea-133">Evaluating Copy Output Protection Levels</span></span>

<span data-ttu-id="602ea-134">Para obtener los niveles de protección de salida de la acción de copia, llame al método [**IWMDRMReader2:: GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) .</span><span class="sxs-lookup"><span data-stu-id="602ea-134">To get output protection levels for the copy action, call the [**IWMDRMReader2::GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) method.</span></span> <span data-ttu-id="602ea-135">Los datos que recibe de la llamada se almacenan en una estructura del [**\_ \_ OPL de copia de DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) .</span><span class="sxs-lookup"><span data-stu-id="602ea-135">The data you receive from the call is stored in a [**DRM\_COPY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) structure.</span></span> <span data-ttu-id="602ea-136">La estructura contiene un nivel de protección de salida base, que especifica el nivel de salida mínimo para la acción de copia en la licencia.</span><span class="sxs-lookup"><span data-stu-id="602ea-136">The structure contains a base output protection level, which specifies the minimum output level for the copy action in the license.</span></span> <span data-ttu-id="602ea-137">Sin embargo, la \_ estructura del OPL de copia \_ de DRM también contiene dos listas de identificadores de tecnología: una para las tecnologías permitidas que se clasifican en un OPL inferior al de la base, y otra para las tecnologías cuya clasificación es igual o superior al OPL base, pero que están restringidas por la licencia.</span><span class="sxs-lookup"><span data-stu-id="602ea-137">However, the DRM\_COPY\_OPL structure also contains two lists of technology identifiers: one for allowed technologies that are rated at a lower OPL than the base, and one for technologies that are rated equal to or higher than the base OPL but that are restricted by the license.</span></span> <span data-ttu-id="602ea-138">Debe comprobar las inclusiones y exclusiones para asegurarse de que la tecnología que está usando la aplicación está permitida por la licencia.</span><span class="sxs-lookup"><span data-stu-id="602ea-138">You must check the inclusions and exclusions to ensure that the technology your application is using is allowed by the license.</span></span>

## <a name="evaluating-play-output-protection-levels"></a><span data-ttu-id="602ea-139">Evaluación de los niveles de protección de la salida de reproducción</span><span class="sxs-lookup"><span data-stu-id="602ea-139">Evaluating Play Output Protection Levels</span></span>

<span data-ttu-id="602ea-140">Para obtener los niveles de protección de salida de la acción Play, llame al método [**IWMDRMReader2:: GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) .</span><span class="sxs-lookup"><span data-stu-id="602ea-140">To get output protection levels for the play action, call the [**IWMDRMReader2::GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) method.</span></span> <span data-ttu-id="602ea-141">Los datos que recibe de la llamada se almacenan en una estructura de receptor de [**\_ \_ reproducción DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) .</span><span class="sxs-lookup"><span data-stu-id="602ea-141">The data you receive from the call is stored in a [**DRM\_PLAY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) structure.</span></span> <span data-ttu-id="602ea-142">La estructura contiene otras estructuras.</span><span class="sxs-lookup"><span data-stu-id="602ea-142">The structure contains several other structures.</span></span> <span data-ttu-id="602ea-143">Los niveles de protección de salida base para la acción de reproducción se almacenan en una estructura de niveles de  [**\_ \_ \_ protección \_ de salida mínima de DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (el miembro minOPL de un **\_ \_ OPL de reproducción de DRM**), que define el valor de OPL mínimo necesario para reproducir contenido en diversos formatos.</span><span class="sxs-lookup"><span data-stu-id="602ea-143">The base output protection levels for the play action are stored in a [**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) structure (the **minOPL** member of **DRM\_PLAY\_OPL**), which defines the minimum OPL required to play content in a variety of formats.</span></span> <span data-ttu-id="602ea-144">Debe comprobar el miembro para el tipo de formato de salida que proporciona la aplicación.</span><span class="sxs-lookup"><span data-stu-id="602ea-144">You must check the member for the type of output formats that your application delivers.</span></span>

<span data-ttu-id="602ea-145">La estructura del **\_ \_ OPL de reproducción de DRM** define dos tipos de restricciones: el muestreo necesario y los identificadores de protección de salida de vídeo permitidos.</span><span class="sxs-lookup"><span data-stu-id="602ea-145">The **DRM\_PLAY\_OPL** structure defines two kinds of restrictions: required down-sampling and allowed video output protection identifiers.</span></span>

<span data-ttu-id="602ea-146">Required: el muestreo se define como una lista de identificadores de tecnología de salida (el miembro **oplIdDownsample** de **DRM Play de DRM \_ \_**) que, si se usa, puede recibir el contenido de la reproducción solo si el contenido se muestra por primera vez en una velocidad de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="602ea-146">Required down-sampling is defined as a list of output technology identifiers (the **oplIdDownsample** member of **DRM\_PLAY\_OPL**) that, if used, can receive the content for playback only if the content is first down-sampled to a lower bit rate.</span></span>

<span data-ttu-id="602ea-147">Los identificadores de protección de salida de vídeo permitidos se definen como una lista de tecnologías de salida de vídeo con información de configuración para cada uno.</span><span class="sxs-lookup"><span data-stu-id="602ea-147">Allowed video output protection identifiers are defined as a list of video output technologies with configuration information for each.</span></span>

## <a name="handling-multiple-licenses"></a><span data-ttu-id="602ea-148">Control de varias licencias</span><span class="sxs-lookup"><span data-stu-id="602ea-148">Handling Multiple Licenses</span></span>

<span data-ttu-id="602ea-149">Algunos archivos pueden tener varias licencias asociadas a ellos en el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="602ea-149">Some files may have multiple licenses associated with them in the local license store.</span></span> <span data-ttu-id="602ea-150">Al evaluar OPLs para un archivo que está leyendo, puede comprobar si hay más licencias llamando al método [**IWMDRMReader2:: TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) .</span><span class="sxs-lookup"><span data-stu-id="602ea-150">When you evaluate OPLs for a file that you are reading, you can check for additional licenses by calling the [**IWMDRMReader2::TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) method.</span></span> <span data-ttu-id="602ea-151">Debe seguir probando licencias hasta que encuentre una que permita la acción que desea realizar o hasta que TryNextLicense devuelva DRM \_ S \_ false, lo que indica que no hay más licencias.</span><span class="sxs-lookup"><span data-stu-id="602ea-151">You should continue trying licenses until you find one that allows the action you want to perform or until TryNextLicense returns DRM\_S\_FALSE, which indicates that there are no more licenses.</span></span>

<span data-ttu-id="602ea-152">En algunos casos, un archivo puede tener una licencia asociada que requiere un OPL que la aplicación no admite.</span><span class="sxs-lookup"><span data-stu-id="602ea-152">In some cases, a file might have an associated license that requires an OPL that your application cannot support.</span></span> <span data-ttu-id="602ea-153">En tal caso, es importante comprobar si hay licencias adicionales, ya que puede existir una licencia que no especifique OPLs.</span><span class="sxs-lookup"><span data-stu-id="602ea-153">In such a case it is important to check for additional licenses because a license may exist that does not specify OPLs.</span></span>

<span data-ttu-id="602ea-154">**Nota:** DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="602ea-154">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="602ea-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="602ea-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="602ea-156">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="602ea-156">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="602ea-157">**Interfaz IWMDRMReader2**</span><span class="sxs-lookup"><span data-stu-id="602ea-157">**IWMDRMReader2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




