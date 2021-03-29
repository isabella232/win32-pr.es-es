---
title: Actualización de complementos de DSP existentes
description: Actualización de complementos de DSP existentes
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Complementos de Windows Media Player, procesamiento de señal digital (DSP)
- complementos, procesamiento de señal digital (DSP)
- Complementos de procesamiento de señal digital, actualizar
- Complementos DSP, actualizar
- versiones de Windows Media Player, Complementos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393cde356e0d86bb920825e731bb12ee0b7c2818
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788745"
---
# <a name="updating-existing-dsp-plug-ins"></a><span data-ttu-id="ccff0-108">Actualización de complementos de DSP existentes</span><span class="sxs-lookup"><span data-stu-id="ccff0-108">Updating Existing DSP Plug-ins</span></span>

<span data-ttu-id="ccff0-109">Los complementos DSP creados antes de la versión del SDK de Windows Media Player 11 podrían no funcionar según lo esperado con Windows Media Player 11 en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ccff0-109">DSP plug-ins created before the release of the Windows Media Player 11 SDK might not work as expected with Windows Media Player 11 running on Windows Vista.</span></span> <span data-ttu-id="ccff0-110">Para asegurarse de que los clientes que ejecutan Windows Media Player 11 en Windows Vista pueden usar los complementos, debe realizar algunos cambios en el código del complemento DSP, volver a compilar el proyecto y distribuir el complemento actualizado a sus clientes.</span><span class="sxs-lookup"><span data-stu-id="ccff0-110">To ensure that customers who run Windows Media Player 11 on Windows Vista can use your plug-ins, you must make some changes to your DSP plug-in code, recompile your project, and distribute the updated plug-in to your customers.</span></span>

