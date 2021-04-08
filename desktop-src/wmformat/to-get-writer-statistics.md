---
title: Para obtener estadísticas del escritor
description: Para obtener estadísticas del escritor
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Advanced Systems Format (ASF), estadísticas del escritor
- ASF (formato de sistemas avanzados), estadísticas del escritor
- Estadísticas del escritor, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103995024"
---
# <a name="to-get-writer-statistics"></a><span data-ttu-id="3a929-106">Para obtener estadísticas del escritor</span><span class="sxs-lookup"><span data-stu-id="3a929-106">To Get Writer Statistics</span></span>

<span data-ttu-id="3a929-107">El escritor puede proporcionar información estadística acerca de las operaciones de escritura.</span><span class="sxs-lookup"><span data-stu-id="3a929-107">The writer can provide statistical information about writing operations.</span></span> <span data-ttu-id="3a929-108">Hay dos métodos para recopilar estadísticas del escritor: [**IWMWriterAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) y [**IWMWriterAdvanced3:: GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span><span class="sxs-lookup"><span data-stu-id="3a929-108">There are two methods for gathering writer statistics: [**IWMWriterAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) and [**IWMWriterAdvanced3::GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span></span> <span data-ttu-id="3a929-109">La información recuperada por **GetStatisticsEx** es más específica que la información recuperada por **GetStatistics**.</span><span class="sxs-lookup"><span data-stu-id="3a929-109">The information retrieved by **GetStatisticsEx** is more specific than the information retrieved by **GetStatistics**.</span></span>

<span data-ttu-id="3a929-110">Ambos métodos rellenan las estructuras con información estadística.</span><span class="sxs-lookup"><span data-stu-id="3a929-110">Both methods populate structures with statistical information.</span></span> <span data-ttu-id="3a929-111">**GetStatistics** usa la estructura de [**\_ \_ estadísticas del escritor de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) y **GetStatisticsEx** usa la estructura de estadísticas del [**escritor de WM \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) .</span><span class="sxs-lookup"><span data-stu-id="3a929-111">**GetStatistics** uses the [**WM\_WRITER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) structure, and **GetStatisticsEx** uses the [**WM\_WRITER\_STATISTICS\_EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) structure.</span></span> <span data-ttu-id="3a929-112">**GetStatisticsEx** no duplica los datos obtenidos por **GetStatistics**.</span><span class="sxs-lookup"><span data-stu-id="3a929-112">**GetStatisticsEx** does not duplicate the data obtained by **GetStatistics**.</span></span> <span data-ttu-id="3a929-113">Para obtener la información más completa, debe llamar a ambos métodos.</span><span class="sxs-lookup"><span data-stu-id="3a929-113">For the most complete information, you should call both methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a929-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a929-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a929-115">**Interfaz IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="3a929-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="3a929-116">**Interfaz IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="3a929-116">**IWMWriterAdvanced3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[<span data-ttu-id="3a929-117">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="3a929-117">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




