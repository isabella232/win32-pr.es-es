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
# <a name="creating-an-asf-profile"></a>Creación de un perfil ASF

En este tema se describe cómo crear como perfil ASF en Microsoft Media Foundation.

-   [Crear un nuevo perfil](#create-a-new-profile)
-   [Obtener el perfil del objeto ASF ContentInfo](#get-the-profile-from-the-asf-contentinfo-object)
-   [Obtener el perfil de un descriptor de presentación](#get-the-profile-from-a-presentation-descriptor)
-   [Temas relacionados](#related-topics)

## <a name="create-a-new-profile"></a>Crear un nuevo perfil

Para crear un perfil ASF vacío, llame a la función [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) . Esta función devuelve un puntero a la interfaz [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) . La aplicación puede utilizar esta interfaz para agregar secuencias al perfil y para configurar cada una de las secuencias. Para obtener más información, vea [crear y configurar secuencias ASF](creating-and-configuring-asf-streams.md).

Opcionalmente, la aplicación puede agregar objetos de exclusión mutua a dos o más secuencias. Consulte [uso de la exclusión mutua para secuencias ASF](using-mutual-exclusion-for-asf-streams.md).

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a>Obtener el perfil del objeto ASF ContentInfo

Una aplicación puede obtener el perfil ASF de un archivo ASF existente del [objeto ASF ContentInfo](asf-contentinfo-object.md). El perfil ya está configurado y contiene la configuración de todas las secuencias del archivo.

Inicialice el objeto ContentInfo analizando el objeto de encabezado ASF del archivo. Esto se realiza a través del método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) . Una vez que se han leído todos los objetos de encabezado y se ha rellenado la biblioteca ASF, se genera el perfil de este archivo. La aplicación puede obtener un puntero a este perfil inicializado mediante una llamada a [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).

## <a name="get-the-profile-from-a-presentation-descriptor"></a>Obtener el perfil de un descriptor de presentación

Puede obtener el objeto de Perfil de un archivo ASF existente del [descriptor de presentación](presentation-descriptors.md) del archivo o del objeto [ContentInfo ASF](asf-contentinfo-object.md) . En este caso, el perfil ya está configurado y contiene la configuración de todas las secuencias del archivo. Esto puede ser útil si desea modificar un perfil ASF existente. Por ejemplo, puede que desee volver a codificar un archivo Windows Media Video a una velocidad de bits inferior.

Para obtener el perfil del descriptor de presentación, llame a [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor). Esta función analiza el descriptor de presentación y rellena un perfil ASF con información sobre el archivo multimedia. La función devuelve un puntero a la interfaz IMFASFProfile. Después, puede usar esta interfaz para modificar el perfil.

Para obtener el descriptor de la presentación, llame a uno de los métodos siguientes:

-   En el origen de medios ASF, llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   En el objeto [ASF ContentInfo](asf-contentinfo-object.md) , llame a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Antes de llamar a este método, asegúrese de que el objeto ContentInfo se inicializa para lectura. Para obtener más información, vea "inicializar el objeto ContentInfo desde un archivo ASF existente" en [leer el objeto de encabezado ASF de un archivo existente](reading-the-asf-header-object-of-an-existing-file.md). Sin embargo, si ya tiene un objeto ContentInfo inicializado, puede obtener el perfil directamente de él. Esto se describe en "obtener el perfil del objeto ContentInfo" más adelante en este tema.

En el ejemplo siguiente se muestra cómo crear un perfil a partir de un descriptor de presentación. La función crea un origen multimedia para el archivo, obtiene el descriptor de presentación del origen multimedia y crea un perfil. En este ejemplo se da por supuesto que *pszFileName* especifica la dirección URL de un archivo ASF.


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



En este ejemplo se usa [SafeRelease](saferelease.md) para liberar punteros de interfaz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Perfil ASF](asf-profile.md)
</dt> </dl>

 

 



