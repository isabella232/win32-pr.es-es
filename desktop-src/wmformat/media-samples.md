---
title: Ejemplos de medios (Windows Media Format SDK 11)
description: Obtenga información sobre los ejemplos multimedia en el SDK Windows Media Format 11. Un ejemplo multimedia es un objeto que contiene una lista ordenada de cero o más búferes.
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media Format SDK,ejemplos multimedia
- Windows Media Format SDK,samples
- Formato de sistemas avanzados (ASF), ejemplos multimedia
- ASF (formato de sistemas avanzados), ejemplos multimedia
- Formato de sistemas avanzados (ASF), ejemplos
- ASF (formato de sistemas avanzados), ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8d264aa23e80f1e692f28789c2f2e631ef3ed8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989080"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="83e54-110">Ejemplos de medios (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="83e54-110">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="83e54-111">Un ejemplo multimedia, o ejemplo, es un bloque de datos multimedia digitales.</span><span class="sxs-lookup"><span data-stu-id="83e54-111">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="83e54-112">Un ejemplo es la unidad básica manipulada por los objetos de lectura y escritura del SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="83e54-112">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="83e54-113">El contenido de una muestra individual viene determinado por el tipo de medio asociado a la muestra.</span><span class="sxs-lookup"><span data-stu-id="83e54-113">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="83e54-114">En el caso del vídeo, cada ejemplo representa un único fotograma.</span><span class="sxs-lookup"><span data-stu-id="83e54-114">For video, each sample represents a single frame.</span></span> <span data-ttu-id="83e54-115">En el caso del audio, la cantidad de datos de un ejemplo individual se establece en el perfil utilizado para crear el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="83e54-115">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="83e54-116">Las muestras pueden contener datos sin comprimir o pueden contener datos comprimidos, en cuyo caso se denominan *ejemplos de secuencia.*</span><span class="sxs-lookup"><span data-stu-id="83e54-116">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="83e54-117">Al crear un archivo ASF, se pasan ejemplos al escritor.</span><span class="sxs-lookup"><span data-stu-id="83e54-117">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="83e54-118">El sistema de escritura coordina la compresión de los ejemplos con el códec adecuado y organiza los datos comprimidos en la sección de datos del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="83e54-118">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="83e54-119">Durante la reproducción, el lector lee los datos comprimidos, los descomprime y proporciona los datos reconstruidos sin comprimir como ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="83e54-119">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="83e54-120">Todos los ejemplos usados por Windows Media Format SDK se encapsulan en el objeto de búfer cuya memoria se asigna automáticamente por los componentes en tiempo de ejecución del SDK.</span><span class="sxs-lookup"><span data-stu-id="83e54-120">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="83e54-121">También puede asignar sus propios búferes si es necesario, mediante las características avanzadas del escritor y el lector.</span><span class="sxs-lookup"><span data-stu-id="83e54-121">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="83e54-122">**Nota** El término ejemplo se usa en este SDK para hacer referencia a un ejemplo multimedia, no a un ejemplo de audio.</span><span class="sxs-lookup"><span data-stu-id="83e54-122">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="83e54-123">En la codificación de audio, un ejemplo hace referencia a un único valor de audio codificado.</span><span class="sxs-lookup"><span data-stu-id="83e54-123">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="83e54-124">Normalmente, la calidad del audio codificado se especifica mediante un número de muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="83e54-124">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="83e54-125">Por ejemplo, el sonido de calidad de CD se registra en 44 100 muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="83e54-125">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="83e54-126">Este valor se abrevia normalmente con la notación Hz, por lo que 44 100 muestras por segundo serían 44 100 Hz o 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="83e54-126">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83e54-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83e54-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83e54-128">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="83e54-128">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="83e54-129">**Interfaz INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="83e54-129">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="83e54-130">**Entradas, flujos y salidas**</span><span class="sxs-lookup"><span data-stu-id="83e54-130">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




