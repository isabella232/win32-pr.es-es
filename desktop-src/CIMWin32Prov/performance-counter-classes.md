---
description: Las clases de contador de rendimiento permiten el acceso de scripts y programas a los datos de rendimiento del sistema calculados por proveedores de alto rendimiento existentes.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Clases de contador de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907539"
---
# <a name="performance-counter-classes"></a><span data-ttu-id="2be21-103">Clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="2be21-103">Performance Counter Classes</span></span>

<span data-ttu-id="2be21-104">Las clases de contador de rendimiento permiten el acceso de scripts y programas a los datos de rendimiento del sistema calculados por proveedores de alto rendimiento existentes.</span><span class="sxs-lookup"><span data-stu-id="2be21-104">Performance Counter classes allow script and program access to system performance data calculated by existing high-performance providers.</span></span> <span data-ttu-id="2be21-105">Estas clases se componen de clases de contador de rendimiento sin procesar y clases de contador de rendimiento con formato.</span><span class="sxs-lookup"><span data-stu-id="2be21-105">These classes consist of raw performance counter classes and formatted performance counter classes.</span></span>

<span data-ttu-id="2be21-106">Los diferentes proveedores proporcionan datos de la biblioteca de rendimiento a través de WMI.</span><span class="sxs-lookup"><span data-stu-id="2be21-106">Different providers supply performance library data through WMI.</span></span> <span data-ttu-id="2be21-107">Los proveedores [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) y [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) proporcionan clases para los [contadores de rendimiento](/windows/desktop/PerfCtrs/performance-counters-portal)de la versión 1 y la versión 2.</span><span class="sxs-lookup"><span data-stu-id="2be21-107">The [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) and [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) providers supply classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="2be21-108">Estos proveedores mantienen la compatibilidad con las clases disponibles en los sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="2be21-108">These providers maintain compatibility with the classes available in earlier operating systems.</span></span>

<span data-ttu-id="2be21-109">Las clases de esta sección son las clases base abstractas utilizadas para crear clases de contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2be21-109">The classes in this section are the abstract base classes used to create performance counter classes.</span></span> <span data-ttu-id="2be21-110">Esta no es una lista completa de las clases que se pueden encontrar en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2be21-110">This is not a complete list of classes that you may find on your operating system.</span></span> <span data-ttu-id="2be21-111">Para obtener más información, consulte [bibliotecas de rendimiento y WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2be21-111">For more information, see [Performance Libraries and WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2be21-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2be21-112">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2be21-113">**Rendimiento de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="2be21-113">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dd>

<span data-ttu-id="2be21-114">La clase base para las clases de contador de rendimiento [**Win32 \_ PerfRawData**](win32-perfrawdata.md) y [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="2be21-114">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

</dd> <dt>

[<span data-ttu-id="2be21-115">**Win32 \_ PerfFormattedData**</span><span class="sxs-lookup"><span data-stu-id="2be21-115">**Win32\_PerfFormattedData**</span></span>](win32-perfformatteddata.md)
</dt> <dd>

<span data-ttu-id="2be21-116">una clase base abstracta para las clases de datos calculadas preinstaladas.</span><span class="sxs-lookup"><span data-stu-id="2be21-116">an abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

[<span data-ttu-id="2be21-117">**Win32 \_ PerfRawData**</span><span class="sxs-lookup"><span data-stu-id="2be21-117">**Win32\_PerfRawData**</span></span>](win32-perfrawdata.md)
</dt> <dd>

<span data-ttu-id="2be21-118">La clase base abstracta para todas las clases de contador de rendimiento sin procesar concretas.</span><span class="sxs-lookup"><span data-stu-id="2be21-118">The abstract base class for all concrete raw performance counter classes.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="2be21-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2be21-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2be21-120">Clases Win32</span><span class="sxs-lookup"><span data-stu-id="2be21-120">Win32 Classes</span></span>](win32-provider.md)
</dt> </dl>

 

 
