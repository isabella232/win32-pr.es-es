---
title: IDXCoreAdapter::IsValid
description: Determina si este objeto de adaptador DXCore sigue siendo válido.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f58d8607b75253efda2e111eb358f576d36b65f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078130"
---
# <a name="idxcoreadapterisvalid-method"></a><span data-ttu-id="28580-103">IDXCoreAdapter:: IsValid (método)</span><span class="sxs-lookup"><span data-stu-id="28580-103">IDXCoreAdapter::IsValid method</span></span>

<span data-ttu-id="28580-104">Determina si este objeto de adaptador DXCore sigue siendo válido.</span><span class="sxs-lookup"><span data-stu-id="28580-104">Determines whether this DXCore adapter object is still valid.</span></span> <span data-ttu-id="28580-105">Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="28580-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="28580-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28580-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a><span data-ttu-id="28580-107">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="28580-107">Returns</span></span>

<span data-ttu-id="28580-108">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="28580-108">Type: **bool**</span></span>

<span data-ttu-id="28580-109">Devuelve  `true`   si este objeto de adaptador de DXCore sigue siendo válido.</span><span class="sxs-lookup"><span data-stu-id="28580-109">Returns `true` if this DXCore adapter object is still valid.</span></span> <span data-ttu-id="28580-110">De lo contrario, devuelve  `false` .</span><span class="sxs-lookup"><span data-stu-id="28580-110">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="28580-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="28580-111">See also</span></span>

<span data-ttu-id="28580-112">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="28580-112">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>