---
description: Uso de Demux con secuencias elementales
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: Uso de Demux con secuencias elementales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b9004d6c99db96405797016b0d9854c96dae92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360878"
---
# <a name="using-the-demux-with-elementary-streams"></a>Uso de Demux con secuencias elementales

Cuando el Demux MPEG-2 entrega cargas de PES, envía el flujo de bytes ES en lotes de ejemplos de medios. El tamaño de muestra predeterminado es 8 KB. Demux inicia un nuevo ejemplo multimedia en cada límite de PES, pero puede dividir una única carga de PES en varios ejemplos. Por ejemplo, si una carga de PES es de 20 000, se entregará en dos ejemplos de 8K seguidos de un ejemplo de 4K. Demux no examina el contenido de la secuencia de bytes. Depende del descodificador analizar los encabezados de la secuencia y buscar los cambios de formato.

Cuando el PIN de salida del filtro de Demux se conecta al descodificador, ofrece el tipo de medio que se especificó cuando se creó el PIN. Dado que Demux no examina el flujo de bytes ES, no valida el tipo de medio. En teoría, un descodificador MPEG-2 debe ser capaz de conectarse solo con el tipo principal y el subtipo rellenado para indicar el tipo de datos. A continuación, el descodificador debe examinar los encabezados de secuencia que llegan en los ejemplos de medios. Sin embargo, en la práctica, muchos descodificadores no se conectarán a menos que el tipo de medio incluya un bloque de formato completo.

Por ejemplo, supongamos que el PID 0x31 contiene el vídeo de perfil principal MPEG-2. Como mínimo, debe realizar los pasos siguientes.

En primer lugar, cree un tipo de medio para vídeo MPEG-2. Dejando el bloque de formato por ahora:


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



A continuación, cree un PIN de salida en Demux:


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Create a new output pin.
    IPin *pPin0;
    hr = pDemux->CreateOutputPin(&mt, L"Video Pin", &pPin0);
    if (SUCCEEDED(hr))
    {
        ....
    }
}
```



Después, consulte el nuevo PIN para la interfaz **IMPEG2PIDMap** y llame a **MapPID**. Especifique el número de PID 0x30 y \_ el \_ flujo elemental de multimedia para las cargas de PES.


```C++
// Query the pin for IMPEG2PIDMap. This implicitly configures the
// demux to carry a transport stream. 
IMPEG2PIDMap *pPidMap;
hr = pPin0->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
if (SUCCEEDED(hr))
{
    // Assign PID 0x31 to pin 0. Set the type to "PES payload."
    ULONG Pid = 0x031;
    hr = pPidMap->MapPID(1, &Pid, MEDIA_ELEMENTARY_STREAM);
    pPidMap->Release();
}
```



Por último, libere todas las interfaces cuando haya terminado:


```C++
pPin0->Release();
pDemux->Release();
```



Este es un ejemplo más completo del establecimiento del tipo de medio, incluido el bloque de formato. En este ejemplo se sigue suponiendo un vídeo de perfil principal MPEG-2. Los detalles variarán en función del contenido del flujo:


```C++
// Set up a byte array to hold the first sequence header. 
// This may or may not be required, depending on the decoder.
BYTE SeqHdr[] = { ... };  // Contains the sequence header (not shown).

AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
mt.formattype = FORMAT_MPEG2Video;

// Allocate the format block, including space for the sequence header. 
mt.cbFormat = sizeof(MPEG2VIDEOINFO) + sizeof(SeqHdr);
mt.pbFormat = (BYTE*)CoTaskMemAlloc(mt.cbFormat);
if (mt.pbFormat == NULL)
{
    // Out of memory; return an error code.
}
ZeroMemory(mt.pbFormat, mt.cbFormat);

// Cast the buffer pointer to an MPEG2VIDEOINFO struct.
MPEG2VIDEOINFO *pMVIH = (MPEG2VIDEOINFO*)mt.pbFormat;

RECT rcSrc = {0, 480, 0, 720};        // Source rectangle.
pMVIH->hdr.rcSource = rcSrc;
pMVIH->hdr.dwBitRate = 4000000;       // Bit rate.
pMVIH->hdr.AvgTimePerFrame = 333667;  // 29.97 fps.
pMVIH->hdr.dwPictAspectRatioX = 4;    // 4:3 aspect ratio.
pMVIH->hdr.dwPictAspectRatioY = 3;

// BITMAPINFOHEADER information.
pMVIH->hdr.bmiHeader.biSize = 40;
pMVIH->hdr.bmiHeader.biWidth = 720;
pMVIH->hdr.bmiHeader.biHeight = 480;

pMVIH->dwLevel = AM_MPEG2Profile_Main;  // MPEG-2 profile. 
pMVIH->dwProfile = AM_MPEG2Level_Main;  // MPEG-2 level.

// Copy the sequence header into the format block.
pMVIH->cbSequenceHeader = sizeof(SeqHdr); // Size of sequence header.
memcpy(pMVIH->dwSequenceHeader, SeqHdr, sizeof(SeqHdr));
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



