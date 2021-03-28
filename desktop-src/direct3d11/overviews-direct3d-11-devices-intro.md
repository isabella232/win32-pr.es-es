---
title: Introducción a un dispositivo en Direct3D 11
description: El modelo de objetos de Direct3D 11 separa la funcionalidad de creación y representación de recursos en un dispositivo y uno o más contextos. Esta separación está diseñada para facilitar el multithreading.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b03333c6594f17d85fee28880e46928241e06c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983686"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a><span data-ttu-id="8bf3f-103">Introducción a un dispositivo en Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="8bf3f-103">Introduction to a Device in Direct3D 11</span></span>

<span data-ttu-id="8bf3f-104">El modelo de objetos de Direct3D 11 separa la funcionalidad de creación y representación de recursos en un dispositivo y uno o más contextos. Esta separación está diseñada para facilitar el multithreading.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-104">The Direct3D 11 object model separates resource creation and rendering functionality into a device and one or more contexts; this separation is designed to facilitate multithreading.</span></span>

-   [<span data-ttu-id="8bf3f-105">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="8bf3f-105">Device</span></span>](#introduction-to-a-device-in-direct3d-11)
-   [<span data-ttu-id="8bf3f-106">Contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8bf3f-106">Device Context</span></span>](#device-context)
    -   [<span data-ttu-id="8bf3f-107">Contexto inmediato</span><span class="sxs-lookup"><span data-stu-id="8bf3f-107">Immediate Context</span></span>](#immediate-context)
    -   [<span data-ttu-id="8bf3f-108">Contexto diferido</span><span class="sxs-lookup"><span data-stu-id="8bf3f-108">Deferred Context</span></span>](#deferred-context)
-   [<span data-ttu-id="8bf3f-109">Consideraciones sobre los subprocesos</span><span class="sxs-lookup"><span data-stu-id="8bf3f-109">Threading Considerations</span></span>](#threading-considerations)
-   [<span data-ttu-id="8bf3f-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bf3f-110">Related topics</span></span>](#related-topics)

## <a name="device"></a><span data-ttu-id="8bf3f-111">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="8bf3f-111">Device</span></span>

<span data-ttu-id="8bf3f-112">Un dispositivo se usa para crear recursos y para enumerar las capacidades de un adaptador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-112">A device is used to create resources and to enumerate the capabilities of a display adapter.</span></span> <span data-ttu-id="8bf3f-113">En Direct3D 11, un dispositivo se representa con una interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="8bf3f-113">In Direct3D 11, a device is represented with an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface.</span></span>

<span data-ttu-id="8bf3f-114">Cada aplicación debe tener al menos un dispositivo, mientras que la mayoría de las aplicaciones solo crea un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-114">Each application must have at least one device, most applications only create one device.</span></span> <span data-ttu-id="8bf3f-115">Cree un dispositivo para uno de los controladores de hardware instalados en el equipo mediante una llamada a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) y especifique el tipo de controlador con la marca de [**\_ \_ tipo de controlador D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="8bf3f-115">Create a device for one of the hardware drivers installed on your machine by calling [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and specify the driver type with the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) flag.</span></span> <span data-ttu-id="8bf3f-116">Cada dispositivo puede usar uno o más contextos de dispositivo, en función de la funcionalidad deseada.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-116">Each device can use one or more device contexts, depending on the functionality desired.</span></span>

## <a name="device-context"></a><span data-ttu-id="8bf3f-117">Contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8bf3f-117">Device Context</span></span>

<span data-ttu-id="8bf3f-118">Un contexto de dispositivo contiene la circunstancia o la configuración en la que se usa un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-118">A device context contains the circumstance or setting in which a device is used.</span></span> <span data-ttu-id="8bf3f-119">Más concretamente, se usa un contexto de dispositivo para establecer el estado de la canalización y generar comandos de representación mediante los recursos que pertenecen a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-119">More specifically, a device context is used to set pipeline state and generate rendering commands using the resources owned by a device.</span></span> <span data-ttu-id="8bf3f-120">Direct3D 11 implementa dos tipos de contextos de dispositivo, uno para la representación inmediata y otro para la representación diferida; ambos contextos se representan con una interfaz [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="8bf3f-120">Direct3D 11 implements two types of device contexts, one for immediate rendering and the other for deferred rendering; both contexts are represented with an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span>

### <a name="immediate-context"></a><span data-ttu-id="8bf3f-121">Contexto inmediato</span><span class="sxs-lookup"><span data-stu-id="8bf3f-121">Immediate Context</span></span>

<span data-ttu-id="8bf3f-122">Un contexto inmediato se representa directamente en el controlador.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-122">An immediate context renders directly to the driver.</span></span> <span data-ttu-id="8bf3f-123">Cada dispositivo tiene uno y solo un contexto inmediato que puede recuperar datos de la GPU.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-123">Each device has one and only one immediate context which can retrieve data from the GPU.</span></span> <span data-ttu-id="8bf3f-124">Un contexto inmediato se puede usar para representar (o reproducir) inmediatamente una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="8bf3f-124">An immediate context can be used to immediately render (or play back) a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span>

<span data-ttu-id="8bf3f-125">Hay dos maneras de obtener un contexto inmediato:</span><span class="sxs-lookup"><span data-stu-id="8bf3f-125">There are two ways to get an immediate context:</span></span>

-   <span data-ttu-id="8bf3f-126">Llamando a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="8bf3f-126">By calling either [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>
-   <span data-ttu-id="8bf3f-127">Llamando a [**ID3D11Device:: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span><span class="sxs-lookup"><span data-stu-id="8bf3f-127">By calling [**ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span></span>

### <a name="deferred-context"></a><span data-ttu-id="8bf3f-128">Contexto diferido</span><span class="sxs-lookup"><span data-stu-id="8bf3f-128">Deferred Context</span></span>

<span data-ttu-id="8bf3f-129">Un contexto diferido registra los comandos de GPU en una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="8bf3f-129">A deferred context records GPU commands into a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="8bf3f-130">Un contexto diferido se utiliza principalmente para el multithreading y no es necesario para una aplicación de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-130">A deferred context is primarily used for multithreading and is not necessary for a single-threaded application.</span></span> <span data-ttu-id="8bf3f-131">Un subproceso de trabajo suele usar un contexto diferido en lugar del subproceso principal de representación.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-131">A deferred context is generally used by a worker thread instead of the main rendering thread.</span></span> <span data-ttu-id="8bf3f-132">Cuando se crea un contexto diferido, no hereda ningún estado del contexto inmediato.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-132">When you create a deferred context, it does not inherit any state from the immediate context.</span></span>

<span data-ttu-id="8bf3f-133">Para obtener un contexto diferido, llame a [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="8bf3f-133">To get a deferred context, call [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

<span data-ttu-id="8bf3f-134">Cualquier contexto: inmediato o aplazado se puede usar en cualquier subproceso, siempre que el contexto solo se use en un subproceso cada vez.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-134">Any context -- immediate or deferred -- can be used on any thread as long as the context is only used in one thread at a time.</span></span>

## <a name="threading-considerations"></a><span data-ttu-id="8bf3f-135">Consideraciones sobre los subprocesos</span><span class="sxs-lookup"><span data-stu-id="8bf3f-135">Threading Considerations</span></span>

<span data-ttu-id="8bf3f-136">En esta tabla se resaltan las diferencias en el modelo de subprocesos de Direct3D 11 de versiones anteriores de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-136">This table highlights the differences in the threading model in Direct3D 11 from prior versions of Direct3D.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8bf3f-137">Diferencias entre Direct3D 11 y versiones anteriores de Direct3D:</span><span class="sxs-lookup"><span data-stu-id="8bf3f-137">Differences between Direct3D 11 and previous versions of Direct3D:</span></span><br/> <span data-ttu-id="8bf3f-138">Todos los métodos de interfaz <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> son de subprocesos libres, lo que significa que es seguro tener varios subprocesos que llaman a las funciones al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-138">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> interface methods are free-threaded, which means it is safe to have multiple threads call the functions at the same time.</span></span><br/>
<ul>
<li><span data-ttu-id="8bf3f-139">Todas las interfaces derivadas de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>(<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) son de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-139">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>-derived interfaces (<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) are free-threaded.</span></span></li>
<li><span data-ttu-id="8bf3f-140">Direct3D 11 divide la creación y representación de recursos en dos interfaces.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-140">Direct3D 11 splits resource creating and rendering into two interfaces.</span></span> <span data-ttu-id="8bf3f-141">Map, unmapping, Begin, end y GetData se implementan en <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> porque <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> define fuertemente el orden de las operaciones.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-141">Map, Unmap, Begin, End, and GetData are implemented on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> because <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> strongly defines the order of operations.</span></span> <span data-ttu-id="8bf3f-142">Las interfaces <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> y <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> también implementan métodos para operaciones de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-142"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> and <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> interfaces also implement methods for free-threaded operations.</span></span></li>
<li><span data-ttu-id="8bf3f-143">Los métodos de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> (excepto los que existen en <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) no son de subprocesos libres, es decir, requieren un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-143">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> methods (except for those that exist on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) are not free-threaded, that is, they require single threading.</span></span> <span data-ttu-id="8bf3f-144">Solo un subproceso puede llamar a cualquiera de sus métodos (dibujar, copiar, asignar, etc.) de forma segura a la vez.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-144">Only one thread may safely be calling any of its methods (Draw, Copy, Map, etc.) at a time.</span></span></li>
<li><span data-ttu-id="8bf3f-145">En general, el subprocesamiento libre minimiza el número de primitivas de sincronización utilizadas y su duración.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-145">In general, free-threading minimizes the number of synchronization primitives used as well as their duration.</span></span> <span data-ttu-id="8bf3f-146">Sin embargo, una aplicación que usa la sincronización durante mucho tiempo puede afectar directamente a la cantidad de simultaneidad que una aplicación puede esperar alcanzar.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-146">However, an application that uses synchronization held for a long time can directly impact how much concurrency an application can expect to achieve.</span></span></li>
</ul>
<span data-ttu-id="8bf3f-147">Los métodos de interfaz ID3D10Device no están diseñados para ser de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-147">ID3D10Device interface methods are not designed to be free-threaded.</span></span> <span data-ttu-id="8bf3f-148">ID3D10Device implementa toda la funcionalidad de creación y representación (como hace ID3D9Device en Direct3D 9).</span><span class="sxs-lookup"><span data-stu-id="8bf3f-148">ID3D10Device implements all create and rendering functionality (as does ID3D9Device in Direct3D 9).</span></span> <span data-ttu-id="8bf3f-149">Map y unmapping se implementan en las interfaces derivadas de ID3D10Resource, Begin, end y GetData se implementan en las interfaces derivadas de ID3D10Asynchronous.</span><span class="sxs-lookup"><span data-stu-id="8bf3f-149">Map and Unmap are implemented on ID3D10Resource-derived interfaces, Begin, End, and GetData are implemented on ID3D10Asynchronous-derived interfaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8bf3f-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bf3f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bf3f-151">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="8bf3f-151">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





