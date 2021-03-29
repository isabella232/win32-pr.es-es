---
title: Para buscar por tiempo mediante el lector sincrónico
description: Para buscar por tiempo mediante el lector sincrónico
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Advanced Systems Format (ASF), búsqueda por tiempo
- ASF (formato de sistemas avanzados), búsqueda por hora
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores sincrónicos, búsquedas por tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788811"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a><span data-ttu-id="8287a-108">Para buscar por tiempo mediante el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="8287a-108">To Seek By Time Using the Synchronous Reader</span></span>

<span data-ttu-id="8287a-109">Para buscar datos mediante el lector sincrónico, especifique un intervalo para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="8287a-109">To seek for data using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="8287a-110">Un intervalo se define mediante un tiempo de presentación inicial y una duración, ambos en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="8287a-110">A range is defined by a starting presentation time and a duration, both in 100-nanosecond units.</span></span>

<span data-ttu-id="8287a-111">Para buscar datos en un archivo ASF por tiempo de presentación mediante el lector sincrónico, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="8287a-111">To seek data in an ASF file by presentation time using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="8287a-112">Especifique una hora de inicio y una duración para la entrega de ejemplo llamando a [**IWMSyncReader:: SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange).</span><span class="sxs-lookup"><span data-stu-id="8287a-112">Specify a starting time and duration for sample delivery by calling [**IWMSyncReader::SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange).</span></span> <span data-ttu-id="8287a-113">Este método no requiere que se especifique un número de secuencia porque los tiempos de presentación de cada flujo ya deben estar sincronizados.</span><span class="sxs-lookup"><span data-stu-id="8287a-113">This method does not require you to specify a stream number because the presentation times of each stream should already be synchronized.</span></span>
2.  <span data-ttu-id="8287a-114">Comience a recuperar ejemplos con llamadas a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="8287a-114">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="8287a-115">Continúe como lo haría normalmente con el lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="8287a-115">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8287a-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8287a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8287a-117">**Interfaz IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="8287a-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="8287a-118">**Leer archivos con el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="8287a-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




