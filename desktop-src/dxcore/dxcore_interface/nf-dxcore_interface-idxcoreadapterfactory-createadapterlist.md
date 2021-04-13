---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Genera una lista de objetos de adaptador que representan el estado actual del adaptador del sistema y que cumplen los criterios especificados.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488035"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a><span data-ttu-id="b9207-103">IDXCoreAdapterFactory:: CreateAdapterList (método)</span><span class="sxs-lookup"><span data-stu-id="b9207-103">IDXCoreAdapterFactory::CreateAdapterList method</span></span>

<span data-ttu-id="b9207-104">Genera una lista de objetos de adaptador que representan el estado actual del adaptador del sistema y que cumplen los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="b9207-104">Generates a list of adapter objects representing the current adapter state of the system, and meeting the criteria specified.</span></span> <span data-ttu-id="b9207-105">Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="b9207-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9207-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9207-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a><span data-ttu-id="b9207-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9207-107">Parameters</span></span>

### <a name="numattributes"></a><span data-ttu-id="b9207-108">numAttributes</span><span class="sxs-lookup"><span data-stu-id="b9207-108">numAttributes</span></span>

<span data-ttu-id="b9207-109">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="b9207-109">Type: **uint32_t**</span></span>

<span data-ttu-id="b9207-110">Número de elementos de la matriz a los que apunta el argumento *filterAttributes* .</span><span class="sxs-lookup"><span data-stu-id="b9207-110">The number of elements in the array pointed to by the *filterAttributes* argument.</span></span>

### <a name="filterattributes-in"></a><span data-ttu-id="b9207-111">filterAttributes [in]</span><span class="sxs-lookup"><span data-stu-id="b9207-111">filterAttributes [in]</span></span>

<span data-ttu-id="b9207-112">Tipo: **GUID \* const**</span><span class="sxs-lookup"><span data-stu-id="b9207-112">Type: **const GUID\***</span></span>

<span data-ttu-id="b9207-113">Puntero a una matriz de GUID de atributo de adaptador.</span><span class="sxs-lookup"><span data-stu-id="b9207-113">A pointer to an array of adapter attribute GUIDs.</span></span> <span data-ttu-id="b9207-114">Para obtener una lista de los GUID de atributo, consulte [GUID del atributo del adaptador de DXCore](../dxcore-adapter-attribute-guids.md).</span><span class="sxs-lookup"><span data-stu-id="b9207-114">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span> <span data-ttu-id="b9207-115">Se debe proporcionar al menos un GUID.</span><span class="sxs-lookup"><span data-stu-id="b9207-115">At least one GUID must be provided.</span></span> <span data-ttu-id="b9207-116">En el caso de que se proporcione más de un GUID en la matriz, solo se incluirán en la lista devuelta los adaptadores que cumplan *todos* los atributos solicitados.</span><span class="sxs-lookup"><span data-stu-id="b9207-116">In the case that more than one GUID is provided in the array, only adapters that meet *all* of the requested attributes will be included in the returned list.</span></span>

### <a name="riid"></a><span data-ttu-id="b9207-117">riid</span><span class="sxs-lookup"><span data-stu-id="b9207-117">riid</span></span>

<span data-ttu-id="b9207-118">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="b9207-118">Type: **REFIID**</span></span>

<span data-ttu-id="b9207-119">Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvAdapterList*.</span><span class="sxs-lookup"><span data-stu-id="b9207-119">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapterList*.</span></span> <span data-ttu-id="b9207-120">Se espera que sea el identificador de interfaz (IID) de [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).</span><span class="sxs-lookup"><span data-stu-id="b9207-120">This is expected to be the interface identifier (IID) of [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).</span></span>

### <a name="ppvadapterlist-out"></a><span data-ttu-id="b9207-121">ppvAdapterList [out]</span><span class="sxs-lookup"><span data-stu-id="b9207-121">ppvAdapterList [out]</span></span>

<span data-ttu-id="b9207-122">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="b9207-122">Type: **void\*\***</span></span>

