---
title: DXCoreNotificationType
description: Define constantes que especifican los tipos de notificaciones generadas por los objetos [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) .
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3eacd77d2cf15c78a0dc959285874de943fd9130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149359"
---
# <a name="dxcorenotificationtype-enum"></a>Enumeración DXCoreNotificationType

Define constantes que especifican los tipos de notificaciones generadas por los objetos [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) .

Puede registrar y anular el registro de estas notificaciones mediante una llamada a [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) y [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), respectivamente.

## <a name="syntax"></a>Sintaxis

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

Esta notificación se genera mediante un objeto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">IDXCoreAdapterList</a> cuando la lista de adaptadores se vuelve obsoleta. La transición actualizada es unidireccional y una sola vez, por lo que esta notificación se genera como máximo una vez.

### <a name="adapternolongervalid"></a>AdapterNoLongerValid

Esta notificación se genera mediante un objeto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> cuando el adaptador deja de ser válido. La transición válida a no válida es unidireccional y una vez, por lo que esta notificación se genera como máximo una vez.

### <a name="adapterbudgetchange"></a>AdapterBudgetChange

Esta notificación se genera mediante un objeto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> cuando se produce un cambio de presupuesto de adaptador. Esta notificación puede producirse muchas veces. El uso de esta notificación es funcionalmente similar a <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3:: RegisterVideoMemoryBudgetChangeNotificationEvent</a>. En respuesta a este evento, debe llamar a [IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (con [DXCoreAdapterState:: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) para evaluar el estado actual del presupuesto de memoria.

### <a name="adapterhardwarecontentprotectionteardown"></a>AdapterHardwareContentProtectionTeardown

Esta notificación se genera mediante un objeto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> para notificar el desmontaje de la protección del contenido del hardware de un adaptador. Esta notificación puede producirse muchas veces. Es funcionalmente similar a <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3:: RegisterHardwareContentProtectionTeardownStatusEvent</a>. En respuesta a este evento, debe volver a evaluar el estado actual de la sesión de cifrado. por ejemplo, al llamar a [ID3D11VideoContext1:: CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) para determinar el impacto del montaje de hardware de una interfaz [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) específica.

## <a name="see-also"></a>Vea también

[IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)