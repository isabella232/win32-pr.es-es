---
title: DXCoreNotificationType
description: Define constantes que especifican tipos de notificaciones generados por objetos [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList.](./nn-dxcore_interface-idxcoreadapterlist.md)
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 230b6c103f83e72dfe0ba7803cde4b4695a32de724ce44c1aaccf5131d077bad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726015"
---
# <a name="dxcorenotificationtype-enum"></a>Enumeración DXCoreNotificationType

Define constantes que especifican tipos de notificaciones generados por objetos [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList.](./nn-dxcore_interface-idxcoreadapterlist.md)

Puede registrar y anular el registro de estas notificaciones llamando a [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) e [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), respectivamente.

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreNotificationType : uint32_t
{
  AdapterListStale = 0,
  AdapterNoLongerValid = 1,
  AdapterBudgetChange = 2,
  AdapterHardwareContentProtectionTeardown = 3
};
```

## <a name="constants"></a>Constantes

### <a name="adapterliststale"></a>AdapterListStale

Un objeto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">IDXCoreAdapterList</a> genera esta notificación cuando la lista de adaptadores se vuelve obsoleta. La transición de nuevo a obsoleto es un solo sentido y única, por lo que esta notificación se genera como máximo una vez.

### <a name="adapternolongervalid"></a>AdapterNoLongerValid

Esta notificación la genera un <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">objeto IDXCoreAdapter</a> cuando el adaptador deja de ser válido. La transición válida a no válida es un solo sentido y única, por lo que esta notificación se genera como máximo una vez.

### <a name="adapterbudgetchange"></a>AdapterBudgetChange

Un objeto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> genera esta notificación cuando se produce un cambio de presupuesto del adaptador. Esta notificación puede producirse muchas veces. El uso de esta notificación es funcionalmente similar a <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent</a>. En respuesta a este evento, debe llamar a [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (con [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) para evaluar el estado del presupuesto de memoria actual.

### <a name="adapterhardwarecontentprotectionteardown"></a>AdapterHardwareContentProtectionTeardown

Esta notificación la genera un objeto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> para notificar la desmontaje de la protección del contenido de hardware de un adaptador. Esta notificación puede producirse muchas veces. Es funcionalmente similar a <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent</a>. En respuesta a este evento, debe volver a evaluar el estado actual de la sesión de criptografía; Por ejemplo, mediante una llamada a [ID3D11VideoContext1::CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) para determinar el impacto de la cancelación de hardware para una interfaz [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) específica.

## <a name="see-also"></a>Vea también

[IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [IDXCoreAdapterFactory::UnregisterEventNotification,](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md) [IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [IDXCoreAdapterList,](./nn-dxcore_interface-idxcoreadapterlist.md) [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)