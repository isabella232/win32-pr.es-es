---
description: Establecer tipos de medios en un DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Establecer tipos de medios en un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061601"
---
# <a name="setting-media-types-on-a-dmo"></a>Establecer tipos de medios en un DMO

Para que DMO procesar datos, el cliente debe establecer el tipo de medio para cada secuencia. (Hay una excepción secundaria a esta regla; vea [Opcional Secuencias](optional-streams.md)). Para buscar el número de secuencias, llame al [**método IMediaObject::GetStreamCount:**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount)


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



Este método devuelve dos valores, el número de entradas y el número de salidas. Estos valores se fijan para la duración del DMO.

**Tipos preferidos**

Para cada secuencia, el DMO asigna una lista de posibles tipos de medios, en orden de preferencia. Por ejemplo, los tipos preferidos podrían ser RGB de 32, RGB de 24 bits y RGB de 16 bits, en ese orden. Cuando el cliente establece los tipos de medios, puede usar estas listas como sugerencia. Para recuperar un tipo preferido para una secuencia, llame al método [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) o [**al método IMediaObject::GetOutputType.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) Especifique el número de secuencia y un valor de índice para el tipo (empezando por cero). Por ejemplo, el código siguiente recupera el primer tipo preferido del primer flujo de entrada:


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



Para enumerar todos los tipos de medios preferidos en una secuencia determinada, use un bucle que incremente el índice de tipos hasta que el método devuelva DMO E NO MORE ITEMS, como se muestra en el \_ \_ ejemplo \_ \_ siguiente:


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



Debe tener en cuenta los siguientes puntos sobre los tipos preferidos:

-   El DMO podría devolver un tipo que no tiene ningún bloque de formato. Por ejemplo, un DMO podría especificar un tipo de vídeo, como RGB de 24 bits, sin proporcionar el ancho y el alto de la imagen. Sin embargo, al establecer el tipo, debe proporcionar un bloque de formato completo. (Algunos tipos de medios, como MIDI, nunca requieren un bloque de formato, en cuyo caso no se aplica este comentario).
-   El DMO no es necesario para admitir todas las combinaciones de tipos preferidos que devuelve. Por ejemplo, si un DMO tiene dos secuencias y cada secuencia tiene cuatro tipos preferidos, hay 16 combinaciones posibles, pero no se garantiza que todas sean válidas.
-   Cuando el cliente establece el tipo de medio para una secuencia, el DMO podría actualizar los tipos preferidos para que otras secuencias reflejen el nuevo estado. Sin embargo, no es necesario hacerlo.
-   Para algunas secuencias, la DMO podría no ofrecer ningún tipo preferido. Normalmente, un DMO debe ofrecer al menos algunos tipos preferidos en algunas secuencias.
-   El DMO no es necesario para ofrecer una lista completa de los tipos de medios que puede aceptar. Puede haber tipos "sin invertir" que el DMO admite, pero no ofrece como tipos preferidos.

En resumen, el cliente debe tratar los tipos preferidos solo como instrucciones. La única manera de saber con certeza qué tipos se admiten es probarlos, como se describe en la sección siguiente.

**Establecimiento del tipo de medio en una secuencia**

Use los [**métodos IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) para establecer el tipo de cada secuencia. Debe proporcionar una estructura **DMO \_ MEDIA \_ TYPE** que contenga una descripción completa del tipo de medio. En el ejemplo siguiente se establece el tipo de medio en el flujo de entrada 0, mediante audio PCM estéreo de 16 bits de 44,1 kHz:


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



Para probar un tipo de medio sin establecerlo, llame a **SetInputType** o **SetOutputType** con la DMO \_ SET \_ TYPEF \_ TEST \_ ONLY. El método devuelve S OK si el tipo es aceptable o S FALSE en caso \_ \_ contrario:


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



Dado que la configuración de una secuencia puede afectar a otra secuencia, es posible que tenga que borrar el tipo de medio de una secuencia. Para ello, llame a **SetInputType** o **SetOutputType** con DMO \_ marca SET \_ TYPEF \_ CLEAR.

Para un descodificador DMO, el cliente normalmente establecería primero el tipo de entrada y, a continuación, elegiría un tipo de salida. Para un codificador DMO, el cliente establecería primero el tipo de salida y, a continuación, el tipo de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hospedaje directo de un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



