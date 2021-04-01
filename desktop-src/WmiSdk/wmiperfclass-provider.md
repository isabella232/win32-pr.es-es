---
description: A partir de Windows Vista, este proveedor crea las clases de contador de rendimiento de WMI.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Proveedor WmiPerfClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082752"
---
# <a name="wmiperfclass-provider"></a><span data-ttu-id="81b2b-103">Proveedor WmiPerfClass</span><span class="sxs-lookup"><span data-stu-id="81b2b-103">WmiPerfClass Provider</span></span>

<span data-ttu-id="81b2b-104">A partir de Windows Vista, este proveedor crea las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)de WMI.</span><span class="sxs-lookup"><span data-stu-id="81b2b-104">Starting with Windows Vista, this provider creates the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="81b2b-105">El proveedor [WMIPerfInst](wmiperfinst-provider.md) proporciona los datos de forma dinámica a estas clases de rendimiento de WMI.</span><span class="sxs-lookup"><span data-stu-id="81b2b-105">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst](wmiperfinst-provider.md) provider.</span></span> <span data-ttu-id="81b2b-106">El proceso de detección automática/purga (ADAP) ya no transfiere objetos de contador de rendimiento a clases de rendimiento de WMI en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="81b2b-106">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="81b2b-107">Para obtener más información, consulte [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="81b2b-107">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="81b2b-108">Para obtener más información, consulte [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="81b2b-108">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="81b2b-109">Aunque no se recomienda desarrollar nuevos objetos de rendimiento mediante la creación de un proveedor de alto rendimiento de WMI y depender del proceso del [*adaptador de ADAP inverso*](gloss-r.md) para transferir los datos a las bibliotecas de rendimiento, la excepción es el desarrollo de un controlador de modelo de controlador de Windows que proporciona datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="81b2b-109">While it is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries, the exception is development of a Windows Driver Model driver that supplies performance data.</span></span> <span data-ttu-id="81b2b-110">Aunque el proceso de adaptador inverso sigue funcionando por compatibilidad con versiones anteriores, el método recomendado es usar los [contadores de rendimiento versión 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="81b2b-110">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="81b2b-111">El nombre de instancia [**\_ \_ Win32Provider**](--win32provider.md) de este proveedor es "WmiPerfClass".</span><span class="sxs-lookup"><span data-stu-id="81b2b-111">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfClass".</span></span>

## <a name="related-topics"></a><span data-ttu-id="81b2b-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81b2b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81b2b-113">Proveedores WMI</span><span class="sxs-lookup"><span data-stu-id="81b2b-113">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="81b2b-114">Bibliotecas de rendimiento y WMI</span><span class="sxs-lookup"><span data-stu-id="81b2b-114">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="81b2b-115">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="81b2b-115">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
