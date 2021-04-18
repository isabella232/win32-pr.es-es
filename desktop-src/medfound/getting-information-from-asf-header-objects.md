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
# <a name="getting-information-from-asf-header-objects"></a>Obtener información de los objetos de encabezado ASF

La información del encabezado ASF se almacena en los objetos de encabezado ASF de un archivo multimedia. Media Foundation proporciona el [objeto ContentInfo de ASF](asf-contentinfo-object.md) para trabajar con el objeto de encabezado. Se requiere un objeto ContentInfo rellenado para que la aplicación pueda leer la información de encabezado de un archivo existente. Esto se logra mediante una llamada a [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader). Si el análisis se completa correctamente, la biblioteca ASF del archivo, que se mantiene internamente mediante Media Foundation, se rellena con información de encabezado de varios objetos de encabezado. Algunas de estas propiedades se exponen a la aplicación, que se puede recuperar a través de los atributos del descriptor de presentación, el descriptor de flujo, el perfil y las propiedades de metadatos.

Para obtener una lista completa de los atributos, consulte [atributos de Media Foundation para los objetos de encabezado ASF](media-foundation-attributes-for-asf-header-objects.md).

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a>Recuperar información de encabezado de un descriptor de presentación

Un objeto de descriptor de presentación contiene la descripción de un origen multimedia determinado, en este caso el origen de medios ASF. Si la llamada a **ParseHeader** se completa correctamente, la información de nivel de archivo del objeto de encabezado se almacena como atributos en el descriptor de presentación. Para crear el descriptor de presentación, llame a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Este método devuelve un puntero a un objeto de descriptor de presentación rellenado que contiene estos atributos para el archivo ASF asociado al objeto ContentInfo. Para obtener valores de atributos específicos, llame a los métodos **IMFAttributes:: GetXXX** en el descriptor de presentación y especifique el atributo **MF \_ PD \_ ASF \_ XXX** .

En el código de ejemplo siguiente se recupera la duración de la reproducción de un archivo ASF, especificado por un objeto ContentInfo.


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



Para obtener más información acerca de los descriptores de presentación en general, consulte [descriptores de presentación](presentation-descriptors.md).

Para obtener el conjunto completo de atributos de descriptor de presentación, vea [atributos de descriptor de presentación](presentation-descriptor-attributes.md).

## <a name="retrieving-header-information-from-a-stream-descriptor"></a>Recuperar información de encabezado de un descriptor de flujo

Un objeto de descriptor de flujo expone la interfaz [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) y describe las características de las secuencias del archivo. El descriptor de presentación del contenido ASF contiene uno o más descriptores de flujo que representan las secuencias enumeradas en el objeto de encabezado. Después de que la llamada a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) finalice correctamente, los descriptores de flujo subyacentes se rellenan con información de nivel de flujo de los distintos objetos de encabezado. Para obtener un descriptor de flujo para una secuencia ASF, llame a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) en el descriptor de presentación que se genera a partir del objeto ContentInfo.

Algunas de las propiedades de la secuencia se establecen como atributos en los descriptores de flujo. Llame a los métodos **IMFAttributes:: GetXXX** en un descriptor de flujo y especifique el atributo **MF \_ SD \_ ASF \_ XXX** .

Para obtener el conjunto completo de atributos de descriptor de secuencia, vea los atributos "descriptor de secuencia específico de ASF" enumerados en [los atributos del descriptor de flujo](stream-descriptor-attributes.md).

## <a name="retrieving-header-information-from-the-profile-object"></a>Recuperar información de encabezado del objeto de perfil

Además de los descriptores de secuencia, el objeto de perfil ASF también describe las propiedades de la secuencia. Para obtener el perfil de un archivo ASF existente, llame a [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). El objeto de perfil ASF devuelto por este método no incluye ninguno de los atributos **MF \_ PD \_ ASF \_ XXX** . Estos atributos solo están disponibles para la aplicación después de llamar a [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) para generar el objeto de Perfil de un descriptor de presentación. Puede usar el perfil para obtener punteros a los objetos de exclusión mutua y de priorización de flujo.

Para obtener información sobre el objeto de perfil, vea [ASF Profile](asf-profile.md) .

## <a name="retrieving-metadata-from-header-objects"></a>Recuperar metadatos de objetos de encabezado

Un archivo ASF puede contener varias propiedades de metadatos que se establecen durante la codificación del archivo. Una aplicación puede enumerar estas propiedades con el objeto ContentInfo. Algunas de estas propiedades, como la información de velocidad de bits variable (VBR), están disponibles para la aplicación a través de los atributos del descriptor de presentación, los descriptores de flujo y los tipos de medios para el archivo multimedia. Estos atributos se establecen en el objeto ContentInfo durante la inicialización a través de la llamada a [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto ContentInfo de ASF](asf-contentinfo-object.md)
</dt> </dl>

 

 



