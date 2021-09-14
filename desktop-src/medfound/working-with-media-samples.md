---
description: Trabajar con ejemplos multimedia
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: Trabajar con ejemplos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363578"
---
# <a name="working-with-media-samples"></a>Trabajar con ejemplos multimedia

En este tema se describe cómo usar la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para manipular objetos de ejemplo multimedia. Para obtener información general sobre los ejemplos de medios, vea [Ejemplos de medios](media-samples.md).

Para crear un nuevo ejemplo multimedia, llame a [**la función MFCreateSample.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) Inicialmente, la lista de búferes del ejemplo está vacía. Para agregar un búfer al final de la lista, llame [**a IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

El código siguiente muestra cómo crear un ejemplo y agregarle un búfer.


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



La manera recomendada de obtener los búferes del ejemplo es llamar [**aSAMPLESample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). Este método devuelve un único búfer continguous.

Para recorrer en iteración los búferes de la lista, empiece por llamar a [**IMFSample::GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount). Este método devuelve el número de búferes. A [**continuación, llame aSAMPLESample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) y especifique el índice del búfer que se recuperará. Los búferes se indexa desde cero.

El código siguiente muestra cómo recorrer en iteración los búferes de un ejemplo.


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



Los ejemplos tienen una marca de tiempo y una duración. La marca de tiempo indica cuándo se deben representar los datos del ejemplo, en relación con el reloj de presentación. La duración es el período de tiempo durante el que se deben representar los datos. Normalmente, el componente que genera los datos establece la marca de tiempo inicial y la duración. La sesión multimedia puede modificar estos valores. Para establecer la marca de tiempo, llame [**a IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Para establecer la duración, llame [**a IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Los ejemplos también pueden tener atributos, que contienen información adicional sobre el ejemplo. Para obtener una lista de atributos de ejemplo, vea [Atributos de ejemplo.](sample-attributes.md) Para establecer y recuperar atributos, use la [**interfazATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), que [**INHERITSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) hereda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de medios](media-samples.md)
</dt> <dt>

[Búferes multimedia](media-buffers.md)
</dt> </dl>

 

 



