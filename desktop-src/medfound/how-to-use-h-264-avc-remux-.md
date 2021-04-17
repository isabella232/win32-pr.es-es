---
description: En este tema se describe cuándo y cómo usar una MFT y un receptor MP4 de H. 264/AVC Remux.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Cuándo y cómo usar H. 264/AVC Remux MFT y el receptor MP4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c582fa16eae56c4fec8809caa4bd501469e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706214"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="a41f7-103">Cuándo y cómo usar H. 264/AVC Remux MFT y el receptor MP4</span><span class="sxs-lookup"><span data-stu-id="a41f7-103">When and How to Use H.264/AVC Remux MFT and MP4 Sink</span></span>

<span data-ttu-id="a41f7-104">En este tema se describe cuándo y cómo usar una MFT y un receptor MP4 de H. 264/AVC Remux.</span><span class="sxs-lookup"><span data-stu-id="a41f7-104">This topic describes when and how to use a H.264/AVC Remux MFT and MP4 Sink.</span></span>

## <a name="when-to-use-h264avc-remux-mft"></a><span data-ttu-id="a41f7-105">Cuándo usar H. 264/AVC Remux MFT</span><span class="sxs-lookup"><span data-stu-id="a41f7-105">When to use H.264/AVC Remux MFT</span></span>

<span data-ttu-id="a41f7-106">El formato de archivo MPEG-4 requiere que cada ejemplo comprimido contenga una imagen principal con unidades NAL en el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="a41f7-106">MPEG-4 file format requires that each compressed sample contains one primary picture with NAL units in the correct order.</span></span> <span data-ttu-id="a41f7-107">(Consulte la definición de la imagen principal y el orden obligatorio de las unidades de NAL en la sección 7.4.1.2.3, el **orden de las unidades nal e imágenes codificadas y la asociación con las unidades de acceso** de la especificación H. 264 AVC). También requiere que cada ejemplo comprimido esté asociado a una marca de tiempo de presentación, la marca de tiempo de descodificación y la duración de la muestra.</span><span class="sxs-lookup"><span data-stu-id="a41f7-107">(Please refer to the definition of primary picture and mandatory NAL units order in section 7.4.1.2.3, **Order of NAL units and coded pictures and association to access units**, of the H.264 AVC specification.) It also requires each compressed sample is associated with a presentation time stamp, decoding time stamp, and sample duration.</span></span>

<span data-ttu-id="a41f7-108">En muchos escenarios en los que las aplicaciones necesitan grabar vídeo H. 264/AVC en un contenedor de archivos MPEG-4, el ejemplo comprimido podría no cumplir los requisitos anteriores.</span><span class="sxs-lookup"><span data-stu-id="a41f7-108">In many scenarios when applications need to record H.264/AVC video in a MPEG-4 file container, the compressed sample may not satisfy the above requirements.</span></span> <span data-ttu-id="a41f7-109">Por ejemplo, un ejemplo comprimido podría no contener una imagen principal completa o podría no tener asociada una marca de tiempo de presentación correcta.</span><span class="sxs-lookup"><span data-stu-id="a41f7-109">For example, one compressed sample might not contain a complete primary picture or might not have a correct presentation time stamp associated with it.</span></span> <span data-ttu-id="a41f7-110">Algunos ejemplos de aplicaciones son:</span><span class="sxs-lookup"><span data-stu-id="a41f7-110">A few application examples are:</span></span>

-   <span data-ttu-id="a41f7-111">Escriba el vídeo elemental de streaming H. 264/AVC en el contenedor de archivos MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="a41f7-111">Write H.264/AVC streaming elementary video into MPEG-4 file container.</span></span>
-   <span data-ttu-id="a41f7-112">Grabe vídeo capturado H. 264/AVC elemental en el contenedor de archivos MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="a41f7-112">Record camera captured H.264/AVC elementary video in MPEG-4 file container.</span></span>
-   <span data-ttu-id="a41f7-113">Grabe la videoconferencia H. 264/AVC en el contenedor de archivos MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="a41f7-113">Record H.264/AVC video conference in MPEG-4 file container.</span></span>
-   <span data-ttu-id="a41f7-114">Concatene dos vídeo H. 264/AVC en MPEG-2 TS o MP4 y escriba en el contenedor de archivos MPEG-4 con las marcas de tiempo correctas.</span><span class="sxs-lookup"><span data-stu-id="a41f7-114">Concatenate two H.264/AVC video in MPEG-2 TS or MP4 and write into MPEG-4 file container with correct time stamps.</span></span>
-   <span data-ttu-id="a41f7-115">Remux H. 264/AVC vídeo desde AVCHD, formato de archivo MPEG-2 TS/PS a formato de archivo MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="a41f7-115">Remux H.264/AVC video from AVCHD, MPEG-2 TS/PS file format to MPEG-4 file format.</span></span>
-   <span data-ttu-id="a41f7-116">Recorte el archivo de vídeo H. 264/AVC sin transcodificar.</span><span class="sxs-lookup"><span data-stu-id="a41f7-116">Trim H.264/AVC video file without transcoding.</span></span>

