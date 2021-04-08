---
description: Los proveedores, a menos que sean proveedores desacoplados que se ejecutan dentro de una aplicación, se cargan en un proceso de Wmiprvse.exe y no a través de Svchost.exe con un proceso de Winmgmt.exe. Para obtener más información, vea hospedaje y seguridad de proveedores.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Depurar proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001592"
---
# <a name="debugging-providers"></a><span data-ttu-id="023eb-104">Depurar proveedores</span><span class="sxs-lookup"><span data-stu-id="023eb-104">Debugging Providers</span></span>

<span data-ttu-id="023eb-105">Los proveedores, a menos que sean [*proveedores desacoplados*](gloss-d.md) que se ejecutan dentro de una aplicación, se cargan en un proceso de Wmiprvse.exe y no a través de Svchost.exe con un proceso de Winmgmt.exe.</span><span class="sxs-lookup"><span data-stu-id="023eb-105">Providers, unless they are [*decoupled providers*](gloss-d.md) running within an application, are loaded in a Wmiprvse.exe process, and not through Svchost.exe with a Winmgmt.exe process.</span></span> <span data-ttu-id="023eb-106">Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="023eb-106">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="023eb-107">Al detenerse en un punto de interrupción, el depurador de Visual Studio inmoviliza todo el proceso de host del proveedor, que suele ser el host compartido Wmiprvse.exe.</span><span class="sxs-lookup"><span data-stu-id="023eb-107">When stopping at a breakpoint, the Visual Studio debugger freezes the entire provider host process, which is usually the shared host Wmiprvse.exe.</span></span> <span data-ttu-id="023eb-108">Esto evita el funcionamiento de cualquier otro componente hospedado en ese proceso, incluida la extensión de Explorador de servidores WMI.</span><span class="sxs-lookup"><span data-stu-id="023eb-108">This prevents the operation of any other components hosted in that process, including the WMI Server Explorer extension.</span></span> <span data-ttu-id="023eb-109">También se bloquean las aplicaciones cliente que llaman al proveedor.</span><span class="sxs-lookup"><span data-stu-id="023eb-109">Client applications that call into the provider are also blocked.</span></span> <span data-ttu-id="023eb-110">Los problemas que se producen son peor en Windows 2000 y versiones anteriores porque el proveedor se carga en el proceso del servicio WMI (Winmgmt.exe).</span><span class="sxs-lookup"><span data-stu-id="023eb-110">The problems that result are worse in Windows 2000 and earlier because the provider is loaded into the WMI service process (Winmgmt.exe).</span></span>

<span data-ttu-id="023eb-111">Si ejecuta WMI Explorador de servidores en otra instancia, el IDE de Visual Studio no se inmoviliza y podrá liberar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="023eb-111">If you run WMI Server Explorer in another instance then Visual Studio IDE does not freeze and you are able to release the breakpoint.</span></span> <span data-ttu-id="023eb-112">Se recomienda ejecutar el proveedor en un proceso de hospedaje independiente durante la fase de desarrollo, de modo que la detención en un punto de interrupción solo inmoviliza el proceso que hospeda el proveedor.</span><span class="sxs-lookup"><span data-stu-id="023eb-112">It is recommended that you run your provider in a separate hosting process during the development phase, so that stopping at a breakpoint only freezes the process hosting your provider.</span></span> <span data-ttu-id="023eb-113">Las demás funciones de WMI continúan siendo accesibles para WMI Explorador de servidores y otras aplicaciones o scripts basados en WMI.</span><span class="sxs-lookup"><span data-stu-id="023eb-113">The other functions in WMI continue to be accessible to WMI Server Explorer and any other WMI-based applications or scripts.</span></span> <span data-ttu-id="023eb-114">Además, si el proveedor se bloquea, no afecta al funcionamiento de otros proveedores cargados en el mismo proceso de host.</span><span class="sxs-lookup"><span data-stu-id="023eb-114">Also, if your provider crashes, it does not affect the operation of other providers loaded into the same host process.</span></span>

<span data-ttu-id="023eb-115">Para realizar la carga del proveedor en su propio proceso de host, modifique el registro del proveedor para establecer la propiedad [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) en, `NetworkServiceHost:[MyProvider]` donde DataProvider puede ser cualquier cadena que identifique de forma única el proveedor.</span><span class="sxs-lookup"><span data-stu-id="023eb-115">To make your provider load in its own host process, modify the provider registration to set the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property to `NetworkServiceHost:[MyProvider]` where MyProvider can be any string that uniquely identifies your provider.</span></span> <span data-ttu-id="023eb-116">Por ejemplo, use el valor **\_ \_ Win32Provider. ClsId** .</span><span class="sxs-lookup"><span data-stu-id="023eb-116">For example, use the **\_\_Win32Provider.ClsId** value.</span></span> <span data-ttu-id="023eb-117">Cuando el proveedor esté listo para su envío, devuelva **\_ \_ Win32Provider. HostingModel** al valor previsto, como **NetworkServiceHost**.</span><span class="sxs-lookup"><span data-stu-id="023eb-117">When your provider is ready to ship, return **\_\_Win32Provider.HostingModel** to the intended value, such as **NetworkServiceHost**.</span></span>

<span data-ttu-id="023eb-118">Si no está depurando la carga del proveedor, puede llamar al [**método Load de la \_ clase de proveedores de msft**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) para forzar la carga del proveedor y, a continuación, asociar al proceso de Wmiprvse.exe que tiene la DLL cargada y depurar según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="023eb-118">If you are not debugging provider loading, you can call the [**Load method of the MSFT\_Providers class**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) to force your provider to load, then attach to the Wmiprvse.exe process that has the DLL loaded, and debug as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="023eb-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="023eb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="023eb-120">Solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="023eb-120">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="023eb-121">Clases de solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="023eb-121">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
