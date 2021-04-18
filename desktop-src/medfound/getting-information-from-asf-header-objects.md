---
description: La información del encabezado ASF se almacena en los objetos de encabezado ASF de un archivo multimedia.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Obtener información de los objetos de encabezado ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25155929c9e3ba7e59ee1b5f46ea7c5930c3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714907"
---
# <a name="getting-information-from-asf-header-objects"></a><span data-ttu-id="d2c5c-103">Obtener información de los objetos de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="d2c5c-103">Getting Information from ASF Header Objects</span></span>

<span data-ttu-id="d2c5c-104">La información del encabezado ASF se almacena en los objetos de encabezado ASF de un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-104">ASF header information is stored in the ASF Header Objects of a media file.</span></span> <span data-ttu-id="d2c5c-105">Media Foundation proporciona el [objeto ContentInfo de ASF](asf-contentinfo-object.md) para trabajar con el objeto de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-105">Media Foundation provides the [ASF ContentInfo Object](asf-contentinfo-object.md) to work with the Header Object.</span></span> <span data-ttu-id="d2c5c-106">Se requiere un objeto ContentInfo rellenado para que la aplicación pueda leer la información de encabezado de un archivo existente.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-106">A populated ContentInfo object is required in order for the application to read header information of an existing file.</span></span> <span data-ttu-id="d2c5c-107">Esto se logra mediante una llamada a [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span><span class="sxs-lookup"><span data-stu-id="d2c5c-107">This is achieved by calling [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span> <span data-ttu-id="d2c5c-108">Si el análisis se completa correctamente, la biblioteca ASF del archivo, que se mantiene internamente mediante Media Foundation, se rellena con información de encabezado de varios objetos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-108">If parsing completes successfully, the ASF library for the file, which is maintained internally by Media Foundation, is populated with header information from various Header Objects.</span></span> <span data-ttu-id="d2c5c-109">Algunas de estas propiedades se exponen a la aplicación, que se puede recuperar a través de los atributos del descriptor de presentación, el descriptor de flujo, el perfil y las propiedades de metadatos.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-109">Some of these properties are exposed to the application, which it can retrieve through attributes on the presentation descriptor, stream descriptor, the profile, and metadata properties.</span></span>

