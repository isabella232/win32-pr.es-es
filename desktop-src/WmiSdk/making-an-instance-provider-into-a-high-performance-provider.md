---
description: No se recomienda escribir un proveedor de alto rendimiento de WMI para crear contadores de rendimiento.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Crear un proveedor de instancias en un proveedor de High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706390"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a><span data-ttu-id="f2148-103">Crear un proveedor de instancias en un proveedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="f2148-103">Making an Instance Provider into a High-Performance Provider</span></span>

<span data-ttu-id="f2148-104">No se recomienda escribir un proveedor de alto rendimiento de WMI para crear contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f2148-104">Writing a WMI high-performance provider to create performance counters is not recommended.</span></span> <span data-ttu-id="f2148-105">A partir de Windows Vista, las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI ya no se migran a las bibliotecas de rendimiento de Windows mediante el adaptador inverso de detección automática/autopurga (ADAP).</span><span class="sxs-lookup"><span data-stu-id="f2148-105">Starting with Windows Vista, the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) are no longer migrated into the Windows performance libraries by the AutoDiscovery/AutoPurge (ADAP) reverse adapter.</span></span> <span data-ttu-id="f2148-106">Para crear un proveedor de contadores de rendimiento, utilice los [contadores de rendimiento versión 2,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="f2148-106">To create a performance counter provider, use [Performance Counters Version 2.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="f2148-107">Después de crear los objetos de biblioteca de rendimiento, el [proveedor de WMIPerfClass](wmiperfclass-provider.md) analiza los objetos y crea o actualiza una clase WMI derivada [**de \_ Perf de Win32**](/windows/desktop/CIMWin32Prov/win32-perf) para cada objeto de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f2148-107">After performance library objects are created, the [WMIPerfClass Provider](wmiperfclass-provider.md) parses the objects and creates or refreshes a WMI class derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) for each performance object.</span></span> <span data-ttu-id="f2148-108">A continuación, el [proveedor WMIPerfInst](wmiperfinst-provider.md) proporciona dinámicamente datos de contador de rendimiento sin formato y con formato a las clases de rendimiento de WMI.</span><span class="sxs-lookup"><span data-stu-id="f2148-108">The [WMIPerfInst Provider](wmiperfinst-provider.md) then dynamically provides raw and formatted performance counter data to the WMI performance classes.</span></span>

<span data-ttu-id="f2148-109">El siguiente procedimiento de alto nivel proporciona los pasos necesarios para crear un proveedor de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f2148-109">The following high-level procedure provides the steps required to create a high-performance provider.</span></span>

<span data-ttu-id="f2148-110">**Para crear un proveedor de alto rendimiento**</span><span class="sxs-lookup"><span data-stu-id="f2148-110">**To create a high-performance provider**</span></span>

1.  <span data-ttu-id="f2148-111">Registre el proveedor con WMI.</span><span class="sxs-lookup"><span data-stu-id="f2148-111">Register your provider with WMI.</span></span> <span data-ttu-id="f2148-112">Para obtener más información, vea [registrar un proveedor de High-Performance](registering-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f2148-112">For more information, see [Registering a High-Performance Provider](registering-a-high-performance-provider.md).</span></span>
2.  <span data-ttu-id="f2148-113">Implemente el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f2148-113">Implement your provider.</span></span> <span data-ttu-id="f2148-114">Para obtener más información, consulte [escribir un proveedor de instancias](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f2148-114">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>
3.  <span data-ttu-id="f2148-115">Implemente la interfaz de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f2148-115">Implement the high-performance interface.</span></span> <span data-ttu-id="f2148-116">Para obtener más información, consulte [implementación de la interfaz High-Performance](implementing-the-high-performance-interface.md).</span><span class="sxs-lookup"><span data-stu-id="f2148-116">For more information, see [Implementing the High-Performance Interface](implementing-the-high-performance-interface.md).</span></span>
4.  <span data-ttu-id="f2148-117">Derive y escriba el esquema de Managed Object Format (MOF) para obtener datos de rendimiento sin procesar.</span><span class="sxs-lookup"><span data-stu-id="f2148-117">Derive and write your Managed Object Format (MOF) schema to obtain raw performance data.</span></span> <span data-ttu-id="f2148-118">Para obtener más información, consulte [compatibilidad con la \_ clase PerfRawData de Win32](supporting-the-win32-perfrawdata-class.md).</span><span class="sxs-lookup"><span data-stu-id="f2148-118">For more information, see [Supporting the Win32\_PerfRawData Class](supporting-the-win32-perfrawdata-class.md).</span></span>
5.  <span data-ttu-id="f2148-119">Derive y escriba el esquema MOF para obtener datos precalculados.</span><span class="sxs-lookup"><span data-stu-id="f2148-119">Derive and write your MOF schema to obtain precalculated data.</span></span> <span data-ttu-id="f2148-120">Al admitir esta clase, no es necesario que el proveedor realice los cálculos.</span><span class="sxs-lookup"><span data-stu-id="f2148-120">By supporting this class, the provider is not required to perform the calculations.</span></span> <span data-ttu-id="f2148-121">Estos datos serán los mismos que aparecen en el monitor de sistema de Perfmon.</span><span class="sxs-lookup"><span data-stu-id="f2148-121">This data will be the same that appears in the System Monitor in Perfmon.</span></span> <span data-ttu-id="f2148-122">Para obtener más información, consulte [compatibilidad con la \_ clase PerfFormattedData de Win32](supporting-the-win32-perfformatteddata-class.md).</span><span class="sxs-lookup"><span data-stu-id="f2148-122">For more information, see [Supporting the Win32\_PerfFormattedData Class](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2148-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2148-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2148-124">Desarrollar un proveedor WMI</span><span class="sxs-lookup"><span data-stu-id="f2148-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="f2148-125">Bibliotecas de rendimiento y WMI</span><span class="sxs-lookup"><span data-stu-id="f2148-125">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
