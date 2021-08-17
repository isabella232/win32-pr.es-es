---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Determina si el sistema operativo (SO) admite un tipo de notificación especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0c5097f89583f0f6b04e0e8fb033446aae45743a8fb5a7fe9134f34bcc5e05fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118709"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a>IDXCoreAdapterFactory::IsNotificationTypeSupported (método)

Determina si el sistema operativo (SO) admite un tipo de notificación especificado. Para obtener instrucciones de programación y ejemplos de código, vea [Uso de DXCore para enumerar adaptadores.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Tipo de notificación para la que está consultando sobre la compatibilidad. Consulte la tabla de [DXCoreNotificationType para](./ne-dxcore_interface-dxcorenotificationtype.md) obtener información sobre los tipos de notificación.

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve `true` si el sistema admite el tipo de notificación. De lo contrario, devuelve `false`.

## <a name="remarks"></a>Comentarios

Puede llamar a **IsNotificationTypeSupported** para determinar si esta versión del sistema operativo conoce un tipo de notificación determinado. Por ejemplo, un tipo de notificación que se introduce en una versión determinada de Windows es desconocido para las versiones anteriores de Windows.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapterFactory,](./nn-dxcore_interface-idxcoreadapterfactory.md) [DXCore Reference,](../dxcore-reference.md) [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)