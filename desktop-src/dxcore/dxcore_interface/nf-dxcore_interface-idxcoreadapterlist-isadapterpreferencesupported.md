---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Determina si el sistema operativo entiende un valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792178"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a><span data-ttu-id="e8329-103">IDXCoreAdapterList:: IsAdapterPreferenceSupported (método)</span><span class="sxs-lookup"><span data-stu-id="e8329-103">IDXCoreAdapterList::IsAdapterPreferenceSupported method</span></span>

## <a name="description"></a><span data-ttu-id="e8329-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8329-104">Description</span></span>

<span data-ttu-id="e8329-105">Determina si el sistema operativo (OS) actual entiende el valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="e8329-105">Determines whether a specified [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value is understood by the current operating system (OS).</span></span> <span data-ttu-id="e8329-106">Puede llamar a **IsAdapterPreferenceSupported** antes de llamar a [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span><span class="sxs-lookup"><span data-stu-id="e8329-106">You can call **IsAdapterPreferenceSupported** before calling [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8329-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8329-107">Syntax</span></span>

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a><span data-ttu-id="e8329-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8329-108">Parameters</span></span>

### <a name="preference"></a><span data-ttu-id="e8329-109">preference</span><span class="sxs-lookup"><span data-stu-id="e8329-109">preference</span></span>

<span data-ttu-id="e8329-110">Tipo: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span><span class="sxs-lookup"><span data-stu-id="e8329-110">Type: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span></span>

<span data-ttu-id="e8329-111">Un valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) que se comprobará para ver si es compatible con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e8329-111">A [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value that will be checked to see whether it's supported by the OS.</span></span>

## <a name="returns"></a><span data-ttu-id="e8329-112">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="e8329-112">Returns</span></span>

<span data-ttu-id="e8329-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="e8329-113">Type: **bool**</span></span>

<span data-ttu-id="e8329-114">Devuelve `true` si el tipo de ordenación lo entiende el sistema operativo actual.</span><span class="sxs-lookup"><span data-stu-id="e8329-114">Returns `true` if the sort type is understood by the current OS.</span></span> <span data-ttu-id="e8329-115">De lo contrario, devuelve `false`.</span><span class="sxs-lookup"><span data-stu-id="e8329-115">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8329-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8329-116">See also</span></span>

<span data-ttu-id="e8329-117">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="e8329-117">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>