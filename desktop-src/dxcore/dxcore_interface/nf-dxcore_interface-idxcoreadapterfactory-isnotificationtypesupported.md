---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Determina si el sistema operativo (OS) admite un tipo de notificación especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 78730167e7ec139733ee1e4011d2e5e59c32782b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359251"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a>IDXCoreAdapterFactory:: IsNotificationTypeSupported (método)

Determina si el sistema operativo (OS) admite un tipo de notificación especificado. Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

El tipo de notificación sobre el que se está consultando el soporte técnico. Vea la tabla en [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) para obtener información sobre los tipos de notificación.

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve  `true`   si el tipo de notificación es compatible con el sistema. De lo contrario, devuelve  `false` .

## <a name="remarks"></a>Observaciones

Puede llamar a **IsNotificationTypeSupported** para determinar si esta versión del sistema operativo conoce un tipo de notificación determinado. Por ejemplo, un tipo de notificación que se introduce en una versión determinada de Windows se desconoce en versiones anteriores de Windows.

## <a name="see-also"></a>Vea también

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore GUID Attribute GUID](../dxcore-adapter-attribute-guids.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)