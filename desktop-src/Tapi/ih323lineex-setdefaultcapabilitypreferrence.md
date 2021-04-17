---
description: Configura las preferencias de las funciones predeterminadas.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'IH323LineEx:: SetDefaultCapabilityPreferrence (método) (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679231"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a><span data-ttu-id="0d67e-103">IH323LineEx:: SetDefaultCapabilityPreferrence (método)</span><span class="sxs-lookup"><span data-stu-id="0d67e-103">IH323LineEx::SetDefaultCapabilityPreferrence method</span></span>

<span data-ttu-id="0d67e-104">\[**SetDefaultCapabilityPreferrence** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0d67e-104">\[**SetDefaultCapabilityPreferrence** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0d67e-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0d67e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0d67e-106">El método **SetDefaultCapabilityPreferrence** configura las preferencias de las funciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="0d67e-106">The **SetDefaultCapabilityPreferrence** method configures the preference of the default capabilities.</span></span> <span data-ttu-id="0d67e-107">Las capacidades tienen un peso predeterminado de 100.</span><span class="sxs-lookup"><span data-stu-id="0d67e-107">Capabilities have a default weight of 100.</span></span> <span data-ttu-id="0d67e-108">Si la aplicación especifica un mayor peso para una funcionalidad, tendrá una prioridad más alta durante la negociación H. 245.</span><span class="sxs-lookup"><span data-stu-id="0d67e-108">If the application specifies a higher weight for a capability, it will have a higher priority during the H.245 negotiation.</span></span> <span data-ttu-id="0d67e-109">Si la aplicación establece el peso de una capacidad en 0, no se utilizará en la negociación H. 245.</span><span class="sxs-lookup"><span data-stu-id="0d67e-109">If the application sets the weight of a capability to 0, it will not be used in the H.245 negotiation.</span></span>

<span data-ttu-id="0d67e-110">Este método es acumulativo.</span><span class="sxs-lookup"><span data-stu-id="0d67e-110">This method is cumulative.</span></span> <span data-ttu-id="0d67e-111">Por ejemplo, si se llama primero a este método para deshabilitar una funcionalidad y se llama de nuevo para deshabilitar otra, ambas funciones se deshabilitarán como resultado de estas dos llamadas.</span><span class="sxs-lookup"><span data-stu-id="0d67e-111">For example, if this method is called first to disable a capability and is called again to disable another, both capabilities will be disabled as the result of these two calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d67e-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d67e-112">Syntax</span></span>


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="0d67e-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d67e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d67e-114">*dwNumCaps* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d67e-114">*dwNumCaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d67e-115">Valor **DWORD** que contiene el número de funciones establecidas con este método.</span><span class="sxs-lookup"><span data-stu-id="0d67e-115">A **DWORD** value that contains the number of capabilities set with this method.</span></span>

</dd> <dt>

<span data-ttu-id="0d67e-116">*pCapabilities* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d67e-116">*pCapabilities* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d67e-117">Una matriz de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="0d67e-117">An array of capabilities.</span></span> <span data-ttu-id="0d67e-118">Cada elemento de la matriz es un valor de [**\_ capacidad de H245**](h245-capability.md) .</span><span class="sxs-lookup"><span data-stu-id="0d67e-118">Each element of the array is an [**H245\_CAPABILITY**](h245-capability.md) value.</span></span>

</dd> <dt>

<span data-ttu-id="0d67e-119">*pWeights* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d67e-119">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d67e-120">Matriz de pesos asociados a las funciones.</span><span class="sxs-lookup"><span data-stu-id="0d67e-120">An array of weights associated with the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d67e-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d67e-121">Return value</span></span>

<span data-ttu-id="0d67e-122">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0d67e-122">This method can return one of these values.</span></span>



| <span data-ttu-id="0d67e-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0d67e-123">Return code</span></span>                                                                                   | <span data-ttu-id="0d67e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d67e-124">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d67e-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0d67e-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0d67e-126">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0d67e-126">Method succeeded.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="0d67e-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0d67e-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0d67e-128">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="0d67e-128">Insufficient memory exists to perform the operation.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="0d67e-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0d67e-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0d67e-130">El parámetro *pCapabilities* es **null**, el parámetro *pWeights* es **null**, o bien *pCapabilities* y *pWeights* son **null**, o bien la matriz pCapabilities contiene un objeto de funcionalidad H. 245 no válido.</span><span class="sxs-lookup"><span data-stu-id="0d67e-130">The *pCapabilities* parameter is **NULL**, or the *pWeights* parameter is **NULL**, or both *pCapabilities* and *pWeights* are **NULL**, or the pCapabilities array contains an invalid H.245 capability object.</span></span><br/> |
| <dl> <span data-ttu-id="0d67e-131"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="0d67e-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0d67e-132">No se puede leer un elemento de la matriz *pWeights* o un elemento de la matriz *pCapabilities* .</span><span class="sxs-lookup"><span data-stu-id="0d67e-132">Unable to read an element of the *pWeights* array or an element of the *pCapabilities* array.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="0d67e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d67e-133">Requirements</span></span>



| <span data-ttu-id="0d67e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d67e-134">Requirement</span></span> | <span data-ttu-id="0d67e-135">Value</span><span class="sxs-lookup"><span data-stu-id="0d67e-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d67e-136">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="0d67e-136">TAPI version</span></span><br/> | <span data-ttu-id="0d67e-137">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0d67e-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0d67e-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d67e-138">Header</span></span><br/>       | <dl> <span data-ttu-id="0d67e-139"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d67e-139"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="0d67e-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d67e-140">Library</span></span><br/>      | <dl> <span data-ttu-id="0d67e-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d67e-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0d67e-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d67e-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="0d67e-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d67e-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




