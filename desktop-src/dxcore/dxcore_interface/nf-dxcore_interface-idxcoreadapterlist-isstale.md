---
title: IDXCoreAdapterList::IsStale
description: Determina si los cambios en este sistema han dado lugar a que este objeto de lista de adaptadores de DXCore esté obsoleto.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68b4e4ba6f3434f76ea5b4a2a98ae4e83486f61e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720172"
---
# <a name="idxcoreadapterlistisstale-method"></a><span data-ttu-id="2f44e-103">IDXCoreAdapterList:: IsStale (método)</span><span class="sxs-lookup"><span data-stu-id="2f44e-103">IDXCoreAdapterList::IsStale method</span></span>

<span data-ttu-id="2f44e-104">Determina si los cambios en este sistema han dado lugar a que este objeto de lista de adaptadores de DXCore esté obsoleto.</span><span class="sxs-lookup"><span data-stu-id="2f44e-104">Determines whether changes to this system have resulted in this DXCore adapter list object becoming out of date.</span></span> <span data-ttu-id="2f44e-105">Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="2f44e-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f44e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f44e-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a><span data-ttu-id="2f44e-107">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="2f44e-107">Returns</span></span>

<span data-ttu-id="2f44e-108">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="2f44e-108">Type: **bool**</span></span>

<span data-ttu-id="2f44e-109">Devuelve  `true`   si, desde que se genera la lista, se han producido cambios en las condiciones del sistema que podrían provocar que esta lista de adaptadores se quedara obsoleta.</span><span class="sxs-lookup"><span data-stu-id="2f44e-109">Returns `true` if, since generating the list, changes to system conditions have occurred that would cause this adapter list to become stale.</span></span> <span data-ttu-id="2f44e-110">De lo contrario, devuelve  `false` .</span><span class="sxs-lookup"><span data-stu-id="2f44e-110">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f44e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f44e-111">Remarks</span></span>

<span data-ttu-id="2f44e-112">Puede sondear **IsStale** para determinar si el cambio de condiciones del sistema ha provocado que esta lista no esté actualizada.</span><span class="sxs-lookup"><span data-stu-id="2f44e-112">You can poll **IsStale** to determine whether changing system conditions have led to this list becoming out of date.</span></span> <span data-ttu-id="2f44e-113">Si **IsStale** devuelve `true` una vez, devuelve `true` para la duración restante del objeto de lista de adaptadores de DXCore.</span><span class="sxs-lookup"><span data-stu-id="2f44e-113">If **IsStale** returns `true` once, then it returns `true` for the remaining lifetime of the DXCore adapter list object.</span></span> <span data-ttu-id="2f44e-114">Un objeto de lista obsoleto se sigue considerando obsoleto aunque las condiciones del sistema vuelvan a un estado que coincida con la lista (las mismas condiciones se obtienen ahora como cuando se generó la lista por primera vez).</span><span class="sxs-lookup"><span data-stu-id="2f44e-114">A stale list object is still considered stale even if system conditions return to a state that matches the list (the same conditions obtain now as did when the list was first generated).</span></span>

## <a name="see-also"></a><span data-ttu-id="2f44e-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f44e-115">See also</span></span>

<span data-ttu-id="2f44e-116">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="2f44e-116">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>