<span data-ttu-id="a41f7-117">En esta situación, la aplicación debe usar una MFT de H. 264/AVC Remux para convertir los ejemplos comprimidos que no contienen una imagen principal completa antes de que se escriban en el contenedor de archivos MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="a41f7-117">In this situation, the application needs to use a H.264/AVC remux MFT to convert the compressed samples not containing a complete primary picture before they are written into the MPEG-4 file container.</span></span>

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="a41f7-118">Uso de la MFT y el receptor MP4 de H. 264/AVC Remux</span><span class="sxs-lookup"><span data-stu-id="a41f7-118">How to use H.264/AVC Remux MFT and MP4 sink</span></span>

<span data-ttu-id="a41f7-119">Establezca el tipo de medio de salida de origen en **MFVideoFormat \_ H264 \_ es**, lo que indica que cada ejemplo podría no contener una imagen principal completa.</span><span class="sxs-lookup"><span data-stu-id="a41f7-119">Set the source output media type to **MFVideoFormat\_H264\_ES**, which indicates each sample might not contain a complete primary picture.</span></span> <span data-ttu-id="a41f7-120">Establezca el tipo de medio de entrada del receptor de MP4 en **MFVideoFormat \_ H264**.</span><span class="sxs-lookup"><span data-stu-id="a41f7-120">Set the input media type of MP4 sink to **MFVideoFormat\_H264**.</span></span> <span data-ttu-id="a41f7-121">Por lo tanto, el tipo de medio de entrada del MFT H. 264/AVC Remux es **MFVideoFormat \_ H264 \_** es y el tipo de medio de salida de la MFT h. 264/AVC Remux es **MFVideoFormat \_ H264**, que se insertará automáticamente en la resolución de la topología.</span><span class="sxs-lookup"><span data-stu-id="a41f7-121">So, the input media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264\_ES** and the output media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264**, which will be automatically inserted into the topology resolver.</span></span>

<span data-ttu-id="a41f7-122">La duración de ejemplo se omite en H. 264/AVC Remux, porque la duración de la muestra para una muestra que no contiene una imagen principal completa no tiene un significado claro.</span><span class="sxs-lookup"><span data-stu-id="a41f7-122">Sample duration is ignored by the H.264/AVC remux, because the sample duration for a sample not containing a complete primary picture does not have clear meaning.</span></span> <span data-ttu-id="a41f7-123">En su lugar, la duración de la muestra se calcula a partir de la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="a41f7-123">Instead, the sample duration is calculated from the frame rate.</span></span> <span data-ttu-id="a41f7-124">La velocidad de fotogramas se calcula a partir del parámetro de secuencia.</span><span class="sxs-lookup"><span data-stu-id="a41f7-124">The frame rate is calculated from the sequence parameter.</span></span> <span data-ttu-id="a41f7-125">Si la información no existe en el parámetro Sequence, la velocidad de fotogramas se calcula a partir de los parámetros del tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="a41f7-125">If the information does not exist in the sequence parameter, the frame rate is calculated from the parameters in the input media type.</span></span> <span data-ttu-id="a41f7-126">Si la información de velocidad de fotogramas no está disponible, se usa la velocidad de fotogramas predeterminada de 29,97 fps.</span><span class="sxs-lookup"><span data-stu-id="a41f7-126">If frame rate information is not available, the default frame rate of 29.97 fps is used.</span></span>

