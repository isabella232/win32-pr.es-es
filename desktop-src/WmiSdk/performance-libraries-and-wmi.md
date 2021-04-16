---
description: El proveedor WMIPerfClass y el proveedor WMIPerfInst proporcionan dinámicamente datos de contador de rendimiento para las clases de contador de rendimiento de WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Bibliotecas de rendimiento y WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705881"
---
# <a name="performance-libraries-and-wmi"></a><span data-ttu-id="8f050-103">Bibliotecas de rendimiento y WMI</span><span class="sxs-lookup"><span data-stu-id="8f050-103">Performance Libraries and WMI</span></span>

<span data-ttu-id="8f050-104">El [proveedor WMIPerfClass](wmiperfclass-provider.md) y el [proveedor WMIPerfInst](wmiperfinst-provider.md) proporcionan dinámicamente datos de contador de rendimiento para las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)de WMI.</span><span class="sxs-lookup"><span data-stu-id="8f050-104">The [WMIPerfClass Provider](wmiperfclass-provider.md) and the [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provide performance counter data for the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span>

## <a name="wmiperfclass-and-wmiperfinst-providers"></a><span data-ttu-id="8f050-105">Proveedores de WMIPerfClass y WMIPerfInst</span><span class="sxs-lookup"><span data-stu-id="8f050-105">WMIPerfClass and WMIPerfInst Providers</span></span>

<span data-ttu-id="8f050-106">El [proveedor WMIPerfClass](wmiperfclass-provider.md) crea [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI en la inicialización del sistema.</span><span class="sxs-lookup"><span data-stu-id="8f050-106">[WMIPerfClass Provider](wmiperfclass-provider.md) creates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) at system initialization.</span></span> <span data-ttu-id="8f050-107">El [proveedor WMIPerfInst](wmiperfinst-provider.md) proporciona dinámicamente datos de contadores de rendimiento para estas clases.</span><span class="sxs-lookup"><span data-stu-id="8f050-107">The [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provides performance counter data for these classes.</span></span> <span data-ttu-id="8f050-108">El proveedor del proveedor WMIPerfClass proporciona clases para los [contadores de rendimiento](/windows/desktop/PerfCtrs/performance-counters-portal)de la versión 1 y la versión 2.</span><span class="sxs-lookup"><span data-stu-id="8f050-108">The WMIPerfClass Provider provider supplies classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="8f050-109">Los contadores de la versión 1 se encuentran en el registro en **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**.</span><span class="sxs-lookup"><span data-stu-id="8f050-109">Version 1 counters are found in the registry under **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services**.</span></span> <span data-ttu-id="8f050-110">Los servicios que proporcionan los datos de rendimiento tienen una subclave de **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="8f050-110">Services that provide performance data have a **Performance** subkey.</span></span> <span data-ttu-id="8f050-111">Las clases de rendimiento de WMI creadas a partir de contadores de la versión 1 no tienen "contadores" como parte de su nombre.</span><span class="sxs-lookup"><span data-stu-id="8f050-111">WMI performance classes created from version 1 counters do not have "Counters" as part of their name.</span></span>

<span data-ttu-id="8f050-112">El **GUID** que identifica un proveedor de contador de rendimiento de la versión 2 se encuentra en el registro en **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.</span><span class="sxs-lookup"><span data-stu-id="8f050-112">The **GUID** s identifying a version 2 performance counter provider are found in the registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib\\\_V2Providers**.</span></span>

<span data-ttu-id="8f050-113">WMIPerfClass se registra como un proveedor de clases WMI normal.</span><span class="sxs-lookup"><span data-stu-id="8f050-113">WMIPerfClass is registered as a normal WMI class provider.</span></span> <span data-ttu-id="8f050-114">WMIPerfInst es un proveedor de instancias de WMI que proporciona datos del ayudante de datos de rendimiento (PDH) para los contadores de la versión 1 y la versión 2.</span><span class="sxs-lookup"><span data-stu-id="8f050-114">WMIPerfInst is a WMI instance provider that supplies data from Performance Data Helper (PDH) for both version 1 and version 2 counters.</span></span> <span data-ttu-id="8f050-115">Para obtener más información, vea [usar las funciones de PDH para consumir datos de contador](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span><span class="sxs-lookup"><span data-stu-id="8f050-115">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f050-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f050-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f050-117">Acerca de WMI</span><span class="sxs-lookup"><span data-stu-id="8f050-117">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="8f050-118">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="8f050-118">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
