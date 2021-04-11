---
title: Trabajar con plantillas de cumplimiento de dispositivos
description: Trabajar con plantillas de cumplimiento de dispositivos
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- perfiles, plantillas de conformidad de dispositivos
- perfiles, plantillas de cumplimiento
- códecs, plantillas de conformidad de dispositivos
- códecs, plantillas de conformidad
- plantillas de conformidad de dispositivos, acerca de
- plantillas de conformidad
- plantillas, plantillas de conformidad de dispositivos
- Advanced Systems Format (ASF), plantillas de conformidad de dispositivos
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149078"
---
# <a name="working-with-device-conformance-templates"></a><span data-ttu-id="15188-112">Trabajar con plantillas de cumplimiento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="15188-112">Working with Device Conformance Templates</span></span>

<span data-ttu-id="15188-113">Debido a la gran flexibilidad de los archivos ASF, a menudo es difícil determinar si un archivo es adecuado para la reproducción en un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="15188-113">Because of the great flexibility of ASF files, it is often difficult to determine whether a file is appropriate for playback on a specific device.</span></span> <span data-ttu-id="15188-114">Por ejemplo, los archivos escritos para la reproducción local en equipos de escritorio no son óptimos para su uso en dispositivos de mano.</span><span class="sxs-lookup"><span data-stu-id="15188-114">For example, files written for local playback on desktop computers are not optimal for use on handheld devices.</span></span> <span data-ttu-id="15188-115">Las plantillas de conformidad de dispositivos permiten a las aplicaciones identificar rápidamente el tipo de dispositivo de reproducción para el que se diseñó un archivo.</span><span class="sxs-lookup"><span data-stu-id="15188-115">Device conformance templates enable applications to quickly identify the type of playback device for which a file was intended.</span></span> <span data-ttu-id="15188-116">Si la plantilla de conformidad del dispositivo no coincide con el dispositivo, la aplicación puede informar al usuario de que el archivo no es apropiado para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15188-116">If the device conformance template does not match the device, the application can inform the user that the file is inappropriate for the device.</span></span> <span data-ttu-id="15188-117">De esta manera, el usuario puede estar seguro de una mejor experiencia de reproducción.</span><span class="sxs-lookup"><span data-stu-id="15188-117">In this way, the user can be assured of a better playback experience.</span></span>

<span data-ttu-id="15188-118">Si está escribiendo archivos exclusivamente para su uso en equipos personales, las plantillas de conformidad de dispositivos no serán la gran parte de un factor en la creación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="15188-118">If you are writing files exclusively for use on personal computers, device conformance templates will not be as much of a factor in creating profiles.</span></span> <span data-ttu-id="15188-119">El propósito principal de estas plantillas es asegurarse de que los archivos creados para su uso con hardware especial son compatibles con una amplia gama de dispositivos y no solo un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15188-119">The main purpose of these templates is to ensure that files created for use with special hardware are compatible with a whole range of devices and not just a single device.</span></span>

<span data-ttu-id="15188-120">Una plantilla de conformidad de dispositivos es una aserción de que un archivo ASF contiene datos codificados en determinados parámetros.</span><span class="sxs-lookup"><span data-stu-id="15188-120">A device conformance template is an assertion that an ASF file contains data encoded within certain parameters.</span></span> <span data-ttu-id="15188-121">Para obtener más información sobre la configuración adecuada para las plantillas individuales, consulte parámetros de la [plantilla de cumplimiento de dispositivos](device-conformance-template-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="15188-121">For more information about the settings appropriate to the individual templates, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="15188-122">Los códecs siguientes son compatibles con las plantillas de conformidad de dispositivos:</span><span class="sxs-lookup"><span data-stu-id="15188-122">The following codecs support device conformance templates:</span></span>

-   <span data-ttu-id="15188-123">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="15188-123">Windows Media Video 9</span></span>
-   <span data-ttu-id="15188-124">Windows Media Audio 9 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="15188-124">Windows Media Audio 9 and later</span></span>
-   <span data-ttu-id="15188-125">Windows Media Audio 9 Professional y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="15188-125">Windows Media Audio 9 Professional and later</span></span>
-   <span data-ttu-id="15188-126">Windows Media Audio 9 Voice</span><span class="sxs-lookup"><span data-stu-id="15188-126">Windows Media Audio 9 Voice</span></span>

<span data-ttu-id="15188-127">No es necesario realizar ningún paso especial para usar las plantillas de cumplimiento de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="15188-127">You do not need to take any special steps to use device conformance templates.</span></span> <span data-ttu-id="15188-128">El códec escribe automáticamente una cadena de plantilla para cada secuencia adecuada en el archivo.</span><span class="sxs-lookup"><span data-stu-id="15188-128">The codec automatically writes a template string for each appropriate stream in the file.</span></span> <span data-ttu-id="15188-129">El códec decidirá qué plantilla se debe usar, en función de los valores de configuración de la secuencia en el perfil.</span><span class="sxs-lookup"><span data-stu-id="15188-129">The codec will decide which template to use, based on the stream configuration settings in the profile.</span></span> <span data-ttu-id="15188-130">Hay cierta superposición en los parámetros de la plantilla de conformidad del dispositivo, por lo que puede que desee solicitar una plantilla específica en lugar de permitir que el códec le asigne una.</span><span class="sxs-lookup"><span data-stu-id="15188-130">There is some overlap in device conformance template parameters, so you may want to request a specific template instead of letting the codec assign one for you.</span></span> <span data-ttu-id="15188-131">Puede especificar la plantilla que desee estableciendo la \_ propiedad g wszDecoderComplexityRequested con los métodos de la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de secuencia adecuado.</span><span class="sxs-lookup"><span data-stu-id="15188-131">You can specify which template you want by setting the g\_wszDecoderComplexityRequested property with the methods of the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the appropriate stream configuration object.</span></span>

<span data-ttu-id="15188-132">Cuando se escribe un archivo ASF, la plantilla de conformidad del dispositivo real para cada flujo se establece en el valor pasado al escritor por el códec.</span><span class="sxs-lookup"><span data-stu-id="15188-132">When an ASF file is written, the actual device conformance template for each stream is set to the value passed to the writer by the codec.</span></span> <span data-ttu-id="15188-133">Al abrir un archivo para leerlo, puede averiguar a qué plantilla se ajustan las secuencias del archivo mediante el uso de los métodos de la interfaz [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) para recuperar el \_ atributo de nivel de secuencia g wszDeviceConformanceTemplate.</span><span class="sxs-lookup"><span data-stu-id="15188-133">When opening a file for reading, you can find out which template the streams of the file conform to by using the methods of the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface to retrieve the g\_wszDeviceConformanceTemplate stream-level attribute.</span></span> <span data-ttu-id="15188-134">Para obtener más información sobre los atributos, vea [trabajar con metadatos](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="15188-134">For more information about attributes, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="15188-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="15188-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15188-136">**Diseñar perfiles**</span><span class="sxs-lookup"><span data-stu-id="15188-136">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="15188-137">**Parámetros de plantilla de conformidad de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="15188-137">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> </dl>

 

 




