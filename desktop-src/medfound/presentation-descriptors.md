---
description: Descriptores de presentación
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Descriptores de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963faeebbb180b504cc11202645a9432bbb3a94e988495b9ddcf96e550b05519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238836"
---
# <a name="presentation-descriptors"></a>Descriptores de presentación

Una *presentación* es un conjunto de secuencias multimedia relacionadas que comparten un tiempo de presentación común. Por ejemplo, una presentación puede constar de las secuencias de audio y vídeo de una película. Un *descriptor de* presentación es un objeto que contiene la descripción de una presentación determinada. Los descriptores de presentación se usan para configurar orígenes multimedia y algunos receptores multimedia.

Cada descriptor de presentación contiene una lista de uno o varios *descriptores de secuencia.* Aquí se describen las secuencias de la presentación. Secuencias se puede seleccionar o no seleccionar. Solo los flujos seleccionados generan datos. Los flujos deseleccionados no están activos y no generan ningún dato. Cada descriptor de flujo tiene un *controlador de tipo* de medio , que se usa para cambiar el tipo de medio de la secuencia u obtener el tipo de medio actual de la secuencia. (Para obtener más información sobre los tipos de medios, vea [Tipos de medios).](media-types.md)

En la tabla siguiente se muestran las interfaces principales que expone cada uno de estos objetos.



| Object                  | Interfaz                                                      |
|-------------------------|----------------------------------------------------------------|
| Descriptor de presentación | [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| Descriptor de secuencia       | [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| Controlador de tipo de medio      | [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a>Presentaciones de orígenes multimedia

Cada origen de medios proporciona un descriptor de presentación que describe la configuración predeterminada para el origen. En la configuración predeterminada, se selecciona al menos una secuencia y cada secuencia seleccionada tiene un tipo de medio. Para obtener el descriptor de presentación, llame [**a IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). El método devuelve un [**puntero IMFPresentationDescriptor.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

Puede modificar el descriptor de presentación del origen para seleccionar un conjunto diferente de secuencias. No modifique el descriptor de presentación a menos que se detenga el origen multimedia. Los cambios se aplican cuando se llama [**a IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) para iniciar el origen.

Para obtener el número de secuencias, llame [**a IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount). Para obtener el descriptor de flujo de una secuencia, llame a [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) y pase el índice de la secuencia. Secuencias se indexa a partir de cero. El **método GetStreamDescriptorByIndex** devuelve un [**puntero IMFStreamDescriptor.**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) También devuelve una marca booleana que indica si la secuencia está seleccionada. Si la secuencia está seleccionada, el origen multimedia genera datos para esa secuencia. De lo contrario, el origen no genera ningún dato para esa secuencia. Para seleccionar una secuencia, llame [**a IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) con el índice de la secuencia. Para anular la selección de una secuencia, llame [**a IMFPresentationDescriptor::D eselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).

El código siguiente muestra cómo obtener el descriptor de presentación de un origen multimedia y enumerar las secuencias.


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a>Controladores de tipos de medios

Para cambiar el tipo de medio de la secuencia o para obtener el tipo de medio actual de la secuencia, use el controlador de tipo de medio del descriptor de secuencia. Llame [**a IMFStreamDescriptor::GetMediaTypeHandler para**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) obtener el controlador de tipo de medio. Este método devuelve un [**puntero IMFMediaTypeHandler.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)

Si simplemente desea saber qué tipo de datos hay en la secuencia, como audio o vídeo, llame a [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Este método devuelve el GUID del tipo de medio principal. Por ejemplo, una aplicación de reproducción normalmente conecta una secuencia de audio al representador de audio y una secuencia de vídeo al representador de vídeo. Si usa la sesión multimedia o el cargador de topologías para compilar una topología, el GUID de tipo principal podría ser la única información de formato que necesita.

Si la aplicación necesita información más detallada sobre el formato actual, llame a [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Este método devuelve un puntero a la [**interfaz IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) del tipo de medio. Use esta interfaz para obtener los detalles del formato.

El controlador de tipos de medios también contiene una lista de tipos de medios admitidos para la secuencia. Para obtener el tamaño de la lista, llame [**a IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount). Para obtener un tipo de medio de la lista, llame a [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) con el índice del tipo de medio. Los tipos de medios se devuelven en el orden aproximado de preferencia. Por ejemplo, para los formatos de audio, se prefieren velocidades de muestreo más altas en lugar de velocidades de muestreo más bajas. Sin embargo, no hay ninguna regla definitiva que rige la ordenación, por lo que debe tratarla simplemente como una guía.

Es posible que la lista de tipos admitidos no contenga todos los posibles tipos de medios que admite la secuencia. Para probar si se admite un tipo de medio determinado, llame a [**IMFMediaTypeHandler::IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported). Para establecer el tipo de medio, llame [**a IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype). Si el método se realiza correctamente, la secuencia contendrá datos que se ajusten al formato especificado. El **método SetCurrentMediaType** no cambia la lista de tipos preferidos.

El código siguiente muestra cómo obtener el controlador de tipo de medio, enumerar los tipos de medios preferidos y establecer el tipo de medio. En este ejemplo se supone que la aplicación tiene algún algoritmo, que no se muestra aquí, para seleccionar el tipo de medio. Los detalles específicos dependerán en gran medida de la aplicación.


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Media Foundation PLATFORM API](media-foundation-platform-apis.md)
</dt> </dl>

 

 



