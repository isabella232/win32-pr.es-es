---
description: La \_ fórmula de tipo de contador varianza de cooker proporciona variabilidad que se usa para caracterizar la dispersión para un conjunto de observaciones sin formato de una propiedad en una instancia de PerfRawData de Win32 \_ .
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f9de6c5241ccd486e4da76864139e3e54f5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082450"
---
# <a name="cooker_variance"></a><span data-ttu-id="00ac4-103">varianza de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="00ac4-103">COOKER\_VARIANCE</span></span>

<span data-ttu-id="00ac4-104">La \_ fórmula de tipo de contador varianza de cooker proporciona variabilidad que se usa para caracterizar la dispersión para un conjunto de observaciones sin formato de una propiedad en una instancia de [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="00ac4-104">The COOKER\_VARIANCE counter type formula provides variability that use to characterize dispersion for a set of raw observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) instance.</span></span> <span data-ttu-id="00ac4-105">La varianza se calcula dividiendo la suma del cuadrado de la desviación de la media de cada contador entre el número de contadores.</span><span class="sxs-lookup"><span data-stu-id="00ac4-105">The variance is calculated by dividing the sum of the square of the deviation from the mean of each counter by the number of counters.</span></span> <span data-ttu-id="00ac4-106">En otras palabras, la varianza es el promedio de las desviaciones cuadradas de la media de cada contador.</span><span class="sxs-lookup"><span data-stu-id="00ac4-106">In other words, the variance is the average of the squared deviations from the mean for each counter.</span></span> <span data-ttu-id="00ac4-107">Este tipo de contador solo se define en WMI y no está disponible para las tecnologías de supervisión de rendimiento, como los [contadores de rendimiento versión 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="00ac4-107">This counter type is defined only within WMI, and it is not available to the performance monitoring technologies, such as [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="00ac4-108">Para obtener más información sobre la fórmula de tipo de contador, vea [tipos de contadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="00ac4-108">For more information about the counter type formula, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>

<span data-ttu-id="00ac4-109">Para obtener más información sobre los proveedores y scripts de alto rendimiento, consulte [tipos de contadores de rendimiento de WMI](wmi-performance-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="00ac4-109">For more information about high-performance providers and scripting, see [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="00ac4-110">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="00ac4-110">Example Code</span></span>

<span data-ttu-id="00ac4-111">Para obtener ejemplos de código, vea [obtener datos de rendimiento estadísticos](obtaining-statistical-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="00ac4-111">For code examples, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00ac4-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00ac4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00ac4-113">Tipos de contadores estadísticos</span><span class="sxs-lookup"><span data-stu-id="00ac4-113">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> <dt>

[<span data-ttu-id="00ac4-114">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="00ac4-114">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
