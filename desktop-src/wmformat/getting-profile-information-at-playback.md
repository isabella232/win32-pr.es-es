---
title: Obtención de información de perfil en la reproducción
description: Obtención de información de perfil en la reproducción
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Media Format SDK, perfiles
- Advanced Systems Format (ASF), perfiles
- ASF (formato de sistemas avanzados), perfiles
- Advanced Systems Format (ASF), exclusión mutua
- ASF (formato de sistemas avanzados), exclusión mutua
- Advanced Systems Format (ASF), uso compartido de ancho de banda
- ASF (formato de sistemas avanzados), uso compartido de ancho de banda
- flujos, obtener información de perfil en la reproducción
- perfiles, obtener información en la reproducción
- exclusión mutua, obtención de información de perfil en la reproducción
- uso compartido de ancho de banda, obtención de información de perfil en la reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5c7083f7bf9e986e8a23ba2c78dfe4404942a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149092"
---
# <a name="getting-profile-information-at-playback"></a><span data-ttu-id="24043-114">Obtención de información de perfil en la reproducción</span><span class="sxs-lookup"><span data-stu-id="24043-114">Getting Profile Information at Playback</span></span>

<span data-ttu-id="24043-115">La información del perfil que se usa para crear un archivo se almacena en la sección de encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="24043-115">Information from the profile used to create a file is stored in the header section of the file.</span></span> <span data-ttu-id="24043-116">Ambos objetos de lector pueden tener acceso a la información de perfil del encabezado de archivo.</span><span class="sxs-lookup"><span data-stu-id="24043-116">Both reader objects can access the profile information from the file header.</span></span> <span data-ttu-id="24043-117">Hay varias razones por las que puede que desee tener acceso a los datos de perfil desde el lector.</span><span class="sxs-lookup"><span data-stu-id="24043-117">There are several reasons why you might want to access profile data from the reader.</span></span> <span data-ttu-id="24043-118">Normalmente, tendrá que recuperar información sobre las secuencias, los objetos de exclusión mutua y los objetos de uso compartido de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="24043-118">Most commonly, you will need to retrieve information about streams, mutual exclusion objects, and bandwidth sharing objects.</span></span>

