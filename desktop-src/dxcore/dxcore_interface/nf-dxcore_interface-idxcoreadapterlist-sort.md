---
title: IDXCoreAdapterList::Sort
description: Ordena un objeto de lista de adaptadores de DXCore basándose en una matriz de entrada proporcionada de criterios de ordenación.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149551"
---
# <a name="idxcoreadapterlistsort-method"></a><span data-ttu-id="f8128-103">IDXCoreAdapterList:: sort (método)</span><span class="sxs-lookup"><span data-stu-id="f8128-103">IDXCoreAdapterList::Sort method</span></span>

## <a name="description"></a><span data-ttu-id="f8128-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8128-104">Description</span></span>

<span data-ttu-id="f8128-105">Ordena un objeto de lista de adaptadores de DXCore basándose en una matriz de entrada proporcionada de criterios de ordenación, donde los elementos de matriz situados antes en la matriz de criterios tienen un peso superior.</span><span class="sxs-lookup"><span data-stu-id="f8128-105">Sorts a DXCore adapter list object based on a provided input array of sort criteria, where array items earlier in the array of criteria are given a higher weight.</span></span> <span data-ttu-id="f8128-106">La **ordenación** le ayuda a encontrar más fácilmente el adaptador ideal en una lista de adaptadores.</span><span class="sxs-lookup"><span data-stu-id="f8128-106">**Sort** helps you to more easily find your ideal adapter in an adapter list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8128-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8128-107">Syntax</span></span>

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a><span data-ttu-id="f8128-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8128-108">Parameters</span></span>

### <a name="numpreferences"></a><span data-ttu-id="f8128-109">numPreferences</span><span class="sxs-lookup"><span data-stu-id="f8128-109">numPreferences</span></span>

<span data-ttu-id="f8128-110">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="f8128-110">Type: **uint32_t**</span></span>

<span data-ttu-id="f8128-111">Número de elementos que se encuentran en la matriz a la que apunta el parámetro *Preferences* .</span><span class="sxs-lookup"><span data-stu-id="f8128-111">The number of elements that are in the array pointed to by the *preferences* parameter.</span></span>

### <a name="preferences-in"></a><span data-ttu-id="f8128-112">preferencias [in]</span><span class="sxs-lookup"><span data-stu-id="f8128-112">preferences [in]</span></span>

<span data-ttu-id="f8128-113">Tipo: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8128-113">Type: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)\***</span></span>

<span data-ttu-id="f8128-114">Puntero a una matriz constante de valores de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) , que representa los criterios de ordenación.</span><span class="sxs-lookup"><span data-stu-id="f8128-114">A pointer to a constant array of [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) values, representing sort criteria.</span></span>

## <a name="returns"></a><span data-ttu-id="f8128-115">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="f8128-115">Returns</span></span>

<span data-ttu-id="f8128-116">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="f8128-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="f8128-117">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="f8128-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="f8128-118">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f8128-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="f8128-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8128-119">Return value</span></span>|<span data-ttu-id="f8128-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8128-120">Description</span></span>|
|-|-|
|<span data-ttu-id="f8128-121">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f8128-121">E_INVALIDARG</span></span>|<span data-ttu-id="f8128-122">El argumento *numPreferences* es cero o el argumento *Preferences* es `nullptr` .</span><span class="sxs-lookup"><span data-stu-id="f8128-122">The *numPreferences* argument is zero, or the *preferences* argument is `nullptr`.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f8128-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8128-123">Remarks</span></span>

<span data-ttu-id="f8128-124">En los casos en los que el sistema operativo (SO) no reconoce un valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) proporcionado, se omite y no se produce un error en la API.</span><span class="sxs-lookup"><span data-stu-id="f8128-124">In cases where a provided [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value isn't recognized by the operating system (OS), it is ignored, and won't cause the API to fail.</span></span> <span data-ttu-id="f8128-125">Los valores de **DXCoreAdapterPreference** conocidos se seguirán considerando en este caso.</span><span class="sxs-lookup"><span data-stu-id="f8128-125">Known **DXCoreAdapterPreference** values will still be considered in this case.</span></span> <span data-ttu-id="f8128-126">Para determinar si la API comprende un tipo de ordenación, llame a [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span><span class="sxs-lookup"><span data-stu-id="f8128-126">To determine whether a sort type is understood by the API, call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

<span data-ttu-id="f8128-127">Los valores de **DXCoreAdapterPreference** que se producen antes en la matriz de *preferencias* proporcionada se tratan con mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="f8128-127">**DXCoreAdapterPreference** values that occur earlier in the provided *preferences* array are treated with higher priority.</span></span> 

<span data-ttu-id="f8128-128">Consulte la documentación de la enumeración **DXCoreAdapterPreference** para obtener más información sobre la lógica que se aplica a cada tipo.</span><span class="sxs-lookup"><span data-stu-id="f8128-128">Refer to the **DXCoreAdapterPreference** enumeration documentation for details about what logic is applied for each type.</span></span> <span data-ttu-id="f8128-129">La lógica interna de un tipo puede desarrollar a medida que el sistema operativo desarrolla.</span><span class="sxs-lookup"><span data-stu-id="f8128-129">The internal logic for a type may develop as the OS develops.</span></span>

<span data-ttu-id="f8128-130">Cuando se devuelva el **orden** , los elementos de la lista de adaptadores de DXCore se ordenarán de la más preferible a la menos preferible.</span><span class="sxs-lookup"><span data-stu-id="f8128-130">When **Sort** returns, items in the DXCore adapter list will have been sorted from most preferable to least preferable.</span></span> <span data-ttu-id="f8128-131">Por lo tanto, al llamar a [IDXCoreAdapterList:: GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) con el índice 0 se recupera el adaptador que mejor coincida con los tipos de preferencia de ordenación solicitados. el índice 1 es la siguiente mejor coincidencia, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="f8128-131">So, calling [IDXCoreAdapterList::GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) with index 0 retrieves the adapter that best matches the requested sort preference types; index 1 is the next best match, and so on.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8128-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8128-132">See also</span></span>

<span data-ttu-id="f8128-133">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f8128-133">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>