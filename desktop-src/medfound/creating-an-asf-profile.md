---
description: En este tema se describe cómo crear como perfil ASF en Microsoft Media Foundation.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Creación de un perfil ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ed9553811645b8589de7fb1805f1a307c4bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686470"
---
# <a name="creating-an-asf-profile"></a><span data-ttu-id="acac6-103">Creación de un perfil ASF</span><span class="sxs-lookup"><span data-stu-id="acac6-103">Creating an ASF Profile</span></span>

<span data-ttu-id="acac6-104">En este tema se describe cómo crear como perfil ASF en Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="acac6-104">This topic describes how to create as ASF profile in Microsoft Media Foundation.</span></span>

-   [<span data-ttu-id="acac6-105">Crear un nuevo perfil</span><span class="sxs-lookup"><span data-stu-id="acac6-105">Create a New Profile</span></span>](#create-a-new-profile)
-   [<span data-ttu-id="acac6-106">Obtener el perfil del objeto ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="acac6-106">Get the Profile from the ASF ContentInfo Object</span></span>](#get-the-profile-from-the-asf-contentinfo-object)
-   [<span data-ttu-id="acac6-107">Obtener el perfil de un descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="acac6-107">Get the Profile from a Presentation Descriptor</span></span>](#get-the-profile-from-a-presentation-descriptor)
-   [<span data-ttu-id="acac6-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acac6-108">Related topics</span></span>](#related-topics)

## <a name="create-a-new-profile"></a><span data-ttu-id="acac6-109">Crear un nuevo perfil</span><span class="sxs-lookup"><span data-stu-id="acac6-109">Create a New Profile</span></span>

<span data-ttu-id="acac6-110">Para crear un perfil ASF vacío, llame a la función [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="acac6-110">To create an empty ASF profile, call the [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) function.</span></span> <span data-ttu-id="acac6-111">Esta función devuelve un puntero a la interfaz [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="acac6-111">This function returns a pointer to the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="acac6-112">La aplicación puede utilizar esta interfaz para agregar secuencias al perfil y para configurar cada una de las secuencias.</span><span class="sxs-lookup"><span data-stu-id="acac6-112">The application can use this interface to add streams to the profile, and to configure each of the streams.</span></span> <span data-ttu-id="acac6-113">Para obtener más información, vea [crear y configurar secuencias ASF](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="acac6-113">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>

<span data-ttu-id="acac6-114">Opcionalmente, la aplicación puede agregar objetos de exclusión mutua a dos o más secuencias.</span><span class="sxs-lookup"><span data-stu-id="acac6-114">Optionally, the application can add mutual-exclusion objects to two or more streams.</span></span> <span data-ttu-id="acac6-115">Consulte [uso de la exclusión mutua para secuencias ASF](using-mutual-exclusion-for-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="acac6-115">See [Using Mutual Exclusion for ASF Streams](using-mutual-exclusion-for-asf-streams.md).</span></span>

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a><span data-ttu-id="acac6-116">Obtener el perfil del objeto ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="acac6-116">Get the Profile from the ASF ContentInfo Object</span></span>

<span data-ttu-id="acac6-117">Una aplicación puede obtener el perfil ASF de un archivo ASF existente del [objeto ASF ContentInfo](asf-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="acac6-117">An application can get the ASF profile of an existing ASF file from the [ASF ContentInfo Object](asf-contentinfo-object.md).</span></span> <span data-ttu-id="acac6-118">El perfil ya está configurado y contiene la configuración de todas las secuencias del archivo.</span><span class="sxs-lookup"><span data-stu-id="acac6-118">The profile is already configured and contains settings for the all of the streams in the file.</span></span>

<span data-ttu-id="acac6-119">Inicialice el objeto ContentInfo analizando el objeto de encabezado ASF del archivo.</span><span class="sxs-lookup"><span data-stu-id="acac6-119">Initialize the ContentInfo object by parsing the ASF Header Object of the file.</span></span> <span data-ttu-id="acac6-120">Esto se realiza a través del método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="acac6-120">This is done through the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="acac6-121">Una vez que se han leído todos los objetos de encabezado y se ha rellenado la biblioteca ASF, se genera el perfil de este archivo.</span><span class="sxs-lookup"><span data-stu-id="acac6-121">After all the Header Objects are read and the ASF library is populated, the profile for this file is generated.</span></span> <span data-ttu-id="acac6-122">La aplicación puede obtener un puntero a este perfil inicializado mediante una llamada a [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="acac6-122">The application can get a pointer to this initialized profile by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>

## <a name="get-the-profile-from-a-presentation-descriptor"></a><span data-ttu-id="acac6-123">Obtener el perfil de un descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="acac6-123">Get the Profile from a Presentation Descriptor</span></span>

<span data-ttu-id="acac6-124">Puede obtener el objeto de Perfil de un archivo ASF existente del [descriptor de presentación](presentation-descriptors.md) del archivo o del objeto [ContentInfo ASF](asf-contentinfo-object.md) .</span><span class="sxs-lookup"><span data-stu-id="acac6-124">You can get the profile object of an existing ASF file from the [presentation descriptor](presentation-descriptors.md) for the file, or from the [ASF ContentInfo](asf-contentinfo-object.md) object.</span></span> <span data-ttu-id="acac6-125">En este caso, el perfil ya está configurado y contiene la configuración de todas las secuencias del archivo.</span><span class="sxs-lookup"><span data-stu-id="acac6-125">In this case, the profile is already configured and contains settings for all of the streams in the file.</span></span> <span data-ttu-id="acac6-126">Esto puede ser útil si desea modificar un perfil ASF existente.</span><span class="sxs-lookup"><span data-stu-id="acac6-126">This can be useful if you want to modify an existing ASF profile.</span></span> <span data-ttu-id="acac6-127">Por ejemplo, puede que desee volver a codificar un archivo Windows Media Video a una velocidad de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="acac6-127">For example, you might wish to re-encode a Windows Media Video file at a lower bit rate.</span></span>

<span data-ttu-id="acac6-128">Para obtener el perfil del descriptor de presentación, llame a [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="acac6-128">To get the profile from the presentation descriptor, call [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span></span> <span data-ttu-id="acac6-129">Esta función analiza el descriptor de presentación y rellena un perfil ASF con información sobre el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="acac6-129">This function parses the presentation descriptor, and populates an ASF profile with information about the media file.</span></span> <span data-ttu-id="acac6-130">La función devuelve un puntero a la interfaz IMFASFProfile.</span><span class="sxs-lookup"><span data-stu-id="acac6-130">The function returns a pointer to the IMFASFProfile interface.</span></span> <span data-ttu-id="acac6-131">Después, puede usar esta interfaz para modificar el perfil.</span><span class="sxs-lookup"><span data-stu-id="acac6-131">You can then use this interface to modify the profile.</span></span>

<span data-ttu-id="acac6-132">Para obtener el descriptor de la presentación, llame a uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="acac6-132">To get the presentation descriptor, call one of the following methods:</span></span>

-   <span data-ttu-id="acac6-133">En el origen de medios ASF, llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="acac6-133">From the ASF media source, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="acac6-134">En el objeto [ASF ContentInfo](asf-contentinfo-object.md) , llame a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="acac6-134">From the [ASF ContentInfo](asf-contentinfo-object.md) object, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="acac6-135">Antes de llamar a este método, asegúrese de que el objeto ContentInfo se inicializa para lectura.</span><span class="sxs-lookup"><span data-stu-id="acac6-135">Prior to calling this method, make sure that the ContentInfo object is initialized for reading.</span></span> <span data-ttu-id="acac6-136">Para obtener más información, vea "inicializar el objeto ContentInfo desde un archivo ASF existente" en [leer el objeto de encabezado ASF de un archivo existente](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="acac6-136">For more information, see "Initializing the ContentInfo Object from an Existing ASF File" in [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span> <span data-ttu-id="acac6-137">Sin embargo, si ya tiene un objeto ContentInfo inicializado, puede obtener el perfil directamente de él.</span><span class="sxs-lookup"><span data-stu-id="acac6-137">However, if you already have an initialized ContentInfo object, you can get the profile directly from it.</span></span> <span data-ttu-id="acac6-138">Esto se describe en "obtener el perfil del objeto ContentInfo" más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="acac6-138">This is described in "Getting the Profile from the ContentInfo Object " later in this topic.</span></span>

<span data-ttu-id="acac6-139">En el ejemplo siguiente se muestra cómo crear un perfil a partir de un descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="acac6-139">The following example shows how to create a profile from a presentation descriptor.</span></span> <span data-ttu-id="acac6-140">La función crea un origen multimedia para el archivo, obtiene el descriptor de presentación del origen multimedia y crea un perfil.</span><span class="sxs-lookup"><span data-stu-id="acac6-140">The function creates a media source for the file, gets the presentation descriptor from the media source, and creates a profile.</span></span> <span data-ttu-id="acac6-141">En este ejemplo se da por supuesto que *pszFileName* especifica la dirección URL de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="acac6-141">This example assumes that *pszFileName* specifies the URL of an ASF file.</span></span>


```C++
HRESULT GetASFProfile(PCWSTR pszFileName, IMFASFProfile** ppProfile)
{
    *ppProfile = NULL;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSourceUnk = NULL;
    IMFMediaSource* pSource = NULL;
    IMFPresentationDescriptor* pPD = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        hr = pResolver->CreateObjectFromURL(
                pszFileName,
                MF_RESOLUTION_MEDIASOURCE, 
                NULL,                      
                &ObjectType,               
                &pSourceUnk   
            );
    }

    // Get the IMFMediaSource interface from the media source.
    if (SUCCEEDED(hr))
    {
        hr = pSourceUnk->QueryInterface(IID_PPV_ARGS(&pSource));
    }

    // Get the presentation desccriptor.
    if (SUCCEEDED(hr))
    {
        hr = pSource->CreatePresentationDescriptor(&pPD);
    }

    // Get the profile from the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFProfileFromPresentationDescriptor(pPD, ppProfile);
    }

    SafeRelease(&pResolver);
    SafeRelease(&pSourceUnk);
    SafeRelease(&pSource);
    SafeRelease(&pPD);
    return hr;
}
```



<span data-ttu-id="acac6-142">En este ejemplo se usa [SafeRelease](saferelease.md) para liberar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="acac6-142">This example uses [SafeRelease](saferelease.md) to release interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acac6-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acac6-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acac6-144">Perfil ASF</span><span class="sxs-lookup"><span data-stu-id="acac6-144">ASF Profile</span></span>](asf-profile.md)
</dt> </dl>

 

 



