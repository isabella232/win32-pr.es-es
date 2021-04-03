---
description: El proveedor de datos de rendimiento con formato de alto rendimiento de WMI calcula los tipos de contador estadísticos en un número especificado de muestras de datos del contador sin formato.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Tipos de contadores estadísticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082977"
---
# <a name="statistical-counter-types"></a><span data-ttu-id="754d1-103">Tipos de contadores estadísticos</span><span class="sxs-lookup"><span data-stu-id="754d1-103">Statistical Counter Types</span></span>

<span data-ttu-id="754d1-104">El proveedor de datos de [rendimiento con formato](formatted-performance-data-provider.md) de alto rendimiento de WMI calcula los tipos de contador estadísticos en un número especificado de muestras de datos del contador sin formato.</span><span class="sxs-lookup"><span data-stu-id="754d1-104">The WMI high-performance [Formatted Performance Data Provider](formatted-performance-data-provider.md) calculates the statistical counter types on a specified number of raw counter data samples.</span></span> <span data-ttu-id="754d1-105">Los algoritmos de los tipos de contador no requieren propiedades de frecuencia o marca de tiempo heredadas (como **timestamp \_ PerfTime** o **Frequency \_ PerfTime**) que otros tipos de contador requieren.</span><span class="sxs-lookup"><span data-stu-id="754d1-105">The algorithms for the counter types do not require inherited timestamp or frequency properties (such as **TimeStamp\_PerfTime** or **Frequency\_PerfTime**) that other counter types require.</span></span>

<span data-ttu-id="754d1-106">En su lugar, los tipos de contador estadísticos admiten un **calificador** que identifique el número de ejemplos que se van a utilizar.</span><span class="sxs-lookup"><span data-stu-id="754d1-106">Instead, the statistical counter types support a **qualifier** that identifies how many samples to use.</span></span> <span data-ttu-id="754d1-107">Se recopila un ejemplo cuando se llama al método [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) para el objeto de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="754d1-107">A sample is collected when the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method is called for the performance object.</span></span> <span data-ttu-id="754d1-108">En el caso de los scripts, use el método [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) .</span><span class="sxs-lookup"><span data-stu-id="754d1-108">For scripts use the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method.</span></span> <span data-ttu-id="754d1-109">Los datos calculados contienen el resultado del cálculo realizado en el número de muestras de **SampleWindow** de la propiedad de datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="754d1-109">The calculated data contains the result of the calculation performed on the **SampleWindow** number of samples from the raw data property.</span></span> <span data-ttu-id="754d1-110">Los datos sin procesar para el cálculo incluyen FRM el nombre de propiedad especificado en el calificador de **contador** .</span><span class="sxs-lookup"><span data-stu-id="754d1-110">The raw data for the calculation comes frm the property name specified in the **Counter** qualifier.</span></span>

<span data-ttu-id="754d1-111">Para obtener más información, vea [obtener datos de rendimiento estadísticos](obtaining-statistical-performance-data.md) y [obtener acceso a las clases de rendimiento preinstaladas de WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="754d1-111">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>



| <span data-ttu-id="754d1-112">Contratipo (constante)</span><span class="sxs-lookup"><span data-stu-id="754d1-112">CounterType Constant</span></span>                    | <span data-ttu-id="754d1-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="754d1-113">Description</span></span>                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="754d1-114">media de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="754d1-114">COOKER\_AVERAGE</span></span>](cooker-average.md)   | <span data-ttu-id="754d1-115">Suma las observaciones repetidas de una propiedad en una clase [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y divide la suma por el número de observaciones.</span><span class="sxs-lookup"><span data-stu-id="754d1-115">Sums repeated observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and divides the sum by the number of observations.</span></span>                              |
| [<span data-ttu-id="754d1-116">COOKER \_ máx.</span><span class="sxs-lookup"><span data-stu-id="754d1-116">COOKER\_MAX</span></span>](cooker-max.md)           | <span data-ttu-id="754d1-117">Valor más grande de un conjunto de observaciones de una propiedad en una clase [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="754d1-117">Largest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                    |
| [<span data-ttu-id="754d1-118">COOKER \_ mín.</span><span class="sxs-lookup"><span data-stu-id="754d1-118">COOKER\_MIN</span></span>](cooker-min.md)           | <span data-ttu-id="754d1-119">Valor menor de un conjunto de observaciones de una propiedad en una clase [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="754d1-119">Smallest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                   |
| [<span data-ttu-id="754d1-120">\_intervalo Cooker</span><span class="sxs-lookup"><span data-stu-id="754d1-120">COOKER\_RANGE</span></span>](cooker-range.md)       | <span data-ttu-id="754d1-121">Diferencia entre los valores [mínimo](cooker-min.md) y [máximo](cooker-max.md) de un conjunto de observaciones sin formato de una propiedad en una clase [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="754d1-121">Difference between the [Min](cooker-min.md) and [Max](cooker-max.md) values for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span> |
| [<span data-ttu-id="754d1-122">varianza de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="754d1-122">COOKER\_VARIANCE</span></span>](cooker-variance.md) | <span data-ttu-id="754d1-123">Medida de variabilidad que se puede utilizar para caracterizar la dispersión para un conjunto de observaciones sin formato de una propiedad en una clase [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="754d1-123">Measure of variability that can be used to characterize dispersion for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="754d1-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="754d1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="754d1-125">Tipos de contador de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="754d1-125">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="754d1-126">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="754d1-126">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="754d1-127">Actualizar datos WMI en scripts</span><span class="sxs-lookup"><span data-stu-id="754d1-127">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="754d1-128">Obtener acceso a los datos de rendimiento del script</span><span class="sxs-lookup"><span data-stu-id="754d1-128">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="754d1-129">Obtener acceso a los datos de rendimiento en C++</span><span class="sxs-lookup"><span data-stu-id="754d1-129">Accessing Performance Data in C++</span></span>](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
