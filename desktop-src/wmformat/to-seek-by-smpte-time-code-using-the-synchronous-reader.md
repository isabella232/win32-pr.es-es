---
title: Para buscar por el código de tiempo de SMPTE mediante el lector sincrónico
description: Para buscar por el código de tiempo de SMPTE mediante el lector sincrónico
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Advanced Systems Format (ASF), búsqueda por códigos de tiempo de SMPTE
- ASF (formato de sistemas avanzados), búsqueda por códigos de tiempo de SMPTE
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- Advanced Systems Format (ASF), códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo SMPTE
- lectores sincrónicos, búsquedas por códigos de tiempo de SMPTE
- lectores sincrónicos, códigos de tiempo SMPTE
- Códigos de tiempo de SMPTE, búsqueda
- Códigos de tiempo de SMPTE, lectores sincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c843ba802272d02f1dfc885a3c65b3d124b7423
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358704"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a><span data-ttu-id="761f6-113">Para buscar por el código de tiempo de SMPTE mediante el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="761f6-113">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>

<span data-ttu-id="761f6-114">El objeto de lector sincrónico puede buscar en un punto de un archivo basándose en el código de tiempo SMPTE asociado con una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="761f6-114">The synchronous reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="761f6-115">Los datos de código de tiempo se encapsulan en las estructuras de [**\_ datos de extensión de código de tiempo \_ \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) que se adjuntan a los ejemplos de vídeo como extensiones de unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="761f6-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="761f6-116">Los códigos de tiempo de SMPTE se definen mediante un intervalo y un código de tiempo dentro de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="761f6-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="761f6-117">Un intervalo es una serie continua de códigos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="761f6-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="761f6-118">Cada código de tiempo se define por horas, minutos, segundos y fotogramas.</span><span class="sxs-lookup"><span data-stu-id="761f6-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="761f6-119">Para buscar datos en un archivo ASF por código de tiempo SMPTE mediante el lector sincrónico, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="761f6-119">To seek data in an ASF file by SMPTE time code using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="761f6-120">Establezca el código de tiempo de inicio y el código de hora de finalización para la entrega de ejemplo llamando a [**IWMSyncReader:: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span><span class="sxs-lookup"><span data-stu-id="761f6-120">Set the starting time code and ending time code for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="761f6-121">Debe especificar el número de secuencia de un flujo de vídeo indexado por código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="761f6-121">You must specify the stream number of a video stream indexed by time code.</span></span> <span data-ttu-id="761f6-122">El lector sincrónico sincronizará el resto de los resultados con el tiempo de presentación del marco especificado de la secuencia especificada.</span><span class="sxs-lookup"><span data-stu-id="761f6-122">The synchronous reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream.</span></span>
2.  <span data-ttu-id="761f6-123">Comience a recuperar ejemplos con llamadas a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="761f6-123">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="761f6-124">Continúe como lo haría normalmente con el lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="761f6-124">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="761f6-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="761f6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="761f6-126">**Leer archivos con el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="761f6-126">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="761f6-127">**Compatibilidad con código de tiempo SMPTE**</span><span class="sxs-lookup"><span data-stu-id="761f6-127">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> <dt>

[<span data-ttu-id="761f6-128">**Trabajar con índices**</span><span class="sxs-lookup"><span data-stu-id="761f6-128">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




