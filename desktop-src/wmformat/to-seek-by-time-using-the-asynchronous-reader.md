---
title: Para buscar por tiempo mediante el lector asincrónico
description: Para buscar por tiempo mediante el lector asincrónico
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Advanced Systems Format (ASF), búsqueda por tiempo
- ASF (formato de sistemas avanzados), búsqueda por hora
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, búsqueda por hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788812"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a><span data-ttu-id="c1aaf-108">Para buscar por tiempo mediante el lector asincrónico</span><span class="sxs-lookup"><span data-stu-id="c1aaf-108">To Seek By Time Using the Asynchronous Reader</span></span>

<span data-ttu-id="c1aaf-109">Si desea buscar un tiempo de presentación específico en un archivo ASF, el archivo debe estar configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c1aaf-109">If you want to seek to a specific presentation time in an ASF file, the file must be properly configured.</span></span> <span data-ttu-id="c1aaf-110">Puede buscar en archivos de solo audio de forma predeterminada, pero los archivos de vídeo se deben indexar antes de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c1aaf-110">You can seek in audio only files by default, but video files need to be indexed before seeking.</span></span> <span data-ttu-id="c1aaf-111">Si no está seguro de cómo se ha creado un archivo, puede comprobar el \_ atributo g wszWMSeekable en el encabezado del archivo llamando a [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="c1aaf-111">If you are not sure about how a file has been created, you can check the g\_wszWMSeekable attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="c1aaf-112">Para buscar datos en un archivo ASF en el momento de la presentación mediante el lector asincrónico, llame a [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), pasando el tiempo deseado y la duración de la parte del archivo que desea leer como *cnsStart* y *cnsDuration* , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c1aaf-112">To seek to data in an ASF file by presentation time using the asynchronous reader, call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passing the desired time and duration of the part of the file you want to read as *cnsStart* and *cnsDuration* respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1aaf-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c1aaf-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1aaf-114">**Interfaz IWMReader**</span><span class="sxs-lookup"><span data-stu-id="c1aaf-114">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="c1aaf-115">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="c1aaf-115">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="c1aaf-116">**Leer metadatos en la reproducción**</span><span class="sxs-lookup"><span data-stu-id="c1aaf-116">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="c1aaf-117">**Trabajar con índices**</span><span class="sxs-lookup"><span data-stu-id="c1aaf-117">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




