---
description: Microsoft Media Foundation admite la captura de audio y vídeo.
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: Captura de audio y vídeo en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506c14ee4ab94a27cfafbe18a97ffa8f05676f1f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697962"
---
# <a name="audiovideo-capture-in-media-foundation"></a>Captura de audio y vídeo en Media Foundation

Microsoft Media Foundation admite la captura de audio y vídeo. Los dispositivos de captura de vídeo se admiten a través del controlador de la clase UVC y deben ser compatibles con UVC 1,1. Los dispositivos de captura de audio se admiten a través de la API de sesión de audio de Windows (WASAPI).

Un dispositivo de captura se representa en Media Foundation mediante un objeto de origen multimedia, que expone la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . En la mayoría de los casos, la aplicación no usará esta interfaz directamente, pero usará una API de nivel superior como el [lector de origen](source-reader.md) para controlar el dispositivo de captura.

## <a name="enumerate-capture-devices"></a>Enumerar dispositivos de captura

Para enumerar los dispositivos de captura en el sistema, realice los pasos siguientes:

1.  Llame a la función [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos.
2.  Establezca el atributo de [ \_ tipo de origen del \_ atributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) en uno de los siguientes valores:

    | Value                                                    | Descripción                      |
    |----------------------------------------------------------|----------------------------------|
    | **\_tipo de origen del atributo MF DEVSOURCE \_ \_ \_ \_ \_ GUID AUDCAP** | Enumerar los dispositivos de captura de audio. |
    | **\_tipo de origen de atributo MF DEVSOURCE de \_ \_ \_ \_ VIDCAP \_ GUID** | Enumerar los dispositivos de captura de vídeo. |

    

     

3.  Llame a la función [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) . Esta función asigna una matriz de punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Cada puntero representa un objeto de activación para un dispositivo del sistema.
4.  Llame al método [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para crear una instancia del origen multimedia a partir de uno de los objetos de activación.

En el ejemplo siguiente se crea un origen de medios para el primer dispositivo de captura de vídeo en la lista de enumeración:


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



Puede consultar los objetos de activación para varios atributos, como los siguientes:

-   El atributo de [ \_ \_ \_ \_ nombre descriptivo del atributo MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) contiene el nombre para mostrar del dispositivo. El nombre para mostrar es adecuado para mostrar al usuario, pero podría no ser único.
-   En el caso de los dispositivos de vídeo, el atributo de [ \_ tipo de origen del atributo MF DEVSOURCE de \_ \_ código fuente de atributo \_ \_ VIDCAP \_ \_ ](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) contiene el vínculo simbólico al dispositivo. El vínculo simbólico identifica de forma única el dispositivo en el sistema, pero no es una cadena legible.
-   En el caso de los dispositivos de audio, el atributo [MF \_ DEVSOURCE \_ tipo de origen de \_ \_ \_ \_ \_ identificador de extremo AUDCAP](mf-devsource-attribute-source-type-audcap-endpoint-id.md) contiene el ID. de punto de conexión de audio del dispositivo. El identificador del punto de conexión de audio es similar a un vínculo simbólico. Identifica de forma única el dispositivo en el sistema, pero no es una cadena legible.

En el ejemplo siguiente se toma una matriz de punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) y se imprime el nombre para mostrar de cada dispositivo en la ventana de depuración:


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



Si ya conoce el vínculo simbólico de un dispositivo de vídeo, hay otra manera de crear el origen de medios para el dispositivo:

1.  Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos.
2.  Establezca el atributo de [tipo de origen del \_ \_ atributo MF \_ \_ DEVSOURCE](mf-devsource-attribute-source-type.md) en el **tipo de origen de \_ atributo MF DEVSOURCE de \_ \_ \_ \_ VIDCAP \_ GUID**.
3.  Establezca el [tipo de origen del atributo MF DEVSOURCE atributo de \_ \_ \_ \_ \_ \_ \_ vínculo simbólico de VIDCAP](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) en el vínculo simbólico.
4.  Llame a la función [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . El primero devuelve un puntero [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . El último devuelve un puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) a un objeto de activación. Puede usar el objeto de activación para crear el origen. (Se pueden calcular las referencias de un objeto de activación en otro proceso, por lo que resulta útil si desea crear el origen en otro proceso. Para obtener más información, vea [objetos de activación](activation-objects.md)).

En el ejemplo siguiente se toma el vínculo simbólico de un dispositivo de vídeo y se crea un origen de medios.


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



Existe una manera equivalente de crear un dispositivo de audio a partir del identificador de punto de conexión de audio:

1.  Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos.
2.  Establezca el atributo de [tipo de origen del \_ \_ atributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) en el **tipo de origen de atributo MF \_ DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID**.
3.  Establezca el atributo de ID. de [ \_ punto de \_ \_ \_ \_ \_ \_ conexión del tipo de origen del atributo MF DEVSOURCE](mf-devsource-attribute-source-type-audcap-endpoint-id.md) en el ID. de extremo.
4.  Llame a la función [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .

En el ejemplo siguiente se toma un identificador de punto de conexión de audio y se crea un origen de medios.


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a>Uso de un dispositivo de captura

Después de crear el origen de medios para un dispositivo de captura, use el [lector de origen](source-reader.md) para obtener datos del dispositivo. El lector de origen proporciona ejemplos de medios que contienen los datos de audio de captura o fotogramas de vídeo. El paso siguiente depende del escenario de la aplicación:

-   Vista previa de vídeo: Use Microsoft Direct3D o Direct2D para mostrar el vídeo.
-   Captura de archivo: Use el [escritor de receptor](sink-writer.md) para codificar el archivo.
-   Vista previa de audio: use [WASAPI](/windows/desktop/CoreAudio/wasapi).

Si quiere combinar la captura de audio con la captura de vídeo, use el *origen multimedia agregado*. El origen multimedia agregado contiene una colección de orígenes multimedia y combina todos sus flujos en un solo objeto de origen multimedia. Para crear una instancia del origen multimedia agregado, llame a la función [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) .

## <a name="shut-down-the-capture-device"></a>Apagar el dispositivo de captura

Cuando el dispositivo de captura ya no sea necesario, debe apagar el dispositivo mediante una llamada a [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el objeto [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que obtuvo mediante una llamada a [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Si no se llama al **cierre** , pueden producirse vínculos de memoria porque el sistema puede mantener una referencia a los recursos de **IMFMediaSource** hasta que se llama al **cierre** .


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



Si ha asignado una cadena que contiene el vínculo simbólico a un dispositivo de captura, también debe liberar este objeto.


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de audio y vídeo](audio-video-capture.md)
</dt> </dl>

 

 
