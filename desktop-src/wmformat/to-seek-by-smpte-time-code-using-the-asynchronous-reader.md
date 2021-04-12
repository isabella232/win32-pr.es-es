---
title: Para buscar por el código de tiempo de SMPTE mediante el lector asincrónico
description: Para buscar por el código de tiempo de SMPTE mediante el lector asincrónico
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Advanced Systems Format (ASF), búsqueda por códigos de tiempo de SMPTE
- ASF (formato de sistemas avanzados), búsqueda por códigos de tiempo de SMPTE
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo SMPTE
- lectores asincrónicos, búsquedas por códigos de tiempo de SMPTE
- lectores asincrónicos, códigos de tiempo SMPTE
- Códigos de tiempo de SMPTE, búsqueda
- Códigos de tiempo de SMPTE, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bb90e899db9820ccbd14e42b9699a5f99c7434
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420233"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a><span data-ttu-id="b1c3b-113">Para buscar por el código de tiempo de SMPTE mediante el lector asincrónico</span><span class="sxs-lookup"><span data-stu-id="b1c3b-113">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>

<span data-ttu-id="b1c3b-114">El objeto lector puede buscar en un punto de un archivo basándose en el código de tiempo SMPTE asociado con una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-114">The reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="b1c3b-115">Los datos de código de tiempo se encapsulan en las estructuras de [**\_ datos de extensión de código de tiempo \_ \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) que se adjuntan a los ejemplos de vídeo como extensiones de unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="b1c3b-116">Los códigos de tiempo de SMPTE se definen mediante un intervalo y un código de tiempo dentro de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="b1c3b-117">Un intervalo es una serie continua de códigos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="b1c3b-118">Cada código de tiempo se define por horas, minutos, segundos y fotogramas.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="b1c3b-119">Para buscar datos en un archivo ASF mediante código de tiempo SMPTE mediante el lector asincrónico, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-119">To seek data in an ASF file by SMPTE time code using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="b1c3b-120">Obtenga un puntero a la interfaz [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) del objeto lector llamando a **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-120">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="b1c3b-121">Establezca el código de tiempo de inicio y la duración mediante una llamada a [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span><span class="sxs-lookup"><span data-stu-id="b1c3b-121">Set the starting time code and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="b1c3b-122">Debe especificar el número de secuencia de un flujo de vídeo que se indexa por código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-122">You must specify the stream number of a video stream that is indexed by time code.</span></span> <span data-ttu-id="b1c3b-123">El lector sincronizará el resto de los resultados con el tiempo de presentación del marco especificado de la secuencia especificada y comenzará a entregar ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-123">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="b1c3b-124">Controle los ejemplos como lo haría normalmente en su implementación del método **IWMReaderCallback::** .</span><span class="sxs-lookup"><span data-stu-id="b1c3b-124">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1c3b-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1c3b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1c3b-126">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="b1c3b-127">**Trabajar con índices**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="b1c3b-128">**Compatibilidad con código de tiempo SMPTE**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-128">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> </dl>

 

 




