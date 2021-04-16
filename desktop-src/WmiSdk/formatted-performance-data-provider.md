---
description: Suministra calculada (&\# 0034; cocida&\# 0034;) datos de contadores de rendimiento. Proporciona datos dinámicos a las clases WMI derivadas de Win32 \_ PerfFormattedData. También se conoce como proveedor de contadores cocidos.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Proveedor de datos de rendimiento con formato
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0db075ebdafcd31c7aa0980d191ed565873f686f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706155"
---
# <a name="formatted-performance-data-provider"></a><span data-ttu-id="d454e-105">Proveedor de datos de rendimiento con formato</span><span class="sxs-lookup"><span data-stu-id="d454e-105">Formatted Performance Data Provider</span></span>

<span data-ttu-id="d454e-106">\[El proveedor de datos de rendimiento con formato, también conocido como "proveedor de contador cocido", ya no está disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="d454e-106">\[The Formatted Performance Data Provider, also known as the "Cooked Counter Provider," is no longer available for use.</span></span> <span data-ttu-id="d454e-107">En su lugar, use el proveedor [WMIPerfInst](wmiperfinst-provider.md) .\]</span><span class="sxs-lookup"><span data-stu-id="d454e-107">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="d454e-108">El proveedor de datos de rendimiento con formato de alto rendimiento proporciona datos de contadores de rendimiento calculados ("cocidos"), como el porcentaje de tiempo que un disco dedica a escribir datos.</span><span class="sxs-lookup"><span data-stu-id="d454e-108">The high-performance Formatted Performance Data provider supplies calculated ("cooked") performance counter data, such as the percentage of time a disk spends writing data.</span></span> <span data-ttu-id="d454e-109">Este proveedor proporciona datos dinámicos a las clases WMI derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="d454e-109">This provider supplies dynamic data to the WMI classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="d454e-110">La diferencia entre este proveedor y el [proveedor de contadores de rendimiento](performance-counter-provider.md) es que el proveedor de contadores de rendimiento proporciona datos sin procesar y el proveedor de contadores elaborados proporciona datos de rendimiento que aparecen exactamente como en el [*monitor de sistema*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="d454e-110">The difference between this provider and the [Performance Counter provider](performance-counter-provider.md) is that the Performance Counter provider supplies raw data and the Cooked Counter provider supplies performance data that appears exactly as in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="d454e-111">El nombre de la instancia de [**\_ \_ Win32Provider**](--win32provider.md) es "HiPerfCooker \_ v1".</span><span class="sxs-lookup"><span data-stu-id="d454e-111">The [**\_\_Win32Provider**](--win32provider.md) instance name is "HiPerfCooker\_v1".</span></span>

<span data-ttu-id="d454e-112">El nombre de clase con formato WMI para un objeto de contador tiene el formato "Win32 PerfFormattedData nombre de objeto nombre de \_ \_ *servicio \_* \_ ".*\_*</span><span class="sxs-lookup"><span data-stu-id="d454e-112">The WMI formatted class name for a counter object is of the form "Win32\_PerfFormattedData\_*service\_name*\_*object\_name*".</span></span> <span data-ttu-id="d454e-113">Por ejemplo, el nombre de clase WMI que contiene los contadores de disco lógico es **Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="d454e-113">For example, the WMI class name that contains the logical disk counters is **Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**.</span></span> <span data-ttu-id="d454e-114">Estas clases se encuentran en el espacio de \\ nombres "root CIMv2".</span><span class="sxs-lookup"><span data-stu-id="d454e-114">These classes are located in the "Root\\CIMv2" namespace.</span></span>

<span data-ttu-id="d454e-115">Dado que las clases de datos de rendimiento se agregan y modifican dinámicamente en un sistema determinado, no es posible documentar formalmente las propiedades de todos los objetos de rendimiento conocidos.</span><span class="sxs-lookup"><span data-stu-id="d454e-115">Because performance data classes are added and modified dynamically on a given system, it is not possible to formally document the properties of all known performance objects.</span></span> <span data-ttu-id="d454e-116">Para determinar qué clases están disponibles, y para identificar qué miembros tienen esas clases, consulte [recuperar documentación para objetos de datos de rendimiento sin formato y con formato](retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="d454e-116">To determine what classes are available to you, and to identify what members those classes have, see [Retrieving Documentation for Raw and Formatted Performance Data Objects](retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="d454e-117">Las [**clases \_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) usan el calificador **CookingType** en los [tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md) para especificar la fórmula para calcular los datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d454e-117">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes use the **CookingType** qualifier in [WMI Performance Counter Types](wmi-performance-counter-types.md) to specify the formula for calculating performance data.</span></span> <span data-ttu-id="d454e-118">Este calificador es el mismo que el calificador de **tipo** en las clases [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="d454e-118">This qualifier is the same as the **CounterType** qualifier in the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span>

<span data-ttu-id="d454e-119">Como proveedor de alto rendimiento, el proveedor de contadores cocidos implementa la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como el método [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) y los siguientes métodos de [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :</span><span class="sxs-lookup"><span data-stu-id="d454e-119">As a high-performance provider, the Cooked Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="d454e-120">**CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="d454e-120">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="d454e-121">**CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="d454e-121">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="d454e-122">**CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="d454e-122">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="d454e-123">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="d454e-123">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="d454e-124">**QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="d454e-124">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="d454e-125">**StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="d454e-125">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="d454e-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d454e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d454e-127">Proveedores WMI</span><span class="sxs-lookup"><span data-stu-id="d454e-127">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
