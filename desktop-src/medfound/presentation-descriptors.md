---
description: Descriptores de presentación
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Descriptores de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677556"
---
# <a name="presentation-descriptors"></a>Descriptores de presentación

Una *presentación* es un conjunto de flujos multimedia relacionados que comparten un tiempo de presentación común. Por ejemplo, una presentación puede constar de secuencias de audio y vídeo de una película. Un *descriptor de presentación* es un objeto que contiene la descripción de una presentación determinada. Los descriptores de presentación se usan para configurar orígenes de medios y algunos receptores de medios.

Cada descriptor de presentación contiene una lista de uno o más descriptores de *flujo*. Describen las secuencias de la presentación. Los flujos pueden estar seleccionados o desactivados. Solo las secuencias seleccionadas generan datos. Los flujos desseleccionados no están activos y no generan ningún dato. Cada descriptor de flujo tiene un *controlador de tipo de medio*, que se usa para cambiar el tipo de archivo multimedia de la secuencia u obtener el tipo de medio actual de la secuencia. (Para obtener más información sobre los tipos de medios, consulte [tipos de medios](media-types.md)).

En la tabla siguiente se muestran las interfaces principales que expone cada uno de estos objetos.



| Object                  | Interfaz                                                      |
|-------------------------|----------------------------------------------------------------|
| Descriptor de presentación | [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| Descriptor de secuencia       | [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| Controlador de tipo de medio      | [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a>Presentaciones de origen de medios

Cada origen multimedia proporciona un descriptor de presentación que describe la configuración predeterminada del origen. En la configuración predeterminada, al menos una secuencia está seleccionada y cada flujo seleccionado tiene un tipo de medio. Para obtener el descriptor de presentación, llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). El método devuelve un puntero [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .

Puede modificar el descriptor de presentación del origen para seleccionar un conjunto diferente de secuencias. No modifique el descriptor de presentación a menos que se detenga el origen del medio. Los cambios se aplican al llamar a [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) para iniciar el origen.

Para obtener el número de secuencias, llame a [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount). Para obtener el descriptor de flujo de una secuencia, llame a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) y pase el índice de la secuencia. Los flujos se indizan desde cero. El método **GetStreamDescriptorByIndex** devuelve un puntero [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) . También devuelve una marca booleana que indica si la secuencia está seleccionada. Si la secuencia está seleccionada, el origen multimedia genera datos para esa secuencia. De lo contrario, el origen no genera ningún dato para ese flujo. Para seleccionar una secuencia, llame a [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) con el índice de la secuencia. Para anular la selección de un flujo, llame a [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).

En el código siguiente se muestra cómo obtener el descriptor de la presentación de un origen multimedia y enumerar las secuencias.


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



## <a name="media-type-handlers"></a>Controladores de tipo de medio

Para cambiar el tipo de archivo multimedia de la secuencia o para obtener el tipo de medio actual de la secuencia, use el controlador de tipo de medio del descriptor de flujo. Llame a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) para obtener el controlador de tipo de medio. Este método devuelve un puntero [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .

Si simplemente desea saber qué tipo de datos hay en la secuencia, como audio o vídeo, llame a [**IMFMediaTypeHandler:: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Este método devuelve el GUID para el tipo de medio principal. Por ejemplo, una aplicación de reproducción normalmente conecta una secuencia de audio al procesador de audio y una secuencia de vídeo al representador de vídeo. Si usa la sesión multimedia o el cargador de topología para compilar una topología, el GUID de tipo principal puede ser la única información de formato que necesite.

Si su aplicación necesita información más detallada sobre el formato actual, llame a [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Este método devuelve un puntero a la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) del tipo de medio. Use esta interfaz para obtener los detalles del formato.

El controlador de tipo de medio también contiene una lista de los tipos de medios admitidos para la secuencia. Para obtener el tamaño de la lista, llame a [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount). Para obtener un tipo de medio de la lista, llame a [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) con el índice del tipo de medio. Los tipos de medios se devuelven en el orden de preferencia aproximado. Por ejemplo, en el caso de los formatos de audio, se prefieren velocidades de ejemplo más altas que las de menor. Sin embargo, no hay ninguna regla definitiva que rija la ordenación, por lo que debe tratarla simplemente como una directriz.

Es posible que la lista de tipos admitidos no contenga todos los tipos de medios posibles que admita la secuencia. Para probar si se admite un tipo de medio determinado, llame a [**IMFMediaTypeHandler:: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported). Para establecer el tipo de medio, llame a [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype). Si el método se ejecuta correctamente, el flujo contendrá datos que se ajustan al formato especificado. El método **SetCurrentMediaType** no cambia la lista de tipos preferidos.

En el código siguiente se muestra cómo obtener el controlador de tipo de medio, enumerar los tipos de medios preferidos y establecer el tipo de medio. En este ejemplo se da por supuesto que la aplicación tiene algún algoritmo, que no se muestra aquí, para seleccionar el tipo de medio. El específico dependerá en gran medida de la aplicación.


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

[API de Media Foundation Platform](media-foundation-platform-apis.md)
</dt> </dl>

 

 