<span data-ttu-id="ccff0-111">Los proyectos creados con la versión más reciente del Asistente para complementos de Windows Media Player contendrán las actualizaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="ccff0-111">Projects created using the latest version of the Windows Media Player plug-in wizard will contain the required updates.</span></span> <span data-ttu-id="ccff0-112">Vea [actualizaciones del Asistente para complementos de DSP para Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="ccff0-112">See [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span> <span data-ttu-id="ccff0-113">(Se recomienda ejecutar el Asistente para crear un nuevo proyecto de ejemplo y, a continuación, usar una herramienta como Windiff.exe, que se incluye con Visual Studio, para inspeccionar las diferencias entre el código de ejemplo y el código de producción).</span><span class="sxs-lookup"><span data-stu-id="ccff0-113">(It is a good idea to run the wizard to create a new sample project and then use a tool like Windiff.exe, which comes with Visual Studio, to inspect the differences between the sample code and your production code.)</span></span>

<span data-ttu-id="ccff0-114">Hay tres cambios principales que debe realizar en los complementos de DSP existentes:</span><span class="sxs-lookup"><span data-stu-id="ccff0-114">There are three main changes you will need to make to any existing DSP plug-ins:</span></span>

-   <span data-ttu-id="ccff0-115">Cambiar la manera en que se registra el complemento.</span><span class="sxs-lookup"><span data-stu-id="ccff0-115">Change the way the plug-in registers.</span></span> <span data-ttu-id="ccff0-116">El complemento existente probablemente registra el modelo de subprocesos como "Apartamento".</span><span class="sxs-lookup"><span data-stu-id="ccff0-116">Your existing plug-in probably registers the threading model as "Apartment".</span></span> <span data-ttu-id="ccff0-117">Windows Media Player 11, que se ejecuta en Windows Vista, requiere que los complementos de DSP registren el modelo de subprocesos como "ambos".</span><span class="sxs-lookup"><span data-stu-id="ccff0-117">Windows Media Player 11 running on Windows Vista requires that DSP plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="ccff0-118">Puede corregir esto cambiando el valor del modelo de subprocesos en el archivo *projectname*. RGS, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ccff0-118">You can fix this by changing the threading model value in your *projectname*.rgs file, as follows:</span></span>

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > <span data-ttu-id="ccff0-119">Al especificar el modelo de subprocesos como "ambos", se quita cualquier serialización que COM proporcione para las llamadas a interfaces personalizadas.</span><span class="sxs-lookup"><span data-stu-id="ccff0-119">Specifying the threading model as "Both" removes any serialization that COM provides for calls to custom interfaces.</span></span> <span data-ttu-id="ccff0-120">Si realiza llamadas a las interfaces personalizadas desde varios subprocesos, debe proporcionar esta serialización usted mismo.</span><span class="sxs-lookup"><span data-stu-id="ccff0-120">If you make calls to your custom interfaces from multiple threads, you must provide this serialization yourself.</span></span>

     

    <span data-ttu-id="ccff0-121">Windows Media Player 11 garantiza que las llamadas a las interfaces de DMO se serializan correctamente.</span><span class="sxs-lookup"><span data-stu-id="ccff0-121">Windows Media Player 11 ensures that calls to DMO interfaces are properly serialized.</span></span>

    1.  <span data-ttu-id="ccff0-122">Agregue llamadas a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) y [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuevo tipo de complemento: wmp \_ PLUGINTYPE \_ DSP \_ OUTOFPROC en DllRegisterServer y DllUnregisterServer en el archivo *projectnamedll*. cpp.</span><span class="sxs-lookup"><span data-stu-id="ccff0-122">Add calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC in DllRegisterServer and DllUnregisterServer in your *projectnamedll*.cpp file.</span></span> <span data-ttu-id="ccff0-123">Para obtener más información, consulte las páginas de referencia de estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ccff0-123">See the reference pages for these methods for details.</span></span>
    2.  <span data-ttu-id="ccff0-124">Cree y distribuya un archivo DLL de proxy/stub para habilitar el cálculo de referencias COM de cualquier interfaz personalizada implementada o creada por la clase de complemento.</span><span class="sxs-lookup"><span data-stu-id="ccff0-124">Create and distribute a proxy/stub DLL to enable COM marshaling of any custom interface implemented on or created by the plug-in class.</span></span> <span data-ttu-id="ccff0-125">Una interfaz personalizada es cualquier interfaz propietaria que defina e implemente para que la use el objeto de complemento.</span><span class="sxs-lookup"><span data-stu-id="ccff0-125">A custom interface is any proprietary interface that you define and implement for use by the plug-in object.</span></span> <span data-ttu-id="ccff0-126">Esto incluye la interfaz personalizada usada por la página de propiedades, si proporcionó una, pero también puede incluir interfaces que se conectan a complementos de la interfaz de usuario, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ccff0-126">This includes the custom interface used by your property page, if you provided one, but might also include interfaces that connect to UI plug-ins, for example.</span></span> <span data-ttu-id="ccff0-127">Un ejemplo de una interfaz personalizada creada por el Asistente para complementos es *Iprojectname*.</span><span class="sxs-lookup"><span data-stu-id="ccff0-127">An example of a custom interface created by the plug-in wizard is *Iprojectname*.</span></span> <span data-ttu-id="ccff0-128">Entre los ejemplos de interfaces que no son interfaces personalizadas se incluyen **IMediaObject** y **IWMPPluginEnable**.</span><span class="sxs-lookup"><span data-stu-id="ccff0-128">Examples of interfaces that are not custom interfaces include **IMediaObject** and **IWMPPluginEnable**.</span></span>

<span data-ttu-id="ccff0-129">Si el complemento de DSP procesa audio, también debe agregar compatibilidad con los siguientes formatos de audio nuevos:</span><span class="sxs-lookup"><span data-stu-id="ccff0-129">If your DSP plug-in processes audio, you must also add support for the following new audio formats:</span></span>

-   <span data-ttu-id="ccff0-130">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="ccff0-130">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
-   <span data-ttu-id="ccff0-131">\_Formato \_ de onda extensible con SUBformato KSDATAFORMAT \_ SubType \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="ccff0-131">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

<span data-ttu-id="ccff0-132">Si el complemento de DSP procesa vídeo, debe agregar compatibilidad con el formato de vídeo NV12.</span><span class="sxs-lookup"><span data-stu-id="ccff0-132">If your DSP plug-in processes video, you must add support for the NV12 video format.</span></span>

<span data-ttu-id="ccff0-133">Vea el complemento DSP de audio o vídeo de ejemplo que crea el Asistente para obtener un ejemplo de cómo procesar estos tipos de formato.</span><span class="sxs-lookup"><span data-stu-id="ccff0-133">See the sample audio or video DSP plug-in that the wizard creates for an example of how to process these format types.</span></span>

## <a name="about-the-proxystub-project"></a><span data-ttu-id="ccff0-134">Acerca del proyecto de proxy o código auxiliar</span><span class="sxs-lookup"><span data-stu-id="ccff0-134">About the Proxy/Stub Project</span></span>

<span data-ttu-id="ccff0-135">Quizás la manera más sencilla de crear un proyecto DLL de proxy/stub para el complemento de DSP es ejecutar el Asistente para complementos de DSP.</span><span class="sxs-lookup"><span data-stu-id="ccff0-135">Perhaps the simplest way to create a proxy/stub DLL project for your DSP plug-in is to run the DSP plug-in wizard.</span></span> <span data-ttu-id="ccff0-136">Se creará un proyecto de proxy/código auxiliar de ejemplo que puede modificar para que funcione con el código existente.</span><span class="sxs-lookup"><span data-stu-id="ccff0-136">This will create a sample proxy/stub project that you can modify to work with your existing code.</span></span> <span data-ttu-id="ccff0-137">Tendrá que realizar los cambios siguientes:</span><span class="sxs-lookup"><span data-stu-id="ccff0-137">You will need to make the following changes:</span></span>

1.  <span data-ttu-id="ccff0-138">Quite todas las definiciones existentes de las interfaces personalizadas del código.</span><span class="sxs-lookup"><span data-stu-id="ccff0-138">Remove any existing definitions for your custom interfaces from your code.</span></span> <span data-ttu-id="ccff0-139">Por ejemplo, el Asistente para complementos de DSP del SDK de Windows Media Player 10 creó la definición de la interfaz *Iprojectname* en el archivo *projectname*. h mediante la palabra clave **interface** .</span><span class="sxs-lookup"><span data-stu-id="ccff0-139">For example, the DSP plug-in wizard from the Windows Media Player 10 SDK created the *Iprojectname* interface definition in the *projectname*.h file by using the **interface** keyword.</span></span>
2.  <span data-ttu-id="ccff0-140">Defina las interfaces personalizadas en el archivo IDL del proyecto de proxy o código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="ccff0-140">Define your custom interfaces in the proxy/stub project's IDL file.</span></span>
3.  <span data-ttu-id="ccff0-141">Compile el proyecto de proxy o código auxiliar antes del proyecto principal.</span><span class="sxs-lookup"><span data-stu-id="ccff0-141">Build the proxy/stub project before your main project.</span></span> <span data-ttu-id="ccff0-142">Puede configurar Visual Studio para que lo haga automáticamente si ambos proyectos forman parte de la misma solución.</span><span class="sxs-lookup"><span data-stu-id="ccff0-142">You can configure Visual Studio to do this automatically if both projects are part of the same solution.</span></span>
4.  <span data-ttu-id="ccff0-143">El compilador MIDL creará un nuevo archivo de encabezado con un nombre con el formato *projectname* \_ h.h.</span><span class="sxs-lookup"><span data-stu-id="ccff0-143">The MIDL compiler will create a new header file having a name in the format *projectname*\_h.h.</span></span> <span data-ttu-id="ccff0-144">Debe incluir este encabezado en el proyecto principal (en *projectname*. h).</span><span class="sxs-lookup"><span data-stu-id="ccff0-144">You must include this header in your main project (in *projectname*.h).</span></span> <span data-ttu-id="ccff0-145">Contiene las definiciones de las interfaces personalizadas.</span><span class="sxs-lookup"><span data-stu-id="ccff0-145">It contains the definitions for your custom interfaces.</span></span>

## <a name="distributing-the-updated-plug-in"></a><span data-ttu-id="ccff0-146">Distribuir el complemento actualizado</span><span class="sxs-lookup"><span data-stu-id="ccff0-146">Distributing the Updated Plug-in</span></span>

<span data-ttu-id="ccff0-147">Puede instalar el complemento actualizado en los equipos de los usuarios exactamente como tenía en el pasado.</span><span class="sxs-lookup"><span data-stu-id="ccff0-147">You can install the updated plug-in on your users' computers exactly as you have in the past.</span></span> <span data-ttu-id="ccff0-148">Sin embargo, ahora debe distribuir y registrar también el archivo DLL de proxy/código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="ccff0-148">However, you must now also distribute and register the proxy/stub DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccff0-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ccff0-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccff0-150">**Introducción al desarrollador de complementos de DSP**</span><span class="sxs-lookup"><span data-stu-id="ccff0-150">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




