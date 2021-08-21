---
description: La información de encabezado de ASF se almacena en los objetos de encabezado asf de un archivo multimedia.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Obtener información de objetos de encabezado de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346e57721137fd6064e4d6b9fd21080d96c10e740bb7f7ed45bf3fef4cc92722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974444"
---
# <a name="getting-information-from-asf-header-objects"></a>Obtener información de objetos de encabezado de ASF

La información de encabezado de ASF se almacena en los objetos de encabezado asf de un archivo multimedia. Media Foundation proporciona el objeto [ContentInfo de ASF](asf-contentinfo-object.md) para trabajar con el objeto de encabezado. Se requiere un objeto ContentInfo rellenado para que la aplicación lea la información de encabezado de un archivo existente. Esto se logra mediante una llamada [**a IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader). Si el análisis se completa correctamente, la biblioteca asf del archivo, que se mantiene internamente mediante Media Foundation, se rellena con información de encabezado de varios objetos de encabezado. Algunas de estas propiedades se exponen a la aplicación, que puede recuperar a través de atributos en el descriptor de presentación, el descriptor de flujo, el perfil y las propiedades de metadatos.

Para obtener la lista completa de atributos, [vea Atributos Media Foundation para objetos de encabezado de ASF.](media-foundation-attributes-for-asf-header-objects.md)

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a>Recuperar información de encabezado de un descriptor de presentación

Un objeto descriptor de presentación contiene la descripción de un origen multimedia determinado, en este caso el origen de medios de ASF. Si la **llamada a ParseHeader** se completa correctamente, la información de nivel de archivo del objeto de encabezado se almacena como atributos en el descriptor de presentación. Para crear el descriptor de presentación, llame [**a IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Este método devuelve un puntero a un objeto de descriptor de presentación rellenado que contiene estos atributos para el archivo ASF asociado al objeto ContentInfo. Para obtener valores para atributos específicos, llame a **los métodos MFAttributes::Getxxx** en el descriptor de presentación y especifique el atributo **MF PD \_ \_ ASF \_ xxx.**

El código de ejemplo siguiente recupera la duración de reproducción de un archivo ASF, especificado por un objeto ContentInfo.


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



Para obtener más información sobre los descriptores de presentación en general, vea [Descriptores de presentación](presentation-descriptors.md).

Para obtener el conjunto completo de atributos del descriptor de presentación, vea [Atributos del descriptor de presentación](presentation-descriptor-attributes.md).

## <a name="retrieving-header-information-from-a-stream-descriptor"></a>Recuperar información de encabezado de un descriptor de flujo

Un objeto de descriptor de flujo expone la [**interfaz IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) y describe las características de las secuencias del archivo. El descriptor de presentación del contenido de ASF contiene uno o varios descriptores de secuencia que representan las secuencias enumeradas en el objeto de encabezado. Una vez completada correctamente la llamada a [**IMFASFContentInfo::GeneratePresentationDescriptor,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) los descriptores de flujo subyacentes se rellenan con información de nivel de flujo de los distintos objetos de encabezado. Para obtener un descriptor de flujo para una secuencia de ASF, llame a [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) en el descriptor de presentación que se genera a partir del objeto ContentInfo.

Algunas de las propiedades de flujo se establecen como atributos en descriptores de flujo. Llame **a los métodos MFAttributes::Getxxx** en un descriptor de flujo y especifique el atributo **XXX de MF SD \_ \_ ASF. \_**

Para obtener el conjunto completo de atributos de descriptor de flujo, vea los atributos "AsF-Specific Stream Descriptor" (Descriptor de flujo específico de ASF) enumerados en Stream Descriptor Attributes (Atributos [de descriptor de flujo).](stream-descriptor-attributes.md)

## <a name="retrieving-header-information-from-the-profile-object"></a>Recuperar información de encabezado desde el objeto Profile

Además de los descriptores de flujo, el objeto de perfil de ASF también describe las propiedades de la secuencia. Para obtener el perfil de un archivo ASF existente, llame a [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). El objeto de perfil de ASF devuelto por este método no incluye ninguno de los atributos XXX de **\_ MF PD \_ ASF. \_** Estos atributos están disponibles para la aplicación solo después de llamar a [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) para generar el objeto de perfil a partir de un descriptor de presentación. Puede usar el perfil para obtener punteros a los objetos de exclusión mutua y priorización de secuencias.

Para obtener información sobre el objeto de perfil, vea [Asf Profile](asf-profile.md) .

## <a name="retrieving-metadata-from-header-objects"></a>Recuperar metadatos de objetos de encabezado

Un archivo ASF puede contener varias propiedades de metadatos que se establecen durante la codificación de archivos. Una aplicación puede enumerar estas propiedades con el objeto ContentInfo. Algunas de estas propiedades, como la información de velocidad de bits variable (VBR), están disponibles para la aplicación a través de atributos en el descriptor de presentación, descriptores de flujo y tipos de medios para el archivo multimedia. Estos atributos se establecen en el objeto ContentInfo durante la inicialización mediante la [**llamada a ParseHeader.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto ContentInfo de ASF](asf-contentinfo-object.md)
</dt> </dl>

 

 



