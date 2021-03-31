---
title: Ejemplos de medios (Windows Media Format 11 SDK)
description: Ejemplos de medios
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- SDK de Windows Media Format, ejemplos de medios
- SDK de Windows Media Format, ejemplos
- Advanced Systems Format (ASF), ejemplos de medios
- ASF (formato de sistemas avanzados), ejemplos de medios
- Advanced Systems Format (ASF), ejemplos
- ASF (formato de sistemas avanzados), ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d46a933775877f4566115ba3936c0f9f8bd7b3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103995874"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="915d0-109">Ejemplos de medios (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="915d0-109">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="915d0-110">Un ejemplo multimedia, o ejemplo, es un bloque de datos multimedia digitales.</span><span class="sxs-lookup"><span data-stu-id="915d0-110">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="915d0-111">Un ejemplo es la unidad básica que manipulan los objetos de lectura y escritura del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="915d0-111">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="915d0-112">El contenido de un ejemplo individual viene determinado por el tipo de medio asociado al ejemplo.</span><span class="sxs-lookup"><span data-stu-id="915d0-112">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="915d0-113">En el caso de vídeo, cada ejemplo representa un solo fotograma.</span><span class="sxs-lookup"><span data-stu-id="915d0-113">For video, each sample represents a single frame.</span></span> <span data-ttu-id="915d0-114">En el caso de audio, la cantidad de datos de un ejemplo individual se establece en el perfil que se usa para crear el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="915d0-114">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="915d0-115">Los ejemplos pueden contener datos sin comprimir o pueden contener datos comprimidos, en cuyo caso se denominan *ejemplos de secuencias*.</span><span class="sxs-lookup"><span data-stu-id="915d0-115">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="915d0-116">Al crear un archivo ASF, se pasan ejemplos al escritor.</span><span class="sxs-lookup"><span data-stu-id="915d0-116">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="915d0-117">El escritor coordina la compresión de los ejemplos con el códec adecuado y organiza los datos comprimidos en la sección de datos del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="915d0-117">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="915d0-118">En la reproducción, el lector Lee los datos comprimidos, los descomprime y proporciona los datos sin comprimir reconstruidos como ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="915d0-118">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="915d0-119">Todos los ejemplos utilizados por el SDK de Windows Media Format se encapsulan en un objeto de búfer cuya memoria se asigna automáticamente por los componentes en tiempo de ejecución del SDK.</span><span class="sxs-lookup"><span data-stu-id="915d0-119">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="915d0-120">También puede asignar sus propios búferes si es necesario, con las características avanzadas del escritor y del lector.</span><span class="sxs-lookup"><span data-stu-id="915d0-120">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="915d0-121">**Nota:** El término ejemplo se usa en este SDK para hacer referencia a un ejemplo multimedia, no a un ejemplo de audio.</span><span class="sxs-lookup"><span data-stu-id="915d0-121">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="915d0-122">En la codificación de audio, un ejemplo hace referencia a un único valor de audio codificado.</span><span class="sxs-lookup"><span data-stu-id="915d0-122">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="915d0-123">Normalmente, la calidad del audio codificado se especifica mediante un número de muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="915d0-123">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="915d0-124">Por ejemplo, el sonido de la calidad del CD se graba en 44.100 muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="915d0-124">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="915d0-125">Este valor suele abreviarse con la notación de Hz, por lo que 44.100 muestras por segundo serían de 44.100 Hz o 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="915d0-125">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="915d0-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="915d0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="915d0-127">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="915d0-127">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="915d0-128">**Interfaz INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="915d0-128">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="915d0-129">**Entradas, secuencias y salidas**</span><span class="sxs-lookup"><span data-stu-id="915d0-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




