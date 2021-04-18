---
description: Propiedades de ejemplo MPEG
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: Propiedades de ejemplo MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686361"
---
# <a name="mpeg-sample-properties"></a><span data-ttu-id="fef06-103">Propiedades de ejemplo MPEG</span><span class="sxs-lookup"><span data-stu-id="fef06-103">MPEG Sample Properties</span></span>

<span data-ttu-id="fef06-104">Los ejemplos de MPEG tienen las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="fef06-104">MPEG samples have the following characteristics.</span></span>

<span data-ttu-id="fef06-105">**Marcas de tiempo**</span><span class="sxs-lookup"><span data-stu-id="fef06-105">**Time Stamps**</span></span>

<span data-ttu-id="fef06-106">No todos los ejemplos tienen tiempos de inicio y detención.</span><span class="sxs-lookup"><span data-stu-id="fef06-106">Not all samples have start and stop times.</span></span> <span data-ttu-id="fef06-107">La hora de detención del ejemplo de los datos de paquete y carga no resulta útil; normalmente se establece en la hora de inicio más una.</span><span class="sxs-lookup"><span data-stu-id="fef06-107">The sample stop time for packet and payload data is not useful; it is usually set to the start time plus one.</span></span> <span data-ttu-id="fef06-108">Los ejemplos de datos de paquetes o carga de MPEG tendrán establecido un tiempo de inicio y detención si el paquete de nivel de sistema del que se generan tiene un valor de PTS válido.</span><span class="sxs-lookup"><span data-stu-id="fef06-108">MPEG packet or payload data samples will have a start and stop time set if the system layer packet they are generated from had a valid PTS.</span></span>

<span data-ttu-id="fef06-109">Para obtener más información acerca de las marcas de tiempo, consulte la sección 2.4.1 de ISO1-11172: "el encabezado del paquete puede contener decodificación y/o marcas de tiempo de presentación (DTS y PTS) que hacen referencia a la primera unidad de acceso del paquete".</span><span class="sxs-lookup"><span data-stu-id="fef06-109">For more information about time stamps, see section 2.4.1 of ISO1-11172: "The packet header may contain decoding and/or presentation time stamps (DTS and PTS) that refer to the first access unit in the packet."</span></span>

<span data-ttu-id="fef06-110">En el caso de los \_ tipos principales de secuencia MPEG, la hora de inicio es la posición en byte del primer byte, clasificado en 1 byte por segundo.</span><span class="sxs-lookup"><span data-stu-id="fef06-110">For MPEG\_Stream major types, the start time is the byte position of the first byte, rated at 1 byte per second.</span></span> <span data-ttu-id="fef06-111">La hora de detención es la posición en bytes del último byte.</span><span class="sxs-lookup"><span data-stu-id="fef06-111">The stop time is the byte position of the last byte.</span></span> <span data-ttu-id="fef06-112">Por lo tanto, las muestras consecutivas deben tener la hora de detención del primer paquete igual a la hora de inicio del siguiente paquete.</span><span class="sxs-lookup"><span data-stu-id="fef06-112">Thus, consecutive samples should have the stop time of the first packet equal to the start time of the next packet.</span></span> <span data-ttu-id="fef06-113">En el caso de los datos de CD de vídeo, el origen del medio debe coincidir con el formato de un archivo de CD de vídeo expuesto por CDFS con el fragmento estándar RIFF en el inicio.</span><span class="sxs-lookup"><span data-stu-id="fef06-113">For Video CD data, the origin of the medium must match the format of a video-CD file exposed by CDFS with the standard RIFF chunk at the start.</span></span>

<span data-ttu-id="fef06-114">En el caso de los tipos de paquete y carga de vídeo MPEG, la marca de tiempo es el tiempo de presentación del primer fotograma de vídeo cuyo código de inicio de imagen comienza en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fef06-114">For MPEG video packet and payload types, the time stamp is the presentation time for the first video frame whose picture start code begins in the sample.</span></span>

<span data-ttu-id="fef06-115">En el caso de los tipos de paquete y carga de audio MPEG, la marca de tiempo es el tiempo de presentación del primer fotograma de audio cuyo código de sincronización comienza en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fef06-115">For MPEG audio packet and payload types, the time stamp is the presentation time for the first audio frame whose sync code starts in the sample.</span></span>

<span data-ttu-id="fef06-116">Se supone que los filtros de control pueden realizar correctamente la reversión de los datos de carga y paquete sin marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fef06-116">It is assumed that packet and payload data without time stamps can be successfully prerolled by the handling filters.</span></span>

<span data-ttu-id="fef06-117">**Discontinuidades**</span><span class="sxs-lookup"><span data-stu-id="fef06-117">**Discontinuities**</span></span>

<span data-ttu-id="fef06-118">Si hay una interrupción en la secuencia (por ejemplo, un hueco en los datos en tiempo real o un error en los datos o después de una búsqueda), se establece la propiedad discontinuidad en el siguiente ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="fef06-118">If there is a break in the stream (for example, a gap in the real-time data, or an error in the data or after a seek), the discontinuity property is set on the next media sample.</span></span> <span data-ttu-id="fef06-119">Esto también permite una discontinuidad de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fef06-119">This also allows for a time-stamp discontinuity.</span></span>

<span data-ttu-id="fef06-120">**Notificaciones de final de secuencia**</span><span class="sxs-lookup"><span data-stu-id="fef06-120">**End-of-Stream Notifications**</span></span>

<span data-ttu-id="fef06-121">Cuando el descodificador recibe esta notificación, debe procesar todos los datos almacenados en búfer.</span><span class="sxs-lookup"><span data-stu-id="fef06-121">When the decoder receives this notification, it must process any buffered data.</span></span> <span data-ttu-id="fef06-122">Los datos nuevos deben comenzar con la propiedad discontinuidad.</span><span class="sxs-lookup"><span data-stu-id="fef06-122">Any new data must then start with the discontinuity property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fef06-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fef06-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fef06-124">Compatibilidad con MPEG-2 en DirectShow</span><span class="sxs-lookup"><span data-stu-id="fef06-124">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



