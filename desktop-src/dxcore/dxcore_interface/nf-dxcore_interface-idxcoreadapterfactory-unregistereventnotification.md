---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Anula el registro de una notificación a la que se registró anteriormente.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421205"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a><span data-ttu-id="bf7d9-103">IDXCoreAdapterFactory:: UnregisterEventNotification (método)</span><span class="sxs-lookup"><span data-stu-id="bf7d9-103">IDXCoreAdapterFactory::UnregisterEventNotification method</span></span>

<span data-ttu-id="bf7d9-104">Anula el registro de una notificación a la que se registró anteriormente.</span><span class="sxs-lookup"><span data-stu-id="bf7d9-104">Unregisters from a notification that you previously registered for.</span></span> <span data-ttu-id="bf7d9-105">Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="bf7d9-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf7d9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf7d9-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a><span data-ttu-id="bf7d9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf7d9-107">Parameters</span></span>

### <a name="eventcookie"></a><span data-ttu-id="bf7d9-108">eventCookie</span><span class="sxs-lookup"><span data-stu-id="bf7d9-108">eventCookie</span></span>

<span data-ttu-id="bf7d9-109">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="bf7d9-109">Type: **uint32_t**</span></span>

<span data-ttu-id="bf7d9-110">El valor de cookie (que se devuelve cuando llamó a [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) que representa un registro anterior para el que desea anular el registro.</span><span class="sxs-lookup"><span data-stu-id="bf7d9-110">The cookie value (returned when you called [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) representing a prior registration that you now wish to unregister for.</span></span>

## <a name="returns"></a><span data-ttu-id="bf7d9-111">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="bf7d9-111">Returns</span></span>

<span data-ttu-id="bf7d9-112">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="bf7d9-112">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="bf7d9-113">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="bf7d9-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="bf7d9-114">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="bf7d9-114">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="bf7d9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf7d9-115">Return value</span></span>|<span data-ttu-id="bf7d9-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf7d9-116">Description</span></span>|
|-|-|
|<span data-ttu-id="bf7d9-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="bf7d9-117">E_INVALIDARG</span></span>|<span data-ttu-id="bf7d9-118">El valor de *eventCookie* no es una cookie válida que representa un registro anterior.</span><span class="sxs-lookup"><span data-stu-id="bf7d9-118">The value of *eventCookie* is not a valid cookie representing a prior registration.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bf7d9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf7d9-119">Remarks</span></span>

<span data-ttu-id="bf7d9-120">**UnregisterEventNotification** devuelve solo después de que se hayan completado todas las devoluciones de llamada pendientes o en curso para este registro.</span><span class="sxs-lookup"><span data-stu-id="bf7d9-120">**UnregisterEventNotification** returns only after all pending/in-progress callbacks for this registration have completed.</span></span> <span data-ttu-id="bf7d9-121">DXCore garantiza que no se producirán nuevas devoluciones de llamada para este registro después de que se devuelva **UnregisterEventNotification** .</span><span class="sxs-lookup"><span data-stu-id="bf7d9-121">DXCore guarantees that no new callbacks will occur for this registration after **UnregisterEventNotification** has returned.</span></span> <span data-ttu-id="bf7d9-122">Sin embargo, para evitar un interbloqueo, si llama a **UnregisterEventNotification** desde dentro de la devolución de llamada, **UnregisterEventNotification** no espera a que se complete la devolución de llamada activa.</span><span class="sxs-lookup"><span data-stu-id="bf7d9-122">However, to avoid a deadlock, if you call **UnregisterEventNotification** from within your callback, then **UnregisterEventNotification** doesn't wait for the active callback to complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf7d9-123">Antes de destruir el objeto DXCore representado por el argumento *dxCoreObject* pasado a [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), debe usar el valor de cookie para anular el registro de ese objeto de las notificaciones mediante una llamada a **UnregisterEventNotification**.</span><span class="sxs-lookup"><span data-stu-id="bf7d9-123">Before you destroy the DXCore object represented by the *dxCoreObject* argument passed to [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), you must use the cookie value to unregister that object from notifications by calling **UnregisterEventNotification**.</span></span> <span data-ttu-id="bf7d9-124">Si no lo hace, se produce una excepción grave cuando se detecta la situación.</span><span class="sxs-lookup"><span data-stu-id="bf7d9-124">If you don't do that, then a fatal exception is raised when the situation is detected.</span></span>

<span data-ttu-id="bf7d9-125">Una vez que se anula el registro de un valor de cookie, ese valor se puede seleccionar para que lo devuelva un registro subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="bf7d9-125">Once you unregister a cookie value, that value is then eligible for being returned by a subsequent registration</span></span>

## <a name="see-also"></a><span data-ttu-id="bf7d9-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf7d9-126">See also</span></span>

<span data-ttu-id="bf7d9-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="bf7d9-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>