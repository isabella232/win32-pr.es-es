---
description: Para consumir datos de contadores, vea consumir datos de contador.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Uso de contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: abc055a34f0937e056d1d983354fc0a3edf182a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667238"
---
# <a name="using-performance-counters"></a><span data-ttu-id="c13a1-103">Uso de contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="c13a1-103">Using Performance Counters</span></span>

<span data-ttu-id="c13a1-104">Los **consumidores** del contador de rendimiento son componentes de software que recopilan y utilizan los datos del contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c13a1-104">Performance counter **consumers** are software components that collect and make use of performance counter data.</span></span> <span data-ttu-id="c13a1-105">Los consumidores de ejemplo proporcionados por Microsoft incluyen monitor de rendimiento (perfmon.exe), Monitor de recursos (resmon.exe), administrador de registros (logman.exe) y typeperf.exe.</span><span class="sxs-lookup"><span data-stu-id="c13a1-105">Example consumers provided by Microsoft include Performance Monitor (perfmon.exe), Resource Monitor (resmon.exe), Log Manager (logman.exe) and typeperf.exe.</span></span> <span data-ttu-id="c13a1-106">Los componentes de software de terceros también pueden recopilar datos de rendimiento a través de las API de recopilación de rendimiento o a través de clases de contador de rendimiento de WMI.</span><span class="sxs-lookup"><span data-stu-id="c13a1-106">Third-party software components may also collect performance data via performance collection APIs or via WMI performance counter classes.</span></span>

<span data-ttu-id="c13a1-107">Los **proveedores** de contadores de rendimiento son componentes de software que publican datos de contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c13a1-107">Performance counter **providers** are software components that publish performance counter data.</span></span> <span data-ttu-id="c13a1-108">Los componentes del sistema operativo, los controladores de dispositivo y los servicios pueden proporcionar los contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c13a1-108">Performance counters can be provided by operating system components, device drivers, and services.</span></span> <span data-ttu-id="c13a1-109">Muchos contadores de rendimiento se proporcionan como parte del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="c13a1-109">Many performance counters are provided as part of the Windows operating system.</span></span> <span data-ttu-id="c13a1-110">Los componentes de software de terceros pueden proporcionar contadores adicionales a través de las API del proveedor de contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c13a1-110">Additional counters may be provided by third-party software components via the performance counter provider APIs.</span></span>

- <span data-ttu-id="c13a1-111">Use [las herramientas del contador de rendimiento](performance-counters-tools.md) si desea recopilar o ver los datos del contador de un sistema.</span><span class="sxs-lookup"><span data-stu-id="c13a1-111">Use [Performance Counter Tools](performance-counters-tools.md) when you want to collect or view the counter data from a system.</span></span>
- <span data-ttu-id="c13a1-112">Use las [API del consumidor del contador de rendimiento](consuming-counter-data.md) cuando desee escribir un programa que recopile datos del contador del sistema local.</span><span class="sxs-lookup"><span data-stu-id="c13a1-112">Use [Performance Counter Consumer APIs](consuming-counter-data.md) when you want to write a program that collects counter data from the local system.</span></span>
- <span data-ttu-id="c13a1-113">Use [clases de contador de rendimiento de WMI](/windows/desktop/WmiSdk/monitoring-performance-data) si desea recopilar datos de contadores de un sistema local o remoto mediante WMI.</span><span class="sxs-lookup"><span data-stu-id="c13a1-113">Use [WMI Performance Counter Classes](/windows/desktop/WmiSdk/monitoring-performance-data) when you want to collect counter data from a local or remote system using WMI.</span></span>
- <span data-ttu-id="c13a1-114">Use las [API de proveedor de contador de rendimiento](providing-counter-data.md) cuando desee publicar datos de contadores de rendimiento del componente de software.</span><span class="sxs-lookup"><span data-stu-id="c13a1-114">Use [Performance Counter Provider APIs](providing-counter-data.md) when you want to publish performance counter data from your software component.</span></span>

## <a name="see-also"></a><span data-ttu-id="c13a1-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="c13a1-115">See also</span></span>

[<span data-ttu-id="c13a1-116">Acerca de los contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="c13a1-116">About Performance Counters</span></span>](about-performance-counters.md)

[<span data-ttu-id="c13a1-117">Referencia de contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="c13a1-117">Performance Counters Reference</span></span>](performance-counters-reference.md)
