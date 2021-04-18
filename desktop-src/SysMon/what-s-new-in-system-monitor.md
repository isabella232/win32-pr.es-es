---
title: Novedades del monitor de sistema
description: En la tabla siguiente se identifican las novedades de cada versión del monitor de sistema (SYSMON).
ms.assetid: 9cb0e0db-0933-4993-a995-74a36a24eccb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3662e83954630232e3fe30c26a3f6d94aa9cc7
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/26/2020
ms.locfileid: "104420378"
---
# <a name="whats-new-in-system-monitor"></a><span data-ttu-id="2fa1f-103">Novedades del monitor de sistema</span><span class="sxs-lookup"><span data-stu-id="2fa1f-103">What's New in System Monitor</span></span>

<span data-ttu-id="2fa1f-104">En la tabla siguiente se identifican las novedades de cada versión del monitor de sistema (SYSMON).</span><span class="sxs-lookup"><span data-stu-id="2fa1f-104">The following table identifies what is new for each release of System Monitor (SYSMON).</span></span>



| <span data-ttu-id="2fa1f-105">Versión</span><span class="sxs-lookup"><span data-stu-id="2fa1f-105">Version</span></span>     | <span data-ttu-id="2fa1f-106">Descripción de las características</span><span class="sxs-lookup"><span data-stu-id="2fa1f-106">Description of features</span></span>                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa1f-107">Versión 3.7</span><span class="sxs-lookup"><span data-stu-id="2fa1f-107">Version 3.7</span></span> | <span data-ttu-id="2fa1f-108">Esta versión agrega nuevos tipos de gráficos, la capacidad de seleccionar varios contadores, recuperar valores de contadores de un punto del gráfico, guardar valores de contadores en un archivo de registro y la opción de hacer que un gráfico de líneas se desplace continuamente en la ventana del gráfico en lugar de ajustarse a sí mismo. Incluido en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-108">This version adds new graph types, the ability to select multiple counters, retrieve counter values from a point on the graph, save graphed counter values to a log file, and the option to have a line graph continuously scroll in the graph window instead of wrap-around on itself.Included in Windows Server 2008 and Windows Vista.</span></span><br/> |



 

## <a name="version-37"></a><span data-ttu-id="2fa1f-109">Versión 3.7</span><span class="sxs-lookup"><span data-stu-id="2fa1f-109">Version 3.7</span></span>

<span data-ttu-id="2fa1f-110">Nuevas propiedades y métodos que se agregaron a un [**objeto de contraelemento**](counteritem.md).</span><span class="sxs-lookup"><span data-stu-id="2fa1f-110">New properties and methods that were added to [**CounterItem**](counteritem.md).</span></span>

-   [<span data-ttu-id="2fa1f-111">**GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-111">**GetDataAt**</span></span>](counteritem-getdataat.md)
-   [<span data-ttu-id="2fa1f-112">**Seleccionado**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-112">**Selected**</span></span>](counteritem-selected.md)
-   [<span data-ttu-id="2fa1f-113">**Visible**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-113">**Visible**</span></span>](counteritem-visible.md)
-   <span data-ttu-id="2fa1f-114">Rango de valores válidos modificados para el valor de [ **peritem. width**](counteritem-width.md)</span><span class="sxs-lookup"><span data-stu-id="2fa1f-114">Range of valid values changed for [**CounterItem.Width**](counteritem-width.md)</span></span>

<span data-ttu-id="2fa1f-115">Nuevas propiedades y métodos que se agregaron a [**SystemMonitor**](systemmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="2fa1f-115">New properties and methods that were added to [**SystemMonitor**](systemmonitor.md).</span></span>

-   [<span data-ttu-id="2fa1f-116">**BatchingLock**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-116">**BatchingLock**</span></span>](systemmonitor-batchinglock.md)
-   [<span data-ttu-id="2fa1f-117">**ChartScroll**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-117">**ChartScroll**</span></span>](systemmonitor-chartscroll.md)
-   [<span data-ttu-id="2fa1f-118">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-118">**ClearData**</span></span>](systemmonitor-cleardata.md)
-   [<span data-ttu-id="2fa1f-119">**DataPointCount**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-119">**DataPointCount**</span></span>](systemmonitor-datapointcount.md)
-   [<span data-ttu-id="2fa1f-120">**EnableDigitGrouping**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-120">**EnableDigitGrouping**</span></span>](systemmonitor-enabledigitgrouping.md)
-   [<span data-ttu-id="2fa1f-121">**EnableToolTips**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-121">**EnableToolTips**</span></span>](systemmonitor-enabletooltips.md)
-   [<span data-ttu-id="2fa1f-122">**GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-122">**GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
-   [<span data-ttu-id="2fa1f-123">**LoadSettings**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-123">**LoadSettings**</span></span>](systemmonitor-loadsettings.md)
-   [<span data-ttu-id="2fa1f-124">**LogSourceStartTime**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-124">**LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
-   [<span data-ttu-id="2fa1f-125">**LogSourceStopTime**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-125">**LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
-   [<span data-ttu-id="2fa1f-126">**Registrar**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-126">**Relog**</span></span>](systemmonitor-relog.md)
-   [<span data-ttu-id="2fa1f-127">**SaveAs**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-127">**SaveAs**</span></span>](systemmonitor-saveas.md)
-   [<span data-ttu-id="2fa1f-128">**ScaleToFit**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-128">**ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
-   [<span data-ttu-id="2fa1f-129">**SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-129">**SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
-   [<span data-ttu-id="2fa1f-130">**ShowTimeAxisLables**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-130">**ShowTimeAxisLables**</span></span>](systemmonitor-showtimeaxislabels.md)

<span data-ttu-id="2fa1f-131">Nuevas enumeraciones que se agregaron.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-131">New enumerations that were added.</span></span>

-   [<span data-ttu-id="2fa1f-132">**SysmonDataType**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-132">**SysmonDataType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)
-   [<span data-ttu-id="2fa1f-133">**SysmonFileType**</span><span class="sxs-lookup"><span data-stu-id="2fa1f-133">**SysmonFileType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)
-   <span data-ttu-id="2fa1f-134">Se agregaron nuevos valores de tipo de presentación a [ **DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span><span class="sxs-lookup"><span data-stu-id="2fa1f-134">New display type values were added to [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span></span>

 

 





