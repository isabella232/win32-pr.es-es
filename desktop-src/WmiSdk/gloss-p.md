---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd72fca871352f8a31652eb72f693da43d1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002947"
---
# <a name="p-wmi"></a><span data-ttu-id="9038a-103">P (WMI)</span><span class="sxs-lookup"><span data-stu-id="9038a-103">P (WMI)</span></span>

<span data-ttu-id="9038a-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [o](gloss-o.md) p [Q](gloss-q.md) [R](gloss-r.md) [s](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="9038a-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="9038a-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**contador de rendimiento**</span><span class="sxs-lookup"><span data-stu-id="9038a-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**performance counter**</span></span>
</dt> <dd>

<span data-ttu-id="9038a-106">Propiedad de una clase de rendimiento que se deriva de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) que almacena los datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="9038a-106">A property in a performance class that is derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) that stores performance data.</span></span>

</dd> <dt>

<span data-ttu-id="9038a-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**objeto de rendimiento**</span><span class="sxs-lookup"><span data-stu-id="9038a-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**performance object**</span></span>
</dt> <dd>

<span data-ttu-id="9038a-108">Objeto de una biblioteca de rendimiento que almacena los datos en los contadores.</span><span class="sxs-lookup"><span data-stu-id="9038a-108">An object in a performance library that stores data in counters.</span></span> <span data-ttu-id="9038a-109">Estos objetos están visibles en la utilidad [*monitor de sistema*](gloss-s.md) .</span><span class="sxs-lookup"><span data-stu-id="9038a-109">These objects are visible in the [*System Monitor*](gloss-s.md) utility.</span></span> <span data-ttu-id="9038a-110">Algunos ejemplos son los objetos de disco lógico y de caché.</span><span class="sxs-lookup"><span data-stu-id="9038a-110">Examples are Cache and Logical Disk objects.</span></span> <span data-ttu-id="9038a-111">Cuando el proceso [*ADAP*](gloss-a.md) lo transfiere a WMI, cada objeto se convierte en dos clases de rendimiento de WMI.</span><span class="sxs-lookup"><span data-stu-id="9038a-111">When transferred into WMI by the [*ADAP*](gloss-a.md) process, each object becomes two WMI performance classes.</span></span> <span data-ttu-id="9038a-112">Una clase, que contiene datos sin procesar, se deriva de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="9038a-112">One class, containing raw data, derives from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="9038a-113">La otra clase se deriva de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) y contiene los mismos datos visibles en el monitor de sistema calculados por el proveedor de contadores cocidos.</span><span class="sxs-lookup"><span data-stu-id="9038a-113">The other class derives from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and contains the same data visible in System Monitor as calculated by the Cooked Counter provider.</span></span>

</dd> <dt>

<span data-ttu-id="9038a-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**consumidor permanente**</span><span class="sxs-lookup"><span data-stu-id="9038a-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**permanent consumer**</span></span>
</dt> <dd>

<span data-ttu-id="9038a-115">[*Consumidor de eventos*](gloss-e.md) cuyo registro se mantiene hasta que se cancela explícitamente.</span><span class="sxs-lookup"><span data-stu-id="9038a-115">An [*event consumer*](gloss-e.md) whose registration lasts until it is explicitly canceled.</span></span> <span data-ttu-id="9038a-116">Vea también [*consumidor temporal*](gloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="9038a-116">Also see [*temporary consumer*](gloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="9038a-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**consumidor físico**</span><span class="sxs-lookup"><span data-stu-id="9038a-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**physical consumer**</span></span>
</dt> <dd>

<span data-ttu-id="9038a-118">Objeto COM implementado por un proveedor de [*consumidor de eventos*](gloss-e.md) que incluye un [*receptor*](gloss-s.md) para recibir notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="9038a-118">A COM object that is implemented by an [*event consumer provider*](gloss-e.md) that includes a [*sink*](gloss-s.md) for receiving event notifications.</span></span>

</dd> <dt>

<span data-ttu-id="9038a-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**propiedad**</span><span class="sxs-lookup"><span data-stu-id="9038a-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="9038a-120">Un par de nombre y valor que describe una unidad de datos para una clase.</span><span class="sxs-lookup"><span data-stu-id="9038a-120">A name/value pair that describes a unit of data for a class.</span></span> <span data-ttu-id="9038a-121">Los valores de propiedad deben tener un tipo de datos [*Managed Object Format válido (MOF)*](gloss-m.md) .</span><span class="sxs-lookup"><span data-stu-id="9038a-121">Property values must have a valid [*Managed Object Format (MOF)*](gloss-m.md) data type.</span></span> <span data-ttu-id="9038a-122">Consulte también [*propiedad Reference*](gloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="9038a-122">Also see [*reference property*](gloss-r.md).</span></span>

</dd> <dt>

<span data-ttu-id="9038a-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**proveedor de propiedades**</span><span class="sxs-lookup"><span data-stu-id="9038a-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**property provider**</span></span>
</dt> <dd>

<span data-ttu-id="9038a-124">Un servidor COM que admite la recuperación y modificación de las propiedades de WMI.</span><span class="sxs-lookup"><span data-stu-id="9038a-124">A COM server that supports the retrieval and modification of WMI properties.</span></span> <span data-ttu-id="9038a-125">Los proveedores de propiedades implementan las interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) y [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) .</span><span class="sxs-lookup"><span data-stu-id="9038a-125">Property providers implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="9038a-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**presta**</span><span class="sxs-lookup"><span data-stu-id="9038a-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="9038a-127">Un servidor COM que se comunica con objetos administrados para obtener acceso a datos y notificaciones de eventos, como el registro o un dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="9038a-127">A COM server that communicates with managed objects to access data and event notifications, such as the registry or an SNMP device.</span></span> <span data-ttu-id="9038a-128">Los proveedores reenvían estos datos al [*Administrador de objetos CIM*](gloss-c.md) para la integración y la interpretación.</span><span class="sxs-lookup"><span data-stu-id="9038a-128">Providers forward this data to the [*CIM Object Manager*](gloss-c.md) for integration and interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="9038a-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**método de proveedor**</span><span class="sxs-lookup"><span data-stu-id="9038a-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**provider method**</span></span>
</dt> <dd>

<span data-ttu-id="9038a-130">Método que implementa un *proveedor* WMI.</span><span class="sxs-lookup"><span data-stu-id="9038a-130">A method that a WMI *provider* implements.</span></span>

</dd> </dl>

 

 
