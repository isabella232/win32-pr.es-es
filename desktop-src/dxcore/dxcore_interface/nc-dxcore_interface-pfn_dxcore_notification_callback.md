---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Función de devolución de llamada (implementada por la aplicación), a la que llama un objeto DXCore para eventos de notificación.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 01d65f6907c60d6c68b612308b9105d18bbe037f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995507"
---
# <a name="pfn_dxcore_notification_callback-callback"></a><span data-ttu-id="eb974-103">Devolución de llamada PFN_DXCORE_NOTIFICATION_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="eb974-103">PFN_DXCORE_NOTIFICATION_CALLBACK callback</span></span>

<span data-ttu-id="eb974-104">Función de devolución de llamada (implementada por la aplicación), a la que llama un objeto DXCore para eventos de notificación.</span><span class="sxs-lookup"><span data-stu-id="eb974-104">A callback function (implemented by your application), which is called by a DXCore object for notification events.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb974-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb974-105">Syntax</span></span>

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a><span data-ttu-id="eb974-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb974-106">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="eb974-107">notificationType</span><span class="sxs-lookup"><span data-stu-id="eb974-107">notificationType</span></span>

<span data-ttu-id="eb974-108">Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="eb974-108">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="eb974-109">El tipo de notificación que representa esta invocación.</span><span class="sxs-lookup"><span data-stu-id="eb974-109">The type of notification representing this invocation.</span></span> <span data-ttu-id="eb974-110">Vea la tabla en [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) para obtener información sobre los tipos válidos con qué tipos de objetos.</span><span class="sxs-lookup"><span data-stu-id="eb974-110">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about what types are valid with which kinds of objects.</span></span>

### <a name="object"></a><span data-ttu-id="eb974-111">object</span><span class="sxs-lookup"><span data-stu-id="eb974-111">object</span></span>

<span data-ttu-id="eb974-112">Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="eb974-112">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="eb974-113">El objeto [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) que genera la notificación.</span><span class="sxs-lookup"><span data-stu-id="eb974-113">The [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) or [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object raising the notification.</span></span>

### <a name="context-in"></a><span data-ttu-id="eb974-114">contexto [in]</span><span class="sxs-lookup"><span data-stu-id="eb974-114">context [in]</span></span>

<span data-ttu-id="eb974-115">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="eb974-115">Type: **void\***</span></span>

<span data-ttu-id="eb974-116">Un puntero, que puede ser `nullptr` , a un objeto que contiene información de contexto.</span><span class="sxs-lookup"><span data-stu-id="eb974-116">A pointer, which may be `nullptr`, to an object containing context info.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb974-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb974-117">See also</span></span>

<span data-ttu-id="eb974-118">[Referencia](../dxcore-reference.md)de [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), DXCore, [usar DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="eb974-118">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>