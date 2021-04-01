---
description: Ventajas del streaming multimedia
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Ventajas del streaming multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd907d9b8e91cb61709479a2d600323d6d420958
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157004"
---
# <a name="advantages-of-multimedia-streaming"></a><span data-ttu-id="2b8ae-103">Ventajas del streaming multimedia</span><span class="sxs-lookup"><span data-stu-id="2b8ae-103">Advantages of Multimedia Streaming</span></span>

> [!Note]  
> <span data-ttu-id="2b8ae-104">Estas API están en desuso.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-104">These APIs are deprecated.</span></span> <span data-ttu-id="2b8ae-105">Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="2b8ae-106">Cuando los desarrolladores usan el streaming multimedia en sus aplicaciones, reduce en gran medida la cantidad de programación específica de formato necesaria.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-106">When developers use multimedia streaming in their applications, it greatly reduces the amount of format-specific programming needed.</span></span> <span data-ttu-id="2b8ae-107">Normalmente, una aplicación que debe obtener datos de medios de un origen de archivos o hardware debe saber todo lo relacionado con el formato de datos y el dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-107">Typically, an application that must obtain media data from a file or hardware source must know everything about the data format and the hardware device.</span></span> <span data-ttu-id="2b8ae-108">La aplicación debe controlar la conexión, la transferencia de datos, cualquier conversión de datos necesaria y la representación de datos real o el almacenamiento de archivos.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-108">The application must handle the connection, transfer of data, any necessary data conversion, and the actual data rendering or file storage.</span></span> <span data-ttu-id="2b8ae-109">Dado que cada formato y dispositivo son ligeramente diferentes, este proceso suele ser complejo y engorroso.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-109">Because each format and device is slightly different, this process is often complex and cumbersome.</span></span> <span data-ttu-id="2b8ae-110">Por otro lado, el streaming multimedia negocia automáticamente la transferencia y la conversión de los datos desde el origen a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-110">Multimedia streaming, on the other hand, automatically negotiates the transfer and conversion of data from the source to the application.</span></span> <span data-ttu-id="2b8ae-111">Las interfaces de streaming proporcionan un método uniforme y predecible de acceso y control de los datos, lo que facilita que una aplicación pueda reproducir los datos, independientemente de su origen o formato original.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-111">The streaming interfaces provide a uniform and predictable method of data access and control, which makes it easy for an application to play back the data, regardless of its original source or format.</span></span>

<span data-ttu-id="2b8ae-112">En los pasos siguientes se muestra cómo implementar el streaming, desde el dispositivo de hardware hasta la reproducción representada.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-112">The following steps show how to implement streaming, from hardware device to rendered playback.</span></span>

1.  <span data-ttu-id="2b8ae-113">Un origen de datos de vídeo, como DirectShow, expone las interfaces de streaming.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-113">A source of video data, such as DirectShow, exposes the streaming interfaces.</span></span>
2.  <span data-ttu-id="2b8ae-114">El desarrollador de aplicaciones utiliza las interfaces de streaming multimedia para controlar la conversión del formato de datos.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-114">The application developer uses the multimedia streaming interfaces to handle data format conversion.</span></span>
3.  <span data-ttu-id="2b8ae-115">El desarrollador de aplicaciones utiliza las interfaces de DirectDraw para representar los datos resultantes.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-115">The application developer uses the DirectDraw interfaces to render the resulting data.</span></span>

<span data-ttu-id="2b8ae-116">La especificación de secuencias multimedia incluye varias interfaces; cada interfaz incluye métodos que controlan un aspecto determinado del proceso de streaming o controlan un determinado tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-116">The specification for multimedia streams comprises several interfaces; each interface includes methods that control a certain aspect of the streaming process or handle a certain type of data.</span></span> <span data-ttu-id="2b8ae-117">Consulte la [lista de interfaces de streaming multimedia](list-of-multimedia-streaming-interfaces.md) para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="2b8ae-117">See [List of Multimedia Streaming Interfaces](list-of-multimedia-streaming-interfaces.md) for additional information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b8ae-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b8ae-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b8ae-119">Acerca de la arquitectura de streaming multimedia</span><span class="sxs-lookup"><span data-stu-id="2b8ae-119">About the Multimedia Streaming Architecture</span></span>](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



