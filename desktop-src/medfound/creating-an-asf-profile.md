---
description: En este tema se describe cómo crear como perfil de ASF en Microsoft Media Foundation.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Creación de un perfil de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a0225a6ff17f68c5443fce15f9bdc196901313ccaaebdde2f7f34c49860538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743253"
---
# <a name="creating-an-asf-profile"></a>Creación de un perfil de ASF

En este tema se describe cómo crear como perfil de ASF en Microsoft Media Foundation.

-   [Crear un nuevo perfil](#create-a-new-profile)
-   [Obtener el perfil del objeto ContentInfo de ASF](#get-the-profile-from-the-asf-contentinfo-object)
-   [Obtener el perfil de un descriptor de presentación](#get-the-profile-from-a-presentation-descriptor)
-   [Temas relacionados](#related-topics)

## <a name="create-a-new-profile"></a>Crear un nuevo perfil

Para crear un perfil de ASF vacío, llame a [**la función MFCreateASFProfile.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) Esta función devuelve un puntero a la [**interfaz IMFASFProfile.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) La aplicación puede usar esta interfaz para agregar secuencias al perfil y para configurar cada una de las secuencias. Para obtener más información, [vea Creating and Configuring ASF Secuencias](creating-and-configuring-asf-streams.md).

Opcionalmente, la aplicación puede agregar objetos de exclusión mutua a dos o más secuencias. Vea [Using Mutual Exclusion for ASF Secuencias](using-mutual-exclusion-for-asf-streams.md).

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a>Obtener el perfil del objeto ContentInfo de ASF

Una aplicación puede obtener el perfil de ASF de un archivo ASF existente desde el [objeto ContentInfo de ASF](asf-contentinfo-object.md). El perfil ya está configurado y contiene la configuración de todas las secuencias del archivo.

Inicialice el objeto ContentInfo analizando el objeto de encabezado ASF del archivo. Esto se realiza mediante el [**método IMFASFContentInfo::P arseHeader.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) Una vez leídos todos los objetos de encabezado y rellenado la biblioteca de ASF, se genera el perfil de este archivo. La aplicación puede obtener un puntero a este perfil inicializado llamando a [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).

## <a name="get-the-profile-from-a-presentation-descriptor"></a>Obtener el perfil de un descriptor de presentación

Puede obtener el objeto de perfil de un archivo ASF existente desde el [descriptor](presentation-descriptors.md) de presentación del archivo o desde el objeto [ContentInfo de ASF.](asf-contentinfo-object.md) En este caso, el perfil ya está configurado y contiene la configuración de todas las secuencias del archivo. Esto puede ser útil si desea modificar un perfil de ASF existente. Por ejemplo, es posible que desee volver a codificar un archivo Windows Media Video a una velocidad de bits inferior.

Para obtener el perfil del descriptor de presentación, llame a [**MFCreateASFProfileFromPresentationDescriptor.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) Esta función analiza el descriptor de presentación y rellena un perfil de ASF con información sobre el archivo multimedia. La función devuelve un puntero a la interfaz IMFASFProfile. A continuación, puede usar esta interfaz para modificar el perfil.

Para obtener el descriptor de presentación, llame a uno de los métodos siguientes:

-   Desde el origen de medios de ASF, llame [**a IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   Desde el [objeto ContentInfo de ASF,](asf-contentinfo-object.md) llame [**a IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Antes de llamar a este método, asegúrese de que el objeto ContentInfo se inicializa para lectura. Para obtener más información, vea "Inicializar el objeto ContentInfo desde un archivo ASF existente" en Lectura del objeto de [encabezado ASF de un archivo existente.](reading-the-asf-header-object-of-an-existing-file.md) Sin embargo, si ya tiene un objeto ContentInfo inicializado, puede obtener el perfil directamente de él. Esto se describe en "Obtener el perfil del objeto ContentInfo" más adelante en este tema.

En el ejemplo siguiente se muestra cómo crear un perfil a partir de un descriptor de presentación. La función crea un origen multimedia para el archivo, obtiene el descriptor de presentación del origen de medios y crea un perfil. En este ejemplo se supone que *pszFileName* especifica la dirección URL de un archivo ASF.


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



En este ejemplo se [usa SafeRelease para](saferelease.md) liberar punteros de interfaz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Perfil de ASF](asf-profile.md)
</dt> </dl>

 

 



