---
description: Multiplexor ASF
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: Multiplexor ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080335"
---
# <a name="asf-multiplexer"></a><span data-ttu-id="e74a6-103">Multiplexor ASF</span><span class="sxs-lookup"><span data-stu-id="e74a6-103">ASF Multiplexer</span></span>

<span data-ttu-id="e74a6-104">El *multiplexor* de ASF es un objeto de capa WMContainer que funciona con el [objeto de datos ASF](asf-file-structure.md) y proporciona a una aplicación la capacidad de generar paquetes de datos para un contenedor ASF.</span><span class="sxs-lookup"><span data-stu-id="e74a6-104">The ASF *multiplexer* is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate data packets for an ASF container.</span></span> <span data-ttu-id="e74a6-105">El multiplexor acepta los datos multimedia en forma de [muestras de medios](media-samples.md) y genera ejemplos de medios basados en los parámetros de paquetes ASF y de transmisión por secuencias definidos en el [objeto de encabezado ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e74a6-105">The multiplexer accepts media data in the form of [Media Samples](media-samples.md) and outputs media samples based on streaming and ASF packet parameters defined in the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="e74a6-106">Los ejemplos de medios de salida contienen referencias a uno o varios búferes multimedia que contienen datos de medios digitales con paquetes. Puede usar este objeto en un escenario de codificación de archivos en el que reciba ejemplos de secuencias codificadas del codificador o para la transcodificación ASF-ASF (remuxing).</span><span class="sxs-lookup"><span data-stu-id="e74a6-106">The output media samples hold references to one or more media buffers that contain packetized digital media data.You can use this object in a file encoding scenario where it receives encoded stream samples from the encoder or for ASF-ASF transcoding (remuxing).</span></span>

<span data-ttu-id="e74a6-107">En el diagrama siguiente se ilustra la generación de paquetes de datos ASF para un archivo ASF mediante el multiplexor.</span><span class="sxs-lookup"><span data-stu-id="e74a6-107">The following diagram illustrates ASF data packet generation for an ASF file using the multiplexer.</span></span>

![diagrama que muestra la generación de paquetes de datos ASF](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

<span data-ttu-id="e74a6-109">Para obtener información acerca de la estructura de un archivo ASF, consulte [ASF File Structure](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e74a6-109">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="e74a6-110">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="e74a6-110">This section contains the following topics:</span></span>



| <span data-ttu-id="e74a6-111">Tema</span><span class="sxs-lookup"><span data-stu-id="e74a6-111">Topic</span></span>                                                                  | <span data-ttu-id="e74a6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e74a6-112">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="e74a6-113">Crear el objeto multiplexor</span><span class="sxs-lookup"><span data-stu-id="e74a6-113">Creating the Multiplexer Object</span></span>](creating-the-multiplexer-object.md) | <span data-ttu-id="e74a6-114">Cómo crear e inicializar el multiplexor.</span><span class="sxs-lookup"><span data-stu-id="e74a6-114">How to create and initialize the multiplexer.</span></span>                     |
| [<span data-ttu-id="e74a6-115">Generación de nuevos paquetes de datos ASF</span><span class="sxs-lookup"><span data-stu-id="e74a6-115">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md) | <span data-ttu-id="e74a6-116">Cómo generar paquetes de datos para constituir un nuevo objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="e74a6-116">How to generate data packets to constitute a new ASF Data Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e74a6-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e74a6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e74a6-118">Componentes de WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="e74a6-118">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="e74a6-119">Tutorial: copiar secuencias ASF de un archivo a otro</span><span class="sxs-lookup"><span data-stu-id="e74a6-119">Tutorial: Copying ASF Streams from One File to Another</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="e74a6-120">Tutorial: escribir un archivo WMA con codificación CBR</span><span class="sxs-lookup"><span data-stu-id="e74a6-120">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



