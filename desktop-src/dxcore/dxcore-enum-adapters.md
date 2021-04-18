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
# <a name="using-dxcore-to-enumerate-adapters"></a>Uso de DXCore para enumerar adaptadores

DXCore es una API de enumeración de adaptadores para dispositivos DirectX, por lo que algunas de sus funciones se superponen con las de [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).

DXCore permite la exposición de nuevos tipos de dispositivos al modo de usuario, como MCDM (modelo de controladores de Microsoft Compute), para su uso con [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md)y [Windows machine learning](/windows/ai/windows-ml/). DXCore, a diferencia de DXGI, no proporciona ninguna información sobre la tecnología o las propiedades relacionadas con la pantalla.

En las siguientes secciones, echaremos un vistazo a las principales características de DXCore con algunos ejemplos de código (escritos en [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)). Los ejemplos de código que se muestran a continuación se extraen de la lista de código fuente completa que puede encontrar en el tema [aplicación DXCore mínima](dxcore-source-code.md).

## <a name="create-an-adapter-factory"></a>Crear un generador de adaptadores

La enumeración del adaptador de DXCore se inicia mediante la creación de un objeto de generador de adaptadores, que se representa mediante la interfaz [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) . Para crear un generador, incluya el `dxcore.h` archivo de encabezado y llame a la función Free de [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) .

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a>Recuperar una lista de adaptadores

A diferencia de lo que ocurre con DXGI, un generador de adaptadores de DXCore recién creado no crea automáticamente una instantánea del estado del adaptador del sistema. En su lugar, DXCore crea esa instantánea cuando se recupera explícitamente un objeto de lista de adaptadores, que se representa mediante la interfaz [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) .

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a>Seleccionar un adaptador apropiado de la lista

En esta sección se muestra cómo, dado un objeto de lista de adaptadores, podría encontrar el primer adaptador de hardware de la lista.

El método [**IDXCoreAdapterList:: GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) indica el número de elementos de la lista y [**IDXCoreAdapterList:: GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) recupera un adaptador específico por índice.

Después, puede consultar las propiedades de ese adaptador siguiendo estos pasos.

- En primer lugar, para confirmar que es válido recuperar el valor de una propiedad determinada para este adaptador en esta versión del sistema operativo, llame a [**IDXCoreAdapter:: IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md). Pase un valor de la enumeración [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) para identificar la propiedad sobre la que está consultando.
- Opcionalmente, confirme el tamaño del valor de propiedad con una llamada a [**IDXCoreAdapter:: GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md). En el caso de una propiedad como **DXCoreAdapterProperty:: IsHardware**, que es un valor booleano simple, este paso no es necesario.
- Y, por último, recupere el valor de la propiedad llamando a [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).

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

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a>Seleccionar el adaptador preferido mediante la ordenación de una lista de adaptadores

Puede ordenar una lista de adaptadores de DXCore llamando al método [IDXCoreAdapterList:: Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) .

La enumeración [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) define valores que representan criterios de ordenación. Pase una matriz de esos valores para **ordenar** y, a continuación, lea el primer adaptador en la lista ordenada resultante.

Para determinar si un tipo de ordenación se va a entender por **orden**, primero llame a [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

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

## <a name="query-and-set-adapter-state-properties"></a>Consulta y establecimiento del estado del adaptador (propiedades)

Puede recuperar y establecer el estado de un elemento de estado especificado de un adaptador llamando a los métodos [**IDXCoreAdapter:: QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) y [**IDXCoreAdapter:: SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) .

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

En la práctica, antes de llamar a **QueryState** y **SetState**, debe llamar a [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que la consulta de la clase de estado está disponible para este adaptador y sistema operativo (SO).

## <a name="adapter-list-freshness"></a>Actualización de la lista de adaptadores

Si una lista de adaptadores se vuelve obsoleta debido a la modificación de las condiciones del sistema, se marcará como tal. Puede determinar la actualización de la lista de adaptadores sondeando su método [**IDXCoreAdapterList:: IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) .

Sin embargo, de forma más cómoda, puede suscribirse a notificaciones para condiciones como la obsolescencia. Para ello, pase [**DXCoreNotificationType:: AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) a [**IDXCoreAdapterFactory:: RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)y almacene de forma segura la cookie devuelta para su uso posterior.

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

A continuación, puede generar un nuevo objeto de lista de adaptadores actual a partir del objeto de generador que ya tiene. La administración de estas condiciones es fundamental para su capacidad de responder sin problemas a eventos como la llegada y eliminación de un adaptador (ya sea una GPU o un adaptador de proceso especializado) y para mover correctamente las cargas de trabajo en respuesta.

Antes de destruir el objeto de lista de adaptadores, debe usar el valor de cookie para anular el registro de ese objeto de las notificaciones mediante una llamada a [IDXCoreAdapterFactory:: UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Si no se anula el registro, se produce una excepción grave cuando se detecta la situación.

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a>Mostrar información

> [!NOTE]
> DXCore no proporciona ninguna información de presentación. En caso necesario, debe usar la clase Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) para recuperar esta información. El [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) de un adaptador proporciona un identificador común que puede usar para asignar un adaptador de DXCore a la información de [**DisplayMonitor. DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) . Para obtener el LUID del adaptador, pase [**DXCoreAdapterProperty:: InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) al método [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) .

## <a name="see-also"></a>Vea también

* [Aplicación DXCore mínima](dxcore-source-code.md)
* [Referencia de DXCore](./dxcore-reference.md)
* [Gráficos de Direct3D 12](../direct3d12/direct3d-12-graphics.md)