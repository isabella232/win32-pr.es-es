---
title: Flujos de datos arbitrarios personalizados
description: Flujos de datos arbitrarios personalizados
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- SDK de Windows Media Format, flujos de datos arbitrarios personalizados
- Advanced Systems Format (ASF), flujos de datos arbitrarios personalizados
- ASF (formato de sistemas avanzados), flujos de datos arbitrarios personalizados
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- flujos de datos arbitrarios personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714255"
---
# <a name="custom-arbitrary-data-streams"></a><span data-ttu-id="43a09-110">Flujos de datos arbitrarios personalizados</span><span class="sxs-lookup"><span data-stu-id="43a09-110">Custom Arbitrary Data Streams</span></span>

<span data-ttu-id="43a09-111">Puede crear una secuencia en un archivo ASF para que contenga cualquier tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="43a09-111">You can create a stream in an ASF file to contain any sort of data.</span></span> <span data-ttu-id="43a09-112">Si ninguno de los tipos de secuencia admitidos se adapta a sus necesidades, debe usar un flujo de datos arbitrario.</span><span class="sxs-lookup"><span data-stu-id="43a09-112">If none of the supported stream types suits your needs, you must use an arbitrary data stream.</span></span> <span data-ttu-id="43a09-113">El objeto de escritor controla un flujo de datos arbitrario tal como hace cualquier flujo sin comprimir; los ejemplos se agrupan y se combinan con los ejemplos de otras secuencias en la sección de datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="43a09-113">The writer object handles an arbitrary data stream just as it does any uncompressed stream; the samples are packetized and combined with the samples from other streams in the data section of the file.</span></span> <span data-ttu-id="43a09-114">Por supuesto, solo una aplicación de lectura que se ha programado específicamente para tratar con su tipo arbitrario podrá controlar los datos después de que los entregue el objeto de lectura.</span><span class="sxs-lookup"><span data-stu-id="43a09-114">Of course, only a reading application that has been specifically programmed to deal with your arbitrary type will be able to handle the data after it is delivered by the reading object.</span></span>

<span data-ttu-id="43a09-115">Un uso común de los flujos de datos arbitrarios es para los datos multimedia codificados con un códec de terceros.</span><span class="sxs-lookup"><span data-stu-id="43a09-115">One common use of arbitrary data streams is for media data encoded by using a third-party codec.</span></span> <span data-ttu-id="43a09-116">Dado que los objetos de este SDK no interactúan directamente con códecs de terceros, la aplicación de escritura debe procesar los ejemplos con la parte de codificación del códec y pasar los ejemplos comprimidos al escritor.</span><span class="sxs-lookup"><span data-stu-id="43a09-116">Because the objects of this SDK do not interact directly with third-party codecs, your writing application must process the samples with the encoding portion of the codec and pass the compressed samples to the writer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43a09-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43a09-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43a09-118">**Flujos arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="43a09-118">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="43a09-119">**Configuración de secuencias arbitrarias personalizadas**</span><span class="sxs-lookup"><span data-stu-id="43a09-119">**Configuring Custom Arbitrary Streams**</span></span>](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




