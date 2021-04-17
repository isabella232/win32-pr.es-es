---
description: Establecimiento de tipos de medios en DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Establecimiento de tipos de medios en DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689665"
---
# <a name="setting-media-types-on-a-dmo"></a>Establecimiento de tipos de medios en DMO

Antes de que un DMO pueda procesar los datos, el cliente debe establecer el tipo de medio para cada flujo. (Hay una excepción secundaria a esta regla; consulte [secuencias opcionales](optional-streams.md)). Para encontrar el número de flujos, llame al método [**IMediaObject:: GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) :


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



Este método devuelve dos valores, el número de entradas y el número de salidas. Estos valores son fijos para la duración de DMO.

**Tipos preferidos**

Para cada flujo, DMO asigna una lista de posibles tipos de medios, en orden de preferencia. Por ejemplo, los tipos preferidos podrían ser 32-RGB, RGB de 24 bits y RGB de 16 bits, en ese orden. Cuando el cliente establece los tipos de medios, puede usar estas listas como una sugerencia. Para recuperar un tipo preferido para un flujo, llame al método [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) o [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) . Especifique el número de secuencia y un valor de índice para el tipo (empezando desde cero). Por ejemplo, el código siguiente recupera el primer tipo preferido del primer flujo de entrada:


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



Para enumerar todos los tipos de medios preferidos en un flujo determinado, use un bucle que incremente el índice de tipo hasta que el método devuelva DMO \_ E \_ ningún \_ \_ elemento más, como se muestra en el ejemplo siguiente:


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



Debe tener en cuenta los siguientes puntos acerca de los tipos preferidos:

-   DMO podría devolver un tipo que no tiene ningún bloque de formato. Por ejemplo, un DMO podría especificar un tipo de vídeo, como RGB de 24 bits, sin proporcionar el ancho y el alto de la imagen. Sin embargo, al establecer el tipo, debe proporcionar un bloque de formato completo. (Algunos tipos de medios, como MIDI, nunca requieren un bloque de formato, en cuyo caso no se aplica este comentario).
-   No es necesario que DMO admita cada combinación de tipos preferidos que devuelve. Por ejemplo, si una DMO tiene dos flujos y cada flujo tiene cuatro tipos preferidos, hay 16 combinaciones posibles, pero no se garantiza que todos ellos sean válidos.
-   Cuando el cliente establece el tipo de medio para un flujo, DMO podría actualizar los tipos preferidos para que otras secuencias reflejen el nuevo estado. Sin embargo, no es necesario hacerlo.
-   En algunos flujos, DMO podría no ofrecer ningún tipo preferido. Normalmente, un DMO debe proporcionar al menos algunos tipos preferidos en algunas secuencias.
-   No es necesario que DMO ofrezca una lista completa de los tipos de medios que puede aceptar. Puede haber tipos "sin anunciar" que el DMO admita pero no ofrezca como tipos preferidos.

En Resumen, el cliente debe tratar solo los tipos preferidos como instrucciones. La única forma de saber para determinados tipos que se admiten es probarla, como se describe en la sección siguiente.

**Establecer el tipo de medio en una secuencia**

Use los métodos [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) y [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) para establecer el tipo de cada flujo. Debe proporcionar una estructura **de \_ \_ tipo de medio DMO** que contenga una descripción completa del tipo de medio. En el ejemplo siguiente se establece el tipo de medio en el flujo de entrada 0, mediante audio PCM estéreo de 16 bits 44,1-kHz:


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



Para probar un tipo de medio sin establecerlo, llame a **SetInputType** o **SetOutputType** con la \_ marca DMO set \_ TYPEF \_ Test \_ only. El método devuelve S \_ OK si el tipo es aceptable o S \_ false en caso contrario:


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



Dado que la configuración de una secuencia puede afectar a otra secuencia, puede que tenga que borrar el tipo de archivo multimedia de una secuencia. Para ello, llame a **SetInputType** o **SetOutputType** con la \_ marca DMO set \_ TYPEF \_ Clear.

Para un descodificador DMO, el cliente normalmente establecería el tipo de entrada primero y, a continuación, elegiría un tipo de salida. Para un codificador DMO, el cliente establecería primero el tipo de salida y, a continuación, el tipo de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hospedar directamente un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