<span data-ttu-id="a41f7-127">H. 264/AVC Remux MFT interpola linealmente las marcas de tiempo de descodificación (DTS) de cada imagen comprimida según la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="a41f7-127">H.264/AVC remux MFT linearly interpolates the decoding time stamps (DTS) for each compressed picture according to the frame rate.</span></span> <span data-ttu-id="a41f7-128">H. 264/AVC Remux MFT respeta las marcas de tiempo de presentación de entrada (PTS) en los ejemplos de entrada y los pasa a la salida si existen.</span><span class="sxs-lookup"><span data-stu-id="a41f7-128">H.264/AVC remux MFT honors the input presentation time stamps (PTS) in input samples and passes them to the output if they exist.</span></span> <span data-ttu-id="a41f7-129">Realiza la interpolación PTS de acuerdo con la velocidad de fotogramas, el PTS anterior y el orden de salida de la imagen a través del proceso de rugosidad del almacenamiento en búfer de imágenes (DBP), tal y como se especifica en el **Anexo C. 4.5.3** de la especificación H. 264 AVC.</span><span class="sxs-lookup"><span data-stu-id="a41f7-129">It performs PTS interpolation according to frame rate, the previous PTS, and the picture output order through Decoded Picture Buffering (DBP) bumping process as specified in **Annex C.4.5.3 Bumping process** of the H.264 AVC specification.</span></span> <span data-ttu-id="a41f7-130">Cada ejemplo de salida de la MFT H. 264/AVC Remux debe tener PTS, DTS y la duración de la muestra.</span><span class="sxs-lookup"><span data-stu-id="a41f7-130">Each output sample from the H.264/AVC remux MFT shall have PTS, DTS, and sample duration.</span></span> <span data-ttu-id="a41f7-131">La MFT H. 264/AVC Remux también identifica las imágenes de IDR en el fragmentada y las establece como punto de limpieza con el atributo MF de [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="a41f7-131">H.264/AVC remux MFT also identifies the IDR pictures in the bitstream and sets them as clean point with the MF attribute of [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md).</span></span>

<span data-ttu-id="a41f7-132">Actualmente, la MFT de H. 264/AVC Remux puede controlar un máximo de 64 fotograma reordenado.</span><span class="sxs-lookup"><span data-stu-id="a41f7-132">Currently the H.264/AVC remux MFT can handle a maximum of 64 reordered frame.</span></span> <span data-ttu-id="a41f7-133">Si el número de fotogramas reordenados supera el valor de 64 con un marco de referencia a largo plazo, el MFT de H. 264/AVC Remux interpolará un valor de PTS equivocado para ese fotograma y generará ese fotograma en un momento equivocado.</span><span class="sxs-lookup"><span data-stu-id="a41f7-133">If the number of reordered frame exceeds 64 with a long term reference frame present, the H.264/AVC remux MFT will interpolate a wrong PTS for that frame and output that frame at a wrong time.</span></span>

<span data-ttu-id="a41f7-134">Para crear una instancia de un MFT de H. 264/AVC Remux, establezca los tipos de medios de entrada y salida correctos en la MFT H. 264/AVC Remux, establezca el tipo de medio de entrada para el receptor MP4 y resuelva la topología.</span><span class="sxs-lookup"><span data-stu-id="a41f7-134">To instantiate a H.264/AVC remux MFT, set the correct input and output media types on the H.264/AVC remux MFT, set the input media type for the MP4 sink, and resolve the topology.</span></span>

<span data-ttu-id="a41f7-135">En el código de ejemplo siguiente se muestra cómo inicializar la MFT de H. 264/AVC Remux y el receptor MP4.</span><span class="sxs-lookup"><span data-stu-id="a41f7-135">The following sample code show how to initialize the H.264/AVC remux MFT and MP4 sink.</span></span>

<span data-ttu-id="a41f7-136">Para MFT Remux de H. 264/AVC,</span><span class="sxs-lookup"><span data-stu-id="a41f7-136">For H.264/AVC remux MFT,</span></span>


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



<span data-ttu-id="a41f7-137">No es necesario realizar ninguna otra configuración.</span><span class="sxs-lookup"><span data-stu-id="a41f7-137">No further configuration is necessary.</span></span>

<span data-ttu-id="a41f7-138">Para el receptor MP4,</span><span class="sxs-lookup"><span data-stu-id="a41f7-138">For MP4 sink,</span></span>


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a><span data-ttu-id="a41f7-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a41f7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a41f7-140">Formatos de medios admitidos en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a41f7-140">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



