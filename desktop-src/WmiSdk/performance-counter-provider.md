---
description: El proveedor de contadores de rendimiento es un proveedor de alto rendimiento que proporciona datos de contador de rendimiento sin procesar a las clases de contador de rendimiento de WMI derivadas de Win32 \_ PerfRawData. El nombre de la \_ \_ instancia de Win32Provider es &\# 0034; NT5 \_ GenericPerfProvider \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Proveedor de contador de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083339"
---
# <a name="performance-counter-provider"></a><span data-ttu-id="a6c43-104">Proveedor de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="a6c43-104">Performance Counter Provider</span></span>

<span data-ttu-id="a6c43-105">\[El proveedor de contadores de rendimiento ya no está disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="a6c43-105">\[The Performance Counter Provider is no longer available for use.</span></span> <span data-ttu-id="a6c43-106">En su lugar, use el proveedor [WMIPerfInst](wmiperfinst-provider.md) .\]</span><span class="sxs-lookup"><span data-stu-id="a6c43-106">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="a6c43-107">El proveedor de contadores de rendimiento es un proveedor de alto rendimiento que proporciona datos de contador de rendimiento sin procesar a las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="a6c43-107">The Performance Counter provider is a high-performance provider that provides raw performance counter data to the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="a6c43-108">El nombre de la instancia de [**\_ \_ Win32Provider**](--win32provider.md) es "NT5 \_ GenericPerfProvider \_ v1".</span><span class="sxs-lookup"><span data-stu-id="a6c43-108">The [**\_\_Win32Provider**](--win32provider.md) instance name is "NT5\_GenericPerfProvider\_V1".</span></span>

<span data-ttu-id="a6c43-109">Las [**clases \_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) se encuentran en el espacio de \\ nombres "root CIMv2" de WMI.</span><span class="sxs-lookup"><span data-stu-id="a6c43-109">The [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes are located in the WMI "Root\\CIMv2" namespace.</span></span> <span data-ttu-id="a6c43-110">Cada clase de rendimiento de WMI corresponde a un objeto de rendimiento en una biblioteca de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a6c43-110">Each WMI performance class corresponds to a performance object in a performance library.</span></span> <span data-ttu-id="a6c43-111">Las propiedades de estas clases representan los contadores para el objeto.</span><span class="sxs-lookup"><span data-stu-id="a6c43-111">The properties of these classes represent the counters for the object.</span></span> <span data-ttu-id="a6c43-112">El nombre de clase WMI para un objeto de contador sin formato tiene el formato \**Win32 \_ \_ \_ PerfRawData* nombre del servicio nombre del \_ *\_* objeto \_ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="a6c43-112">The WMI class name for a raw counter object is of the form \**Win32\_PerfRawData\_\_* service\_name *\_* object\_name\*\*\*.</span></span> <span data-ttu-id="a6c43-113">Por ejemplo, el nombre de clase WMI que contiene los contadores de disco lógico es [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="a6c43-113">For example, the WMI class name that contains the logical disk counters is [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="a6c43-114">Puede usar la clase [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondiente para obtener los datos de rendimiento calculados previamente que se muestran en el [*monitor de sistema*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="a6c43-114">You can use the corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class to get the pre-calculated performance data shown in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="a6c43-115">Por ejemplo, use la clase [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) para obtener datos de disco calculados previamente.</span><span class="sxs-lookup"><span data-stu-id="a6c43-115">For example, use the [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class to get pre-calculated disk data.</span></span>

<span data-ttu-id="a6c43-116">Para obtener más información sobre cómo escribir un cliente que pueda tener acceso a datos de rendimiento sin procesar, vea [obtener acceso a los datos de rendimiento en C++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="a6c43-116">For more information about how to write a client that can access raw performance data, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

<span data-ttu-id="a6c43-117">Como proveedor de alto rendimiento, el proveedor de contadores de rendimiento implementa la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como el método [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) y los siguientes métodos [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :</span><span class="sxs-lookup"><span data-stu-id="a6c43-117">As a high-performance provider, the Performance Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="a6c43-118">**CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="a6c43-118">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="a6c43-119">**CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="a6c43-119">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="a6c43-120">**CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="a6c43-120">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="a6c43-121">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="a6c43-121">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="a6c43-122">**QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="a6c43-122">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="a6c43-123">**StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="a6c43-123">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="a6c43-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6c43-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6c43-125">Proveedores WMI</span><span class="sxs-lookup"><span data-stu-id="a6c43-125">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
