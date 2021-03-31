---
title: Trabajar con salidas
description: Trabajar con salidas
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- SDK de Windows Media Format, trabajar con salidas
- Advanced Systems Format (ASF), trabajar con salidas
- ASF (formato de sistemas avanzados), trabajar con salidas
- Formato de sistemas avanzados (ASF), números y formatos de salida
- ASF (formato de sistemas avanzados), números y formatos de salida
- números y formatos de salida, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788733"
---
# <a name="working-with-outputs"></a><span data-ttu-id="5e1cd-109">Trabajar con salidas</span><span class="sxs-lookup"><span data-stu-id="5e1cd-109">Working with Outputs</span></span>

<span data-ttu-id="5e1cd-110">De forma predeterminada, cada ejemplo que recibe de cualquier objeto de lector está asociado a un número de salida.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-110">As a default, every sample you receive from either reader object is associated with an output number.</span></span> <span data-ttu-id="5e1cd-111">Cada número de salida corresponde a una secuencia del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-111">Each output number corresponds to a stream in the ASF file.</span></span> <span data-ttu-id="5e1cd-112">El lector asigna los números de salida a las secuencias del archivo cuando se abre el archivo.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-112">The reader assigns output numbers to the streams in the file when the file is opened.</span></span> <span data-ttu-id="5e1cd-113">Normalmente, hay una salida para cada flujo en un archivo.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-113">Normally there is one output for each stream in a file.</span></span> <span data-ttu-id="5e1cd-114">Sin embargo, si el archivo usa la exclusión mutua, se asigna un único número de salida a cada grupo de flujos mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-114">If the file uses mutual exclusion, however, each group of mutually exclusive streams is assigned a single output number.</span></span> <span data-ttu-id="5e1cd-115">La secuencia que se corresponde con el número de salida de las secuencias mutuamente excluyente viene determinada por el lector, en el caso de varios archivos de velocidad de bits (MBR) o por la aplicación, si se usa la selección de flujo manual.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-115">The stream that corresponds to the output number of the mutually exclusive streams is determined either by the reader, in the case of multiple bit rate (MBR) files, or by your application, if you are using manual stream selection.</span></span>

<span data-ttu-id="5e1cd-116">Dado que el nombre de conexión establecido en el perfil no se conserva en el archivo, el lector crea un nombre de conexión predeterminado para cada salida que es simplemente una representación de cadena del número de salida, por ejemplo, "1", "2", "3", etc.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-116">Because the connection name set in the profile is not persisted in the file, the reader creates a default connection name for each output that is simply a string representation of the output number, for example "1", "2", "3" and so on.</span></span> <span data-ttu-id="5e1cd-117">Los nombres de conexión permiten a las aplicaciones y al propio lector correlacionar las salidas con las secuencias.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-117">The connection names enable applications, and the reader itself, to correlate outputs to streams.</span></span> <span data-ttu-id="5e1cd-118">En un archivo de velocidad de bits múltiple, varios flujos comparten un nombre de conexión.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-118">In a multiple bit rate file, several streams share a connection name.</span></span> <span data-ttu-id="5e1cd-119">Esto no importa al lector, porque las propiedades de salida de cada flujo MBR son idénticas.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-119">This does not matter to the reader, because the output properties for each MBR stream are identical.</span></span>

<span data-ttu-id="5e1cd-120">Cada salida tiene uno o más formatos de salida admitidos.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-120">Each output has one or more supported output formats.</span></span> <span data-ttu-id="5e1cd-121">Un formato de salida es el formato que usan los ejemplos sin comprimir proporcionados por el lector.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-121">An output format is the format that the uncompressed samples delivered by the reader use.</span></span> <span data-ttu-id="5e1cd-122">Cuando el lector abre un archivo, establece el formato de cada salida en el valor predeterminado para el subtipo de medio.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-122">When the reader opens a file, it sets the format of each output to the default for the media subtype.</span></span> <span data-ttu-id="5e1cd-123">El número y el tipo de formatos de salida admitidos viene determinado por el códec que descomprime los datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-123">The number and type of output formats supported is determined by the codec that decompresses the media data.</span></span>

<span data-ttu-id="5e1cd-124">En los temas siguientes se explica cómo trabajar con resultados:</span><span class="sxs-lookup"><span data-stu-id="5e1cd-124">The following topics explain how to work with outputs:</span></span>

-   [<span data-ttu-id="5e1cd-125">Para identificar los números de salida</span><span class="sxs-lookup"><span data-stu-id="5e1cd-125">To Identify Output Numbers</span></span>](to-identify-output-numbers.md)
-   [<span data-ttu-id="5e1cd-126">Asignar formatos de salida</span><span class="sxs-lookup"><span data-stu-id="5e1cd-126">Assigning Output Formats</span></span>](assigning-output-formats.md)

## <a name="related-topics"></a><span data-ttu-id="5e1cd-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e1cd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e1cd-128">**Interfaz IWMReader**</span><span class="sxs-lookup"><span data-stu-id="5e1cd-128">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="5e1cd-129">**Interfaz IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="5e1cd-129">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="5e1cd-130">**Leer archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="5e1cd-130">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