<span data-ttu-id="b9207-123">Dirección de un puntero a una interfaz con el IID especificado en el parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="b9207-123">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="b9207-124">Si la devolución es correcta, *\* ppvAdapterList* (la dirección desreferenciada) contiene un puntero a la lista de adaptadores creada.</span><span class="sxs-lookup"><span data-stu-id="b9207-124">Upon successful return, *\*ppvAdapterList* (the dereferenced address) contains a pointer to the adapter list created.</span></span>

## <a name="returns"></a><span data-ttu-id="b9207-125">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="b9207-125">Returns</span></span>

<span data-ttu-id="b9207-126">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="b9207-126">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="b9207-127">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="b9207-127">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="b9207-128">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b9207-128">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="b9207-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9207-129">Return value</span></span>|<span data-ttu-id="b9207-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9207-130">Description</span></span>|
|-|-|
|<span data-ttu-id="b9207-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b9207-131">E_INVALIDARG</span></span>|<span data-ttu-id="b9207-132">`nullptr` se proporcionó para *filterAttributes* o se proporcionó 0 para *numAttributes*.</span><span class="sxs-lookup"><span data-stu-id="b9207-132">`nullptr` was provided for *filterAttributes*, or 0 was provided for *numAttributes*.</span></span>|
|<span data-ttu-id="b9207-133">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="b9207-133">E_NOINTERFACE</span></span>|<span data-ttu-id="b9207-134">Se proporcionó un valor no válido para *riid*.</span><span class="sxs-lookup"><span data-stu-id="b9207-134">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="b9207-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="b9207-135">E_POINTER</span></span>|<span data-ttu-id="b9207-136">`nullptr` se proporcionó para *ppvAdapterList*.</span><span class="sxs-lookup"><span data-stu-id="b9207-136">`nullptr` was provided for *ppvAdapterList*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b9207-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9207-137">Remarks</span></span>

<span data-ttu-id="b9207-138">Aunque no se encuentre ningún adaptador, siempre y cuando los argumentos sean válidos, **CreateAdapterList** crea un objeto [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) válido y devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="b9207-138">Even if no adapters are found, as long as the arguments are valid, **CreateAdapterList** creates a valid [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object, and returns **S_OK**.</span></span> <span data-ttu-id="b9207-139">Una vez generados, los adaptadores de esta lista específica no cambiarán.</span><span class="sxs-lookup"><span data-stu-id="b9207-139">Once generated, the adapters in this specific list won't change.</span></span> <span data-ttu-id="b9207-140">Pero la lista se considerará obsoleta si uno de los adaptadores deja de ser válido, o si llega un nuevo adaptador que cumpla los criterios de filtro proporcionados.</span><span class="sxs-lookup"><span data-stu-id="b9207-140">But the list will be considered stale if one of the adapters later becomes invalid, or if a new adapter arrives that meets the provided filter criteria.</span></span> <span data-ttu-id="b9207-141">La lista devuelta por **CreateAdapterList** no se ordena de ninguna manera determinada, pero el orden de una lista es coherente entre varias llamadas e incluso entre reinicios del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b9207-141">The list returned by **CreateAdapterList** is not ordered in any particular way, but the ordering of a list is consistent across multiple calls, and even across operating system restarts.</span></span> <span data-ttu-id="b9207-142">El orden puede variar tras los cambios de configuración del sistema, incluida la adición o eliminación de un adaptador, o la actualización de un controlador en un adaptador existente.</span><span class="sxs-lookup"><span data-stu-id="b9207-142">The ordering may change upon system configuration changes, including the addition or removal of an adapter, or a driver update on an existing adapter.</span></span> <span data-ttu-id="b9207-143">Puede registrarse para estos cambios con [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) mediante el tipo de notificación **DXCoreNotificationType. AdapterListStale**.</span><span class="sxs-lookup"><span data-stu-id="b9207-143">You can register for these changes with [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) using the notification type **DXCoreNotificationType.AdapterListStale**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9207-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9207-144">See also</span></span>

<span data-ttu-id="b9207-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore GUID Attribute GUID](../dxcore-adapter-attribute-guids.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="b9207-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>