<span data-ttu-id="24043-119">Tanto el objeto lector asincrónico como el objeto lector sincrónico se pueden consultar para la interfaz [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="24043-119">Both the asynchronous reader object and the synchronous reader object can be queried for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="24043-120">Ningún cambio realizado en la información del perfil puede afectar al archivo en el lector.</span><span class="sxs-lookup"><span data-stu-id="24043-120">No changes made to the profile information can have any affect on the file in the reader.</span></span> <span data-ttu-id="24043-121">Para obtener más información sobre el acceso a la información de perfil, consulte [trabajar con perfiles](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="24043-121">For more information about accessing profile information, see [Working with Profiles](working-with-profiles.md).</span></span>

## <a name="stream-information"></a><span data-ttu-id="24043-122">Información de secuencia</span><span class="sxs-lookup"><span data-stu-id="24043-122">Stream Information</span></span>

<span data-ttu-id="24043-123">A veces es importante saber cómo se configura un flujo.</span><span class="sxs-lookup"><span data-stu-id="24043-123">It is sometimes important to know how a stream is configured.</span></span> <span data-ttu-id="24043-124">Cuando se recuperan las propiedades de los medios de cualquiera de los objetos de lector, se obtienen las propiedades de las salidas.</span><span class="sxs-lookup"><span data-stu-id="24043-124">When you retrieve media properties from the either of the reader objects, you get the properties of the outputs.</span></span> <span data-ttu-id="24043-125">Las propiedades de salida describen cómo el lector va a entregar los datos sin comprimir de una secuencia, no cómo se configura el flujo en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="24043-125">Output properties describe how the uncompressed data from a stream is going to be delivered by the reader, not how the stream is configured within the ASF file.</span></span>

<span data-ttu-id="24043-126">Al recibir ejemplos de secuencias sin comprimir de cualquier objeto lector, debe usar la información del perfil para identificar el formato de los datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="24043-126">When receiving uncompressed stream samples from either reader object, you must use the profile information to identify the format of the compressed data.</span></span> <span data-ttu-id="24043-127">Esto es especialmente importante si va a escribir la secuencia comprimida en otro archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="24043-127">This is particularly important if you are going to write the compressed stream to another ASF file.</span></span>

<span data-ttu-id="24043-128">También debe tener acceso a la información de la secuencia al utilizar la recompresión inteligente para transcodificar una secuencia de audio a una velocidad de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="24043-128">You also need to access stream information when using smart recompression to transcode an audio stream to a lower bit rate.</span></span>

<span data-ttu-id="24043-129">Puede que desee determinar si una secuencia se escribió con codificación de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="24043-129">You may want to determine whether a stream was written using variable bit rate (VBR) encoding.</span></span> <span data-ttu-id="24043-130">No se puede tener acceso a ninguna información de VBR de la interfaz **IWMProfile** de cualquier objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="24043-130">You cannot access any VBR information from the **IWMProfile** interface of either reader object.</span></span> <span data-ttu-id="24043-131">Esto se debe a que la información de VBR no se almacena en el archivo después de la codificación.</span><span class="sxs-lookup"><span data-stu-id="24043-131">This is because the VBR information is not stored in the file after encoding.</span></span> <span data-ttu-id="24043-132">Puede determinar si se ha creado una secuencia mediante la codificación VBR obteniendo un puntero a la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) del objeto lector y llamando a [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="24043-132">You can determine whether a stream was created using VBR encoding by obtaining a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface of the reader object and calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span> <span data-ttu-id="24043-133">Debe especificar el número de secuencia y pasar g \_ wszIsVBR como el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="24043-133">You must specify the stream number and pass g\_wszIsVBR as the attribute name.</span></span>

## <a name="mutual-exclusion-information"></a><span data-ttu-id="24043-134">Información de exclusión mutua</span><span class="sxs-lookup"><span data-stu-id="24043-134">Mutual Exclusion Information</span></span>

<span data-ttu-id="24043-135">Si desea crear una aplicación de lectura que use la exclusión mutua, querrá tener acceso a la información sobre los objetos de exclusión mutua incluidos en el perfil.</span><span class="sxs-lookup"><span data-stu-id="24043-135">If you want to create a reading application that uses mutual exclusion, you will want to access the information about any mutual exclusion objects included in the profile.</span></span> <span data-ttu-id="24043-136">Para todos los tipos de exclusión mutua excepto la velocidad de bits, la aplicación de lectura es responsable de cualquier cambio de flujo necesario.</span><span class="sxs-lookup"><span data-stu-id="24043-136">For all mutual exclusion types except bit rate, the reading application is responsible for any stream switching that is required.</span></span> <span data-ttu-id="24043-137">Para cambiar de flujo, debe saber qué secuencias son.</span><span class="sxs-lookup"><span data-stu-id="24043-137">To switch streams, you need to know which streams are which.</span></span>

## <a name="bandwidth-sharing-information"></a><span data-ttu-id="24043-138">Información de uso compartido de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="24043-138">Bandwidth Sharing Information</span></span>

<span data-ttu-id="24043-139">Los objetos de uso compartido de ancho de banda que se incluyen en un perfil solo se incluyen con fines informativos.</span><span class="sxs-lookup"><span data-stu-id="24043-139">Bandwidth sharing objects that are included in a profile are included only for informational purposes.</span></span> <span data-ttu-id="24043-140">Ni el objeto de escritor ni ninguno de los objetos de lector toman ninguna acción como resultado de los datos de uso compartido de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="24043-140">Neither the writer object nor either of the reader objects takes any action as a result of bandwidth sharing data.</span></span> <span data-ttu-id="24043-141">Si desea utilizar el uso compartido de ancho de banda en la aplicación de lectura, debe tener acceso a la información de uso compartido de ancho de banda de los datos del perfil.</span><span class="sxs-lookup"><span data-stu-id="24043-141">If you want to use bandwidth sharing in your reading application, you must access the bandwidth sharing information from the profile data.</span></span>

> [!Note]  
> <span data-ttu-id="24043-142">No toda la información del perfil que se usa para crear un archivo está presente en el encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="24043-142">Not all of the information from the profile used to create a file is present in the file header.</span></span> <span data-ttu-id="24043-143">Como norma general, los datos que se usan solo en el momento de la codificación no se conservan en el archivo.</span><span class="sxs-lookup"><span data-stu-id="24043-143">As a general rule, data that is used only at the time of encoding is not persisted in the file.</span></span> <span data-ttu-id="24043-144">Esto incluye los valores de entrada que se establecieron mediante el método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) , así como las propiedades establecidas con el método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="24043-144">This includes input settings that were set using the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method, as well as properties set using the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="24043-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24043-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24043-146">**Interfaz IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="24043-146">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="24043-147">**Leer archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="24043-147">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