<span data-ttu-id="d2c5c-110">Para obtener una lista completa de los atributos, consulte [atributos de Media Foundation para los objetos de encabezado ASF](media-foundation-attributes-for-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d2c5c-110">For the complete list of attributes, see [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a><span data-ttu-id="d2c5c-111">Recuperar información de encabezado de un descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="d2c5c-111">Retrieving Header Information from a Presentation Descriptor</span></span>

<span data-ttu-id="d2c5c-112">Un objeto de descriptor de presentación contiene la descripción de un origen multimedia determinado, en este caso el origen de medios ASF.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-112">A presentation descriptor object contains the description of a particular media source, in this case the ASF media source.</span></span> <span data-ttu-id="d2c5c-113">Si la llamada a **ParseHeader** se completa correctamente, la información de nivel de archivo del objeto de encabezado se almacena como atributos en el descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-113">If the **ParseHeader** call completes successfully, file-level information from the Header Object is stored as attributes on the presentation descriptor.</span></span> <span data-ttu-id="d2c5c-114">Para crear el descriptor de presentación, llame a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="d2c5c-114">To create the presentation descriptor, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="d2c5c-115">Este método devuelve un puntero a un objeto de descriptor de presentación rellenado que contiene estos atributos para el archivo ASF asociado al objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-115">This method returns a pointer to a populated presentation descriptor object that contains these attributes for the ASF file associated with the ContentInfo object.</span></span> <span data-ttu-id="d2c5c-116">Para obtener valores de atributos específicos, llame a los métodos **IMFAttributes:: GetXXX** en el descriptor de presentación y especifique el atributo **MF \_ PD \_ ASF \_ XXX** .</span><span class="sxs-lookup"><span data-stu-id="d2c5c-116">To get values for specific attributes, call **IMFAttributes::Getxxx** methods on the presentation descriptor and specify the **MF\_PD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="d2c5c-117">En el código de ejemplo siguiente se recupera la duración de la reproducción de un archivo ASF, especificado por un objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-117">The following example code retrieves the play duration of an ASF file, specified by a ContentInfo object.</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



<span data-ttu-id="d2c5c-118">Para obtener más información acerca de los descriptores de presentación en general, consulte [descriptores de presentación](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="d2c5c-118">For more information about presentation descriptors in general, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="d2c5c-119">Para obtener el conjunto completo de atributos de descriptor de presentación, vea [atributos de descriptor de presentación](presentation-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d2c5c-119">For the complete set of presentation descriptor attributes, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-a-stream-descriptor"></a><span data-ttu-id="d2c5c-120">Recuperar información de encabezado de un descriptor de flujo</span><span class="sxs-lookup"><span data-stu-id="d2c5c-120">Retrieving Header Information from a Stream Descriptor</span></span>

<span data-ttu-id="d2c5c-121">Un objeto de descriptor de flujo expone la interfaz [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) y describe las características de las secuencias del archivo.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-121">A stream descriptor object exposes the [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface and describes the characteristics of the streams in the file.</span></span> <span data-ttu-id="d2c5c-122">El descriptor de presentación del contenido ASF contiene uno o más descriptores de flujo que representan las secuencias enumeradas en el objeto de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-122">The presentation descriptor for the ASF content contains one or more stream descriptors that represent the streams listed in the Header Object.</span></span> <span data-ttu-id="d2c5c-123">Después de que la llamada a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) finalice correctamente, los descriptores de flujo subyacentes se rellenan con información de nivel de flujo de los distintos objetos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-123">After the call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) completes successfully, the underlying stream descriptors are populated with stream-level information from the various Header Objects.</span></span> <span data-ttu-id="d2c5c-124">Para obtener un descriptor de flujo para una secuencia ASF, llame a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) en el descriptor de presentación que se genera a partir del objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-124">To get a stream descriptor for an ASF stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) on the presentation descriptor that is generated from the ContentInfo object.</span></span>

<span data-ttu-id="d2c5c-125">Algunas de las propiedades de la secuencia se establecen como atributos en los descriptores de flujo.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-125">Some of the stream properties are set as attributes on stream descriptors.</span></span> <span data-ttu-id="d2c5c-126">Llame a los métodos **IMFAttributes:: GetXXX** en un descriptor de flujo y especifique el atributo **MF \_ SD \_ ASF \_ XXX** .</span><span class="sxs-lookup"><span data-stu-id="d2c5c-126">Call **IMFAttributes::Getxxx** methods on a stream descriptor and specify the **MF\_SD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="d2c5c-127">Para obtener el conjunto completo de atributos de descriptor de secuencia, vea los atributos "descriptor de secuencia específico de ASF" enumerados en [los atributos del descriptor de flujo](stream-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d2c5c-127">For the complete set of stream descriptor attributes, see "ASF-Specific Stream Descriptor" attributes listed in [Stream Descriptor Attributes](stream-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-the-profile-object"></a><span data-ttu-id="d2c5c-128">Recuperar información de encabezado del objeto de perfil</span><span class="sxs-lookup"><span data-stu-id="d2c5c-128">Retrieving Header Information from the Profile Object</span></span>

<span data-ttu-id="d2c5c-129">Además de los descriptores de secuencia, el objeto de perfil ASF también describe las propiedades de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-129">In addition to stream descriptors, the ASF profile object also describes the stream properties.</span></span> <span data-ttu-id="d2c5c-130">Para obtener el perfil de un archivo ASF existente, llame a [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="d2c5c-130">To get the profile of an existing ASF file, call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="d2c5c-131">El objeto de perfil ASF devuelto por este método no incluye ninguno de los atributos **MF \_ PD \_ ASF \_ XXX** .</span><span class="sxs-lookup"><span data-stu-id="d2c5c-131">The ASF profile object returned by this method does not include any of the **MF\_PD\_ASF\_xxx** attributes.</span></span> <span data-ttu-id="d2c5c-132">Estos atributos solo están disponibles para la aplicación después de llamar a [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) para generar el objeto de Perfil de un descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-132">These attributes are available to the application only after it calls [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) to generate the profile object from a presentation descriptor.</span></span> <span data-ttu-id="d2c5c-133">Puede usar el perfil para obtener punteros a los objetos de exclusión mutua y de priorización de flujo.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-133">You can use the profile to get pointers to the mutual exclusion and stream prioritization objects.</span></span>

<span data-ttu-id="d2c5c-134">Para obtener información sobre el objeto de perfil, vea [ASF Profile](asf-profile.md) .</span><span class="sxs-lookup"><span data-stu-id="d2c5c-134">For information about the profile object, see [ASF Profile](asf-profile.md) .</span></span>

## <a name="retrieving-metadata-from-header-objects"></a><span data-ttu-id="d2c5c-135">Recuperar metadatos de objetos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d2c5c-135">Retrieving Metadata from Header Objects</span></span>

<span data-ttu-id="d2c5c-136">Un archivo ASF puede contener varias propiedades de metadatos que se establecen durante la codificación del archivo.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-136">An ASF file can contain several metadata properties that are set during file encoding.</span></span> <span data-ttu-id="d2c5c-137">Una aplicación puede enumerar estas propiedades con el objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-137">An application can enumerate these properties with the ContentInfo object.</span></span> <span data-ttu-id="d2c5c-138">Algunas de estas propiedades, como la información de velocidad de bits variable (VBR), están disponibles para la aplicación a través de los atributos del descriptor de presentación, los descriptores de flujo y los tipos de medios para el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="d2c5c-138">Some of these properties, such as variable bit rate (VBR) information, are available to the application through attributes on presentation descriptor, stream descriptors, and media types for the media file.</span></span> <span data-ttu-id="d2c5c-139">Estos atributos se establecen en el objeto ContentInfo durante la inicialización a través de la llamada a [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="d2c5c-139">These attributes are set on the ContentInfo object during initialization through the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2c5c-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d2c5c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2c5c-141">Objeto ContentInfo de ASF</span><span class="sxs-lookup"><span data-stu-id="d2c5c-141">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> </dl>

 

 



