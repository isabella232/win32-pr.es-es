---
description: A partir de Windows Vista, el proveedor WmiPerfInst proporciona datos del contador de rendimiento sin formato y con formato de forma dinámica a clases de contador de rendimiento de WMI derivadas de rendimiento de Win32 \_ .
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Proveedor WmiPerfInst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696914"
---
# <a name="wmiperfinst-provider"></a><span data-ttu-id="c1546-103">Proveedor WmiPerfInst</span><span class="sxs-lookup"><span data-stu-id="c1546-103">WmiPerfInst Provider</span></span>

<span data-ttu-id="c1546-104">A partir de Windows Vista, el proveedor WmiPerfInst proporciona datos del contador de rendimiento sin formato y con formato de forma dinámica a [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI derivadas de [**\_ rendimiento de Win32**](/windows/desktop/CIMWin32Prov/win32-perf).</span><span class="sxs-lookup"><span data-stu-id="c1546-104">Starting with Windows Vista, the WmiPerfInst provider supplies raw and formatted performance counter data dynamically to WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span> <span data-ttu-id="c1546-105">Este proveedor reemplaza el [proveedor de datos de rendimiento con formato](formatted-performance-data-provider.md), también conocido como "proveedor de contador cocido", y el [proveedor de contadores de rendimiento](performance-counter-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c1546-105">This provider replaces the [Formatted Performance Data Provider](formatted-performance-data-provider.md), also known as the "Cooked Counter Provider", and the [Performance Counter Provider](performance-counter-provider.md).</span></span>

<span data-ttu-id="c1546-106">El proveedor WmiPerfInst proporciona datos a las clases WMI que proporciona el proveedor [WMIPerfClass](wmiperfclass-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="c1546-106">The WmiPerfInst provider supplies data to the WMI classes that are provided by the [WMIPerfClass](wmiperfclass-provider.md) provider.</span></span> <span data-ttu-id="c1546-107">Este proveedor es un puente entre las instancias del ayudante de datos de rendimiento (PDH) y las clases de rendimiento de WMI proporcionadas por el proveedor de WmiPerfClass.</span><span class="sxs-lookup"><span data-stu-id="c1546-107">This provider is a bridge between Performance Data Helper (PDH) instances and the WMI performance classes supplied by the WmiPerfClass Provider.</span></span> <span data-ttu-id="c1546-108">Cuando WmiPerfInst recibe una consulta de datos, carga la clase y usa los [calificadores](qualifiers-specific-to-wmi-performance-classes.md) de clase y propiedad para buscar las instancias de PDH.</span><span class="sxs-lookup"><span data-stu-id="c1546-108">When WmiPerfInst receives a query for data, it loads the class and uses the class and property [qualifiers](qualifiers-specific-to-wmi-performance-classes.md) to locate the PDH instances.</span></span> <span data-ttu-id="c1546-109">Para obtener más información, vea [usar las funciones de PDH para consumir datos de contador](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span><span class="sxs-lookup"><span data-stu-id="c1546-109">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

<span data-ttu-id="c1546-110">No se recomienda desarrollar nuevos objetos de rendimiento mediante la creación de un proveedor de alto rendimiento de WMI y depender del proceso del [*adaptador de ADAP inverso*](gloss-r.md) para transferir los datos a las bibliotecas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c1546-110">It is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries.</span></span> <span data-ttu-id="c1546-111">La excepción es cuando se desarrolla un controlador de Modelo de controlador de Windows y se desea proporcionar datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c1546-111">The exception is when you are developing a Windows Driver Model driver and want to supply performance data.</span></span> <span data-ttu-id="c1546-112">Aunque el proceso de adaptador inverso sigue funcionando por compatibilidad con versiones anteriores, el método recomendado es usar los [contadores de rendimiento versión 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="c1546-112">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="c1546-113">El nombre de instancia [**\_ \_ Win32Provider**](--win32provider.md) de este proveedor es "WmiPerfInst".</span><span class="sxs-lookup"><span data-stu-id="c1546-113">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfInst".</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1546-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c1546-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1546-115">Proveedores WMI</span><span class="sxs-lookup"><span data-stu-id="c1546-115">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="c1546-116">Bibliotecas de rendimiento y WMI</span><span class="sxs-lookup"><span data-stu-id="c1546-116">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="c1546-117">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="c1546-117">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
