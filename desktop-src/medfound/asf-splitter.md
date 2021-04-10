---
description: Divisor ASF
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: Divisor ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153689"
---
# <a name="asf-splitter"></a><span data-ttu-id="7e355-103">Divisor ASF</span><span class="sxs-lookup"><span data-stu-id="7e355-103">ASF Splitter</span></span>

<span data-ttu-id="7e355-104">El objeto de *separador* ASF es un componente de nivel WMContainer que analiza el objeto de datos ASF de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="7e355-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="7e355-105">Puede usar el divisor para leer los paquetes de datos en el objeto de datos y generar ejemplos de secuencias.</span><span class="sxs-lookup"><span data-stu-id="7e355-105">You can use the splitter to read the data packets in the Data Object and generate stream samples.</span></span> <span data-ttu-id="7e355-106">Para obtener información acerca de la estructura de un archivo ASF, consulte [ASF File Structure](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="7e355-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="7e355-107">El divisor expone la interfaz [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="7e355-107">The splitter exposes the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span> <span data-ttu-id="7e355-108">El divisor analiza los paquetes de datos ASF de las secuencias seleccionadas y los vuelve a empaquetar en objetos de ejemplo individuales que exponen la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="7e355-108">The splitter parses ASF data packets for the selected streams and repackages them into individual sample objects that expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="7e355-109">El divisor es uno de los componentes de nivel de plataforma de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7e355-109">The splitter is one of the platform-level components of Media Foundation.</span></span> <span data-ttu-id="7e355-110">El origen de medios ASF usa el divisor internamente para analizar archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="7e355-110">The ASF media source uses the splitter internally to parse ASF files.</span></span>

<span data-ttu-id="7e355-111">En el siguiente diagrama se ilustra la generación de muestras para un archivo ASF a través del divisor.</span><span class="sxs-lookup"><span data-stu-id="7e355-111">The following diagram illustrates sample generation for an ASF file through the splitter.</span></span>

![diagrama que muestra la generación de ejemplo de un archivo ASF](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

<span data-ttu-id="7e355-113">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="7e355-113">This section contains the following topics:</span></span>



| <span data-ttu-id="7e355-114">Tema</span><span class="sxs-lookup"><span data-stu-id="7e355-114">Topic</span></span>                                                                                                                        | <span data-ttu-id="7e355-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e355-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="7e355-116">Crear el objeto divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="7e355-116">Creating the ASF Splitter Object</span></span>](creating-the-asf-splitter-object.md)                                                     | <span data-ttu-id="7e355-117">Cómo crear e inicializar el divisor.</span><span class="sxs-lookup"><span data-stu-id="7e355-117">How to create and initialize the splitter.</span></span>                              |
| [<span data-ttu-id="7e355-118">Configurar el objeto divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="7e355-118">Configuring the ASF Splitter Object</span></span>](configuring-the-asf-splitter-object.md)                                               | <span data-ttu-id="7e355-119">Opciones de configuración para el divisor.</span><span class="sxs-lookup"><span data-stu-id="7e355-119">Configuration settings for the splitter.</span></span>                                |
| [<span data-ttu-id="7e355-120">Generar ejemplos de secuencia a partir de un objeto de datos ASF existente</span><span class="sxs-lookup"><span data-stu-id="7e355-120">Generating Stream Samples from an Existing ASF Data Object</span></span>](generating-stream-samples-from-an-existing-asf-data-object.md) | <span data-ttu-id="7e355-121">Cómo analizar el objeto de datos ASF y generar muestras de vapor de paquetes.</span><span class="sxs-lookup"><span data-stu-id="7e355-121">How to parse the ASF Data Object and generate packetized steam samples.</span></span> |



 

<span data-ttu-id="7e355-122">En la tabla siguiente se muestran los atributos de objeto de datos pertinentes.</span><span class="sxs-lookup"><span data-stu-id="7e355-122">The following table shows the relevant Data Object attributes.</span></span>



| <span data-ttu-id="7e355-123">Atributo</span><span class="sxs-lookup"><span data-stu-id="7e355-123">Attribute</span></span>                                                                                                    | <span data-ttu-id="7e355-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e355-124">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e355-125">**\_ \_ \_ paquetes FILEPROPERTIES MF de \_ ASF**</span><span class="sxs-lookup"><span data-stu-id="7e355-125">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)                   | <span data-ttu-id="7e355-126">Número de paquetes de datos en el objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="7e355-126">Number of data packets in the ASF Data Object.</span></span>                                                       |
| [<span data-ttu-id="7e355-127">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ min \_ Packet \_ size**</span><span class="sxs-lookup"><span data-stu-id="7e355-127">**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | <span data-ttu-id="7e355-128">Tamaño mínimo de los paquetes de datos en el archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="7e355-128">Minimum size of the data packets in the file, in bytes.</span></span>                                              |
| [<span data-ttu-id="7e355-129">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ tamaño máximo de \_ paquete \_**</span><span class="sxs-lookup"><span data-stu-id="7e355-129">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | <span data-ttu-id="7e355-130">Tamaño máximo de los paquetes de datos en el archivo, en bytes</span><span class="sxs-lookup"><span data-stu-id="7e355-130">Maximum size of the data packets in the file, in bytes</span></span>                                               |
| [<span data-ttu-id="7e355-131">**\_longitud de \_ \_ datos ASF \_ de MF PD**</span><span class="sxs-lookup"><span data-stu-id="7e355-131">**MF\_PD\_ASF\_DATA\_LENGTH**</span></span>](mf-pd-asf-data-length-attribute.md)                                         | <span data-ttu-id="7e355-132">Tamaño del objeto de datos ASF, en bytes.</span><span class="sxs-lookup"><span data-stu-id="7e355-132">Size of the ASF Data Object, in bytes.</span></span>                                                               |
| [<span data-ttu-id="7e355-133">**\_desplazamiento de \_ \_ Inicio de datos ASF \_ \_ de MF PD**</span><span class="sxs-lookup"><span data-stu-id="7e355-133">**MF\_PD\_ASF\_DATA\_START\_OFFSET**</span></span>](mf-pd-asf-data-start-offset-attribute.md)                            | <span data-ttu-id="7e355-134">Desplazamiento, en bytes, al primer paquete de datos del objeto de datos ASF relativo al inicio del archivo.</span><span class="sxs-lookup"><span data-stu-id="7e355-134">Offset, in bytes, to the first data packet in the ASF Data Object relative to the start of the file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7e355-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e355-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e355-136">Componentes de WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="7e355-136">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="7e355-137">Tutorial: lectura de un archivo ASF</span><span class="sxs-lookup"><span data-stu-id="7e355-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="7e355-138">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e355-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



