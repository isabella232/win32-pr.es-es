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
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a><span data-ttu-id="0007e-103">IDXCoreAdapterFactory:: IsNotificationTypeSupported (método)</span><span class="sxs-lookup"><span data-stu-id="0007e-103">IDXCoreAdapterFactory::IsNotificationTypeSupported method</span></span>

<span data-ttu-id="0007e-104">Determina si el sistema operativo (OS) admite un tipo de notificación especificado.</span><span class="sxs-lookup"><span data-stu-id="0007e-104">Determines whether a specified notification type is supported by the operating system (OS).</span></span> <span data-ttu-id="0007e-105">Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="0007e-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0007e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0007e-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a><span data-ttu-id="0007e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0007e-107">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="0007e-108">notificationType</span><span class="sxs-lookup"><span data-stu-id="0007e-108">notificationType</span></span>

<span data-ttu-id="0007e-109">Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="0007e-109">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="0007e-110">El tipo de notificación sobre el que se está consultando el soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="0007e-110">The type of notification that you're querying about support for.</span></span> <span data-ttu-id="0007e-111">Vea la tabla en [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) para obtener información sobre los tipos de notificación.</span><span class="sxs-lookup"><span data-stu-id="0007e-111">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about the notification types.</span></span>

## <a name="returns"></a><span data-ttu-id="0007e-112">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="0007e-112">Returns</span></span>

<span data-ttu-id="0007e-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="0007e-113">Type: **bool**</span></span>

<span data-ttu-id="0007e-114">Devuelve  `true`   si el tipo de notificación es compatible con el sistema.</span><span class="sxs-lookup"><span data-stu-id="0007e-114">Returns `true` if the notification type is supported by the system.</span></span> <span data-ttu-id="0007e-115">De lo contrario, devuelve  `false` .</span><span class="sxs-lookup"><span data-stu-id="0007e-115">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="0007e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0007e-116">Remarks</span></span>

<span data-ttu-id="0007e-117">Puede llamar a **IsNotificationTypeSupported** para determinar si esta versión del sistema operativo conoce un tipo de notificación determinado.</span><span class="sxs-lookup"><span data-stu-id="0007e-117">You can call **IsNotificationTypeSupported** to determine whether a given notification type is known to this version of the OS.</span></span> <span data-ttu-id="0007e-118">Por ejemplo, un tipo de notificación que se introduce en una versión determinada de Windows se desconoce en versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="0007e-118">For example, a notification type that's introduced in a particular version of Windows is unknown to previous versions of Windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="0007e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0007e-119">See also</span></span>

<span data-ttu-id="0007e-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore GUID Attribute GUID](../dxcore-adapter-attribute-guids.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="0007e-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>