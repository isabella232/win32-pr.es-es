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
# <a name="using-the-demux-with-elementary-streams"></a><span data-ttu-id="be0fb-103">Uso de Demux con secuencias elementales</span><span class="sxs-lookup"><span data-stu-id="be0fb-103">Using the Demux with Elementary Streams</span></span>

<span data-ttu-id="be0fb-104">Cuando el Demux MPEG-2 entrega cargas de PES, envía el flujo de bytes ES en lotes de ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="be0fb-104">When the MPEG-2 demux delivers PES payloads, it sends the ES byte stream in batches of media samples.</span></span> <span data-ttu-id="be0fb-105">El tamaño de muestra predeterminado es 8 KB.</span><span class="sxs-lookup"><span data-stu-id="be0fb-105">The default sample size is 8K.</span></span> <span data-ttu-id="be0fb-106">Demux inicia un nuevo ejemplo multimedia en cada límite de PES, pero puede dividir una única carga de PES en varios ejemplos.</span><span class="sxs-lookup"><span data-stu-id="be0fb-106">The demux starts a new media sample on each PES boundary, but may break a single PES payload into several samples.</span></span> <span data-ttu-id="be0fb-107">Por ejemplo, si una carga de PES es de 20 000, se entregará en dos ejemplos de 8K seguidos de un ejemplo de 4K.</span><span class="sxs-lookup"><span data-stu-id="be0fb-107">For example, if a PES payload is 20K, it will be delivered in two 8K samples followed by one 4K sample.</span></span> <span data-ttu-id="be0fb-108">Demux no examina el contenido de la secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="be0fb-108">The demux does not examine the contents of the byte stream.</span></span> <span data-ttu-id="be0fb-109">Depende del descodificador analizar los encabezados de la secuencia y buscar los cambios de formato.</span><span class="sxs-lookup"><span data-stu-id="be0fb-109">It is up to the decoder to parse the sequence headers and look for format changes.</span></span>

<span data-ttu-id="be0fb-110">Cuando el PIN de salida del filtro de Demux se conecta al descodificador, ofrece el tipo de medio que se especificó cuando se creó el PIN.</span><span class="sxs-lookup"><span data-stu-id="be0fb-110">When the demux filter's output pin connects to the decoder, it offers the media type that was specified when the pin was created.</span></span> <span data-ttu-id="be0fb-111">Dado que Demux no examina el flujo de bytes ES, no valida el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="be0fb-111">Because the demux does not examine the ES byte stream, it does not validate the media type.</span></span> <span data-ttu-id="be0fb-112">En teoría, un descodificador MPEG-2 debe ser capaz de conectarse solo con el tipo principal y el subtipo rellenado para indicar el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="be0fb-112">In theory, an MPEG-2 decoder should be able to connect with just the major type and subtype filled in, to indicate the type of data.</span></span> <span data-ttu-id="be0fb-113">A continuación, el descodificador debe examinar los encabezados de secuencia que llegan en los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="be0fb-113">The decoder should then examine the sequence headers that arrive in the media samples.</span></span> <span data-ttu-id="be0fb-114">Sin embargo, en la práctica, muchos descodificadores no se conectarán a menos que el tipo de medio incluya un bloque de formato completo.</span><span class="sxs-lookup"><span data-stu-id="be0fb-114">However, in practice, many decoders will not connect unless the media type includes a complete format block.</span></span>

<span data-ttu-id="be0fb-115">Por ejemplo, supongamos que el PID 0x31 contiene el vídeo de perfil principal MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="be0fb-115">For example, suppose that PID 0x31 contains MPEG-2 main profile video.</span></span> <span data-ttu-id="be0fb-116">Como mínimo, debe realizar los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="be0fb-116">At a minimum, you would need to do the following steps.</span></span>

<span data-ttu-id="be0fb-117">En primer lugar, cree un tipo de medio para vídeo MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="be0fb-117">First, create a media type for MPEG-2 video.</span></span> <span data-ttu-id="be0fb-118">Dejando el bloque de formato por ahora:</span><span class="sxs-lookup"><span data-stu-id="be0fb-118">Leaving aside the format block for now:</span></span>


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



<span data-ttu-id="be0fb-119">A continuación, cree un PIN de salida en Demux:</span><span class="sxs-lookup"><span data-stu-id="be0fb-119">Next, create an output pin on the demux:</span></span>


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



<span data-ttu-id="be0fb-120">Después, consulte el nuevo PIN para la interfaz **IMPEG2PIDMap** y llame a **MapPID**.</span><span class="sxs-lookup"><span data-stu-id="be0fb-120">Then, query the new pin for the **IMPEG2PIDMap** interface and call **MapPID**.</span></span> <span data-ttu-id="be0fb-121">Especifique el número de PID 0x30 y \_ el \_ flujo elemental de multimedia para las cargas de PES.</span><span class="sxs-lookup"><span data-stu-id="be0fb-121">Specify PID number 0x30, and MEDIA\_ELEMENTARY\_STREAM for PES payloads.</span></span>


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



<span data-ttu-id="be0fb-122">Por último, libere todas las interfaces cuando haya terminado:</span><span class="sxs-lookup"><span data-stu-id="be0fb-122">Finally, release all interfaces when you are done:</span></span>


```C++
pPin0->Release();
pDemux->Release();
```



<span data-ttu-id="be0fb-123">Este es un ejemplo más completo del establecimiento del tipo de medio, incluido el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="be0fb-123">Here is a more complete example of setting the media type, including the format block.</span></span> <span data-ttu-id="be0fb-124">En este ejemplo se sigue suponiendo un vídeo de perfil principal MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="be0fb-124">This example still assumes an MPEG-2 main profile video.</span></span> <span data-ttu-id="be0fb-125">Los detalles variarán en función del contenido del flujo:</span><span class="sxs-lookup"><span data-stu-id="be0fb-125">The details will vary depending on stream contents:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="be0fb-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="be0fb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be0fb-127">Usar el demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="be0fb-127">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



