---
title: Compatibilidad con código de tiempo SMPTE
description: Compatibilidad con código de tiempo SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- SDK de Windows Media Format, códigos de tiempo SMPTE
- Advanced Systems Format (ASF), códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo SMPTE
- SDK de Windows Media Format, interfaz IWMReaderTimecode
- Advanced Systems Format (ASF), IWMReaderTimecode (interfaz)
- ASF (formato de sistemas avanzados), interfaz IWMReaderTimecode
- Códigos de tiempo SMPTE, acerca de
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532992"
---
# <a name="smpte-time-code-support"></a><span data-ttu-id="3ed73-111">Compatibilidad con código de tiempo SMPTE</span><span class="sxs-lookup"><span data-stu-id="3ed73-111">SMPTE Time Code Support</span></span>

<span data-ttu-id="3ed73-112">El SDK de Windows Media Format proporciona compatibilidad limitada para el código de tiempo SMPTE, que es un formato de código de hora estándar para películas y televisión.</span><span class="sxs-lookup"><span data-stu-id="3ed73-112">The Windows Media Format SDK provides limited support for SMPTE time code, which is a standard time code format for movies and television.</span></span> <span data-ttu-id="3ed73-113">Puede incluir datos de código de tiempo SMPTE con ejemplos como extensiones de unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="3ed73-113">You can include SMPTE time code data with samples as data unit extensions.</span></span> <span data-ttu-id="3ed73-114">La parte de datos de la extensión es una estructura de [**\_ datos de extensión de código de tiempo \_ \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) que contiene la información de la marca de tiempo de SMPTE original.</span><span class="sxs-lookup"><span data-stu-id="3ed73-114">The data portion of the extension is a [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structure containing the information from the original SMPTE time stamp.</span></span>

<span data-ttu-id="3ed73-115">El mantenimiento del código de tiempo SMPTE en los archivos ASF incluye límites de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="3ed73-115">Maintaining SMPTE time code in your ASF files comes with performance limits.</span></span> <span data-ttu-id="3ed73-116">Cada ejemplo con una marca de tiempo de SMPTE asociada requiere el transporte de los 14 bytes en la estructura de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3ed73-116">Each sample with an associated SMPTE time stamp requires transport of the 14 bytes in the time stamp structure.</span></span> <span data-ttu-id="3ed73-117">En un escenario de streaming, este mayor requisito de ancho de banda podría ser catastrófico.</span><span class="sxs-lookup"><span data-stu-id="3ed73-117">In a streaming scenario, this increased bandwidth requirement could be catastrophic.</span></span> <span data-ttu-id="3ed73-118">Como resultado, se recomienda que los códigos de tiempo de SMPTE solo se almacenen en archivos ASF durante el proceso de edición de vídeo, que normalmente se realiza con archivos locales.</span><span class="sxs-lookup"><span data-stu-id="3ed73-118">As a result, it is suggested that SMPTE time codes only be persisted in ASF files during the video editing process, which is typically done with local files.</span></span> <span data-ttu-id="3ed73-119">Cuando se cree el archivo final, debe quitar las extensiones de unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="3ed73-119">When the final file is created, you should remove the data unit extensions.</span></span>

<span data-ttu-id="3ed73-120">Puede leer las marcas de tiempo de SMPTE tal como lo haría con cualquier otra extensión de unidad de datos, pero los objetos de lectura proporcionan compatibilidad integrada para la búsqueda por código de tiempo de SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3ed73-120">You can read SMPTE time stamps just as you would read any other data unit extension, but the reading objects provide integrated support for searching by SMPTE time code.</span></span> <span data-ttu-id="3ed73-121">Para poder buscar marcas de tiempo de SMPTE, primero debe indexar el archivo por código de tiempo de SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3ed73-121">To be able to search for SMPTE time stamps, you must first index the file by SMPTE time code.</span></span> <span data-ttu-id="3ed73-122">Puede configurar el indexador para indexar los códigos de tiempo mediante el método [**IWMIndexer2:: configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) .</span><span class="sxs-lookup"><span data-stu-id="3ed73-122">You can configure the indexer to index time codes by using the [**IWMIndexer2::Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) method.</span></span>

<span data-ttu-id="3ed73-123">Con el lector asincrónico, puede navegar por las marcas de tiempo de SMPTE en un archivo mediante los métodos de la interfaz [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) y el método [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) .</span><span class="sxs-lookup"><span data-stu-id="3ed73-123">Using the asynchronous reader, you can navigate a file by SMPTE time stamps using the methods of the [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) interface and the [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) method.</span></span> <span data-ttu-id="3ed73-124">Con el lector sincrónico, use [**IWMSyncReader2:: SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span><span class="sxs-lookup"><span data-stu-id="3ed73-124">With the synchronous reader, use [**IWMSyncReader2::SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ed73-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3ed73-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ed73-126">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="3ed73-126">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="3ed73-127">**Configuración de extensiones de unidades de datos**</span><span class="sxs-lookup"><span data-stu-id="3ed73-127">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




