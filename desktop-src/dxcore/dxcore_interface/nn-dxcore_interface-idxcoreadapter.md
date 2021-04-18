---
title: IDXCoreAdapter
description: La interfaz **IDXCoreAdapter**   implementa métodos para recuperar detalles sobre un elemento de adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149550"
---
# <a name="idxcoreadapter-interface"></a><span data-ttu-id="7cc8d-103">Interfaz IDXCoreAdapter</span><span class="sxs-lookup"><span data-stu-id="7cc8d-103">IDXCoreAdapter interface</span></span>

<span data-ttu-id="7cc8d-104">La interfaz **IDXCoreAdapter**   implementa métodos para recuperar detalles sobre un elemento de adaptador.</span><span class="sxs-lookup"><span data-stu-id="7cc8d-104">The **IDXCoreAdapter** interface implements methods for retrieving details about an adapter item.</span></span> <span data-ttu-id="7cc8d-105">**IDXCoreAdapter** hereda de la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7cc8d-105">**IDXCoreAdapter** inherits from the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7cc8d-106">Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="7cc8d-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7cc8d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7cc8d-107">Remarks</span></span>

<span data-ttu-id="7cc8d-108">Las propiedades de un adaptador se establecen en el momento en que se inicia el adaptador y son inmutables mientras dure el adaptador.</span><span class="sxs-lookup"><span data-stu-id="7cc8d-108">An adapter's properties are established at the time the adapter starts, and they're immutable for the lifetime of the adapter.</span></span> <span data-ttu-id="7cc8d-109">Esto contrasta con el estado de un adaptador, que se puede consultar o establecer, y los valores de que pueden cambiar con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="7cc8d-109">This is in contrast to an adapter's state, which can be queried or set, and the values of which can change over time.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cc8d-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cc8d-110">See also</span></span>

<span data-ttu-id="7cc8d-111">[Referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="7cc8d-111">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>