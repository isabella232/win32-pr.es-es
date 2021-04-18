---
title: Uso de DXCore para enumerar adaptadores
description: Un vistazo a las principales características de DXCore con algunos ejemplos de código, así como una lista completa de código fuente de una aplicación DXCore mínima.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: f1c21971f2daea69de1f317d1db8eceb9ec00118
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720146"
---
# <a name="using-dxcore-to-enumerate-adapters"></a><span data-ttu-id="434a7-103">Uso de DXCore para enumerar adaptadores</span><span class="sxs-lookup"><span data-stu-id="434a7-103">Using DXCore to enumerate adapters</span></span>

<span data-ttu-id="434a7-104">DXCore es una API de enumeración de adaptadores para dispositivos DirectX, por lo que algunas de sus funciones se superponen con las de [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="434a7-104">DXCore is an adapter enumeration API for DirectX devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span>

<span data-ttu-id="434a7-105">DXCore permite la exposición de nuevos tipos de dispositivos al modo de usuario, como MCDM (modelo de controladores de Microsoft Compute), para su uso con [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md)y [Windows machine learning](/windows/ai/windows-ml/).</span><span class="sxs-lookup"><span data-stu-id="434a7-105">DXCore enables the exposure of new device types to user mode, such as MCDM (Microsoft Compute Driver Model), for use with [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md), and [Windows Machine Learning](/windows/ai/windows-ml/).</span></span> <span data-ttu-id="434a7-106">DXCore, a diferencia de DXGI, no proporciona ninguna información sobre la tecnología o las propiedades relacionadas con la pantalla.</span><span class="sxs-lookup"><span data-stu-id="434a7-106">DXCore, unlike DXGI, does not provide any information about display-related technology or properties</span></span>

<span data-ttu-id="434a7-107">En las siguientes secciones, echaremos un vistazo a las principales características de DXCore con algunos ejemplos de código (escritos en [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span><span class="sxs-lookup"><span data-stu-id="434a7-107">In the next few sections, we'll take a look at the main features of DXCore with some code examples (written in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span></span> <span data-ttu-id="434a7-108">Los ejemplos de código que se muestran a continuación se extraen de la lista de código fuente completa que puede encontrar en el tema [aplicación DXCore mínima](dxcore-source-code.md).</span><span class="sxs-lookup"><span data-stu-id="434a7-108">The code examples shown below are extracted from the full source code listing that you can find in the topic [Minimal DXCore application](dxcore-source-code.md).</span></span>

## <a name="create-an-adapter-factory"></a><span data-ttu-id="434a7-109">Crear un generador de adaptadores</span><span class="sxs-lookup"><span data-stu-id="434a7-109">Create an adapter factory</span></span>

<span data-ttu-id="434a7-110">La enumeración del adaptador de DXCore se inicia mediante la creación de un objeto de generador de adaptadores, que se representa mediante la interfaz [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="434a7-110">You begin DXCore adapter enumeration by creating an adapter factory object, which is represented by the [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span> <span data-ttu-id="434a7-111">Para crear un generador, incluya el `dxcore.h` archivo de encabezado y llame a la función Free de [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="434a7-111">To create a factory, include the `dxcore.h` header file, and call the [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) free function.</span></span>

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a><span data-ttu-id="434a7-112">Recuperar una lista de adaptadores</span><span class="sxs-lookup"><span data-stu-id="434a7-112">Retrieve an adapter list</span></span>

<span data-ttu-id="434a7-113">A diferencia de lo que ocurre con DXGI, un generador de adaptadores de DXCore recién creado no crea automáticamente una instantánea del estado del adaptador del sistema.</span><span class="sxs-lookup"><span data-stu-id="434a7-113">Unlike with DXGI, a newly-created DXCore adapter factory doesn't automatically create a snapshot of the adapter state of the system.</span></span> <span data-ttu-id="434a7-114">En su lugar, DXCore crea esa instantánea cuando se recupera explícitamente un objeto de lista de adaptadores, que se representa mediante la interfaz [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) .</span><span class="sxs-lookup"><span data-stu-id="434a7-114">Instead, DXCore creates that snapshot when you explicitly retrieve an adapter list object, which is represented by the [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface.</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a><span data-ttu-id="434a7-115">Seleccionar un adaptador apropiado de la lista</span><span class="sxs-lookup"><span data-stu-id="434a7-115">Select an appropriate adapter from the list</span></span>

<span data-ttu-id="434a7-116">En esta sección se muestra cómo, dado un objeto de lista de adaptadores, podría encontrar el primer adaptador de hardware de la lista.</span><span class="sxs-lookup"><span data-stu-id="434a7-116">This section demonstrates how, given an adapter list object, you could find the first hardware adapter in the list.</span></span>

<span data-ttu-id="434a7-117">El método [**IDXCoreAdapterList:: GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) indica el número de elementos de la lista y [**IDXCoreAdapterList:: GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) recupera un adaptador específico por índice.</span><span class="sxs-lookup"><span data-stu-id="434a7-117">The [**IDXCoreAdapterList::GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) method tells you the number of elements in the list, and [**IDXCoreAdapterList::GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) retrieves a specific adapter by index.</span></span>

<span data-ttu-id="434a7-118">Después, puede consultar las propiedades de ese adaptador siguiendo estos pasos.</span><span class="sxs-lookup"><span data-stu-id="434a7-118">You can then query the properties of that adapter, by following these steps.</span></span>

- <span data-ttu-id="434a7-119">En primer lugar, para confirmar que es válido recuperar el valor de una propiedad determinada para este adaptador en esta versión del sistema operativo, llame a [**IDXCoreAdapter:: IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span><span class="sxs-lookup"><span data-stu-id="434a7-119">First, to confirm that it's valid to retrieve the value of a given property for this adapter on this operating system version, you call [**IDXCoreAdapter::IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span></span> <span data-ttu-id="434a7-120">Pase un valor de la enumeración [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) para identificar la propiedad sobre la que está consultando.</span><span class="sxs-lookup"><span data-stu-id="434a7-120">Pass a value of the [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) enumeration to identify which property you're querying about.</span></span>
- <span data-ttu-id="434a7-121">Opcionalmente, confirme el tamaño del valor de propiedad con una llamada a [**IDXCoreAdapter:: GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span><span class="sxs-lookup"><span data-stu-id="434a7-121">Optionally confirm the size of the property value with a call to [**IDXCoreAdapter::GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span></span> <span data-ttu-id="434a7-122">En el caso de una propiedad como **DXCoreAdapterProperty:: IsHardware**, que es un valor booleano simple, este paso no es necesario.</span><span class="sxs-lookup"><span data-stu-id="434a7-122">For a property such as **DXCoreAdapterProperty::IsHardware**, which is a simple Boolean, this step isn't necessary.</span></span>
- <span data-ttu-id="434a7-123">Y, por último, recupere el valor de la propiedad llamando a [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="434a7-123">And, finally, retrieve the property's value by calling [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

const uint32_t count{ d3D12CoreComputeAdapters->GetAdapterCount() };

for (uint32_t i = 0; i < count; ++i)
{
    winrt::com_ptr<IDXCoreAdapter> candidateAdapter;
    winrt::check_hresult(
        d3D12CoreComputeAdapters->GetAdapter(i, candidateAdapter.put()));

    bool isHardware{ false };
    winrt::check_hresult(candidateAdapter->GetProperty(
        DXCoreAdapterProperty::IsHardware,
        &isHardware));

    if (isHardware)
    {
        // Choose the first hardware adapter, and stop looping.
        preferredAdapter = candidateAdapter;
        break;
    }

    // Otherwise, ensure that (as long as there are *any* adapters) we'll
    // at least choose one.
    if (!preferredAdapter)
    {
        preferredAdapter = candidateAdapter;
    }
}
```

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a><span data-ttu-id="434a7-124">Seleccionar el adaptador preferido mediante la ordenación de una lista de adaptadores</span><span class="sxs-lookup"><span data-stu-id="434a7-124">Select the preferred adapter by sorting an adapter list</span></span>

<span data-ttu-id="434a7-125">Puede ordenar una lista de adaptadores de DXCore llamando al método [IDXCoreAdapterList:: Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) .</span><span class="sxs-lookup"><span data-stu-id="434a7-125">You can sort a DXCore adapter list by calling the [IDXCoreAdapterList::Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) method.</span></span>

<span data-ttu-id="434a7-126">La enumeración [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) define valores que representan criterios de ordenación.</span><span class="sxs-lookup"><span data-stu-id="434a7-126">The [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) enumeration defines values that representing sort criteria.</span></span> <span data-ttu-id="434a7-127">Pase una matriz de esos valores para **ordenar** y, a continuación, lea el primer adaptador en la lista ordenada resultante.</span><span class="sxs-lookup"><span data-stu-id="434a7-127">Pass an array of those values to **Sort**, and then read off the first adapter in the resulting sorted list.</span></span>

<span data-ttu-id="434a7-128">Para determinar si un tipo de ordenación se va a entender por **orden**, primero llame a [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span><span class="sxs-lookup"><span data-stu-id="434a7-128">To determine whether a sort type is going to be understood by **Sort**, first call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> TryFindHardwareHighPerformanceGraphicsAdapter()
{
    // You begin DXCore adapter enumeration by creating an adapter factory.
    winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
    winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));

    // From the factory, retrieve a list of all the Direct3D 12 Graphics adapters.
    winrt::com_ptr<IDXCoreAdapterList> d3D12GraphicsAdapters;
    GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS };
    winrt::check_hresult(
        adapterFactory->CreateAdapterList(_countof(attributes),
            attributes,
            d3D12GraphicsAdapters.put()));

    DXCoreAdapterPreference sortPreferences[]{
        DXCoreAdapterPreference::Hardware, DXCoreAdapterPreference::HighPerformance };

    // Ask the OS to sort for the highest performance hardware adapter.
    winrt::check_hresult(d3D12GraphicsAdapters->Sort(_countof(sortPreferences), sortPreferences));

    winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

    if (d3D12GraphicsAdapters->GetAdapterCount() > 0)
    {
        winrt::check_hresult(d3D12GraphicsAdapters->GetAdapter(0, preferredAdapter.put()));
    }

    return preferredAdapter;
}
```

## <a name="query-and-set-adapter-state-properties"></a><span data-ttu-id="434a7-129">Consulta y establecimiento del estado del adaptador (propiedades)</span><span class="sxs-lookup"><span data-stu-id="434a7-129">Query and set adapter state (properties)</span></span>

<span data-ttu-id="434a7-130">Puede recuperar y establecer el estado de un elemento de estado especificado de un adaptador llamando a los métodos [**IDXCoreAdapter:: QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) y [**IDXCoreAdapter:: SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) .</span><span class="sxs-lookup"><span data-stu-id="434a7-130">You can retrieve and set the state of a specified state item of an adapter by calling the [**IDXCoreAdapter::QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) and [**IDXCoreAdapter::SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) methods.</span></span>

```cppwinrt
void SetDesiredMemoryReservation(winrt::com_ptr<IDXCoreAdapter> const& adapter, uint64_t reservation)
{
    DXCoreAdapterMemoryBudgetNodeSegmentGroup nodeSegmentGroup{};
    nodeSegmentGroup.nodeIndex = 0;
    nodeSegmentGroup.segmentGroup = DXCoreSegmentGroup::Local;

    DXCoreAdapterMemoryBudget memoryBudget{};
    winrt::check_hresult(adapter->QueryState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &memoryBudget));

    // Clamp the reservation to what's available.
    reservation = std::min<uint64_t>(reservation, memoryBudget.availableForReservation);

    winrt::check_hresult(adapter->SetState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &reservation));
}
```

<span data-ttu-id="434a7-131">En la práctica, antes de llamar a **QueryState** y **SetState**, debe llamar a [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que la consulta de la clase de estado está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="434a7-131">In practice, before calling **QueryState** and **SetState**, you should call [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="adapter-list-freshness"></a><span data-ttu-id="434a7-132">Actualización de la lista de adaptadores</span><span class="sxs-lookup"><span data-stu-id="434a7-132">Adapter list freshness</span></span>

<span data-ttu-id="434a7-133">Si una lista de adaptadores se vuelve obsoleta debido a la modificación de las condiciones del sistema, se marcará como tal.</span><span class="sxs-lookup"><span data-stu-id="434a7-133">Should an adapter list become stale due to changing system conditions, it will be marked as such.</span></span> <span data-ttu-id="434a7-134">Puede determinar la actualización de la lista de adaptadores sondeando su método [**IDXCoreAdapterList:: IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) .</span><span class="sxs-lookup"><span data-stu-id="434a7-134">You can determine an adapter list's freshness by polling its [**IDXCoreAdapterList::IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) method.</span></span>

<span data-ttu-id="434a7-135">Sin embargo, de forma más cómoda, puede suscribirse a notificaciones para condiciones como la obsolescencia.</span><span class="sxs-lookup"><span data-stu-id="434a7-135">More conveniently, though, you can subscribe to notifications for conditions such as staleness.</span></span> <span data-ttu-id="434a7-136">Para ello, pase [**DXCoreNotificationType:: AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) a [**IDXCoreAdapterFactory:: RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)y almacene de forma segura la cookie devuelta para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="434a7-136">To do that, pass [**DXCoreNotificationType::AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) to [**IDXCoreAdapterFactory::RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), and safely store the returned cookie for use later.</span></span>

```cppwinrt
uint32_t m_eventCookie = 0;
...
winrt::check_hresult(factory->RegisterEventNotification(
    m_adapters.get(),
    DXCoreNotificationType::AdapterListStale,
    OnAdapterListStale,
    this,
    &m_eventCookie));
...
static void WINAPI OnAdapterListStale(
    DXCoreNotificationType notificationType,
    IUnknown* staleObject,
    void* context)
{
    ...
}
```

<span data-ttu-id="434a7-137">A continuación, puede generar un nuevo objeto de lista de adaptadores actual a partir del objeto de generador que ya tiene.</span><span class="sxs-lookup"><span data-stu-id="434a7-137">You can then generate a new, current, adapter list object from the factory object that you already have.</span></span> <span data-ttu-id="434a7-138">La administración de estas condiciones es fundamental para su capacidad de responder sin problemas a eventos como la llegada y eliminación de un adaptador (ya sea una GPU o un adaptador de proceso especializado) y para mover correctamente las cargas de trabajo en respuesta.</span><span class="sxs-lookup"><span data-stu-id="434a7-138">Handling these conditions is critical to your ability to seamlessly respond to events such as adapter arrival and removal (whether that be a GPU, or a specialized compute adapter), and to appropriately shift workloads in response.</span></span>

<span data-ttu-id="434a7-139">Antes de destruir el objeto de lista de adaptadores, debe usar el valor de cookie para anular el registro de ese objeto de las notificaciones mediante una llamada a [IDXCoreAdapterFactory:: UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span><span class="sxs-lookup"><span data-stu-id="434a7-139">Before you destroy the adapter list object, you must use the cookie value to unregister that object from notifications by calling [IDXCoreAdapterFactory::UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span></span> <span data-ttu-id="434a7-140">Si no se anula el registro, se produce una excepción grave cuando se detecta la situación.</span><span class="sxs-lookup"><span data-stu-id="434a7-140">If you don't unregister, then a fatal exception is raised when the situation is detected.</span></span>

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a><span data-ttu-id="434a7-141">Mostrar información</span><span class="sxs-lookup"><span data-stu-id="434a7-141">Display information</span></span>

> [!NOTE]
> <span data-ttu-id="434a7-142">DXCore no proporciona ninguna información de presentación.</span><span class="sxs-lookup"><span data-stu-id="434a7-142">DXCore doesn't itself provide any display information.</span></span> <span data-ttu-id="434a7-143">En caso necesario, debe usar la clase Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) para recuperar esta información.</span><span class="sxs-lookup"><span data-stu-id="434a7-143">Where necessary, you should use the Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) class to retrieve this information.</span></span> <span data-ttu-id="434a7-144">El [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) de un adaptador proporciona un identificador común que puede usar para asignar un adaptador de DXCore a la información de [**DisplayMonitor. DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) .</span><span class="sxs-lookup"><span data-stu-id="434a7-144">An adapter's [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) provides a common identifier that you can use to map a DXCore adapter to [**DisplayMonitor.DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) information.</span></span> <span data-ttu-id="434a7-145">Para obtener el LUID del adaptador, pase [**DXCoreAdapterProperty:: InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) al método [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="434a7-145">To obtain an adapter's LUID, pass [**DXCoreAdapterProperty::InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) to the [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="434a7-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="434a7-146">See also</span></span>

* [<span data-ttu-id="434a7-147">Aplicación DXCore mínima</span><span class="sxs-lookup"><span data-stu-id="434a7-147">Minimal DXCore application</span></span>](dxcore-source-code.md)
* [<span data-ttu-id="434a7-148">Referencia de DXCore</span><span class="sxs-lookup"><span data-stu-id="434a7-148">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="434a7-149">Gráficos de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="434a7-149">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)