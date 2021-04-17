---
description: El método GetAd recupera un elemento de la colección mediante un índice basado en cero.
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'IPortableDeviceValuesCollection:: GetAt (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ffbc65f39aab63189aa451005008f585c46bd8d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708211"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a><span data-ttu-id="3e38a-103">IPortableDeviceValuesCollection:: GetAt (método)</span><span class="sxs-lookup"><span data-stu-id="3e38a-103">IPortableDeviceValuesCollection::GetAt method</span></span>

<span data-ttu-id="3e38a-104">El método **GetAd** recupera un elemento de la colección mediante un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="3e38a-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e38a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e38a-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a><span data-ttu-id="3e38a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e38a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e38a-107">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e38a-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e38a-108">**DWORD** que especifica un índice basado en cero en la colección.</span><span class="sxs-lookup"><span data-stu-id="3e38a-108">**DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="3e38a-109">*ppValues* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3e38a-109">*ppValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e38a-110">Dirección de una variable que recibe un puntero a una interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="3e38a-110">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface from the collection.</span></span> <span data-ttu-id="3e38a-111">El autor de la llamada es responsable de llamar a **Release** en esta interfaz cuando se realiza con ella.</span><span class="sxs-lookup"><span data-stu-id="3e38a-111">The caller is responsible for calling **Release** on this interface when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e38a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e38a-112">Return value</span></span>

<span data-ttu-id="3e38a-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3e38a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3e38a-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="3e38a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3e38a-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3e38a-115">Return code</span></span>                                                                                  | <span data-ttu-id="3e38a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e38a-116">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e38a-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3e38a-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3e38a-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="3e38a-118">The method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="3e38a-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3e38a-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3e38a-120">El índice de base cero que se pasó estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="3e38a-120">The zero-based index that was passed in was out of range.</span></span><br/>             |
| <dl> <span data-ttu-id="3e38a-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3e38a-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="3e38a-122">Un argumento de puntero necesario era **null**.</span><span class="sxs-lookup"><span data-stu-id="3e38a-122">A required pointer argument was **NULL**.</span></span><br/>                             |
| <dl> <span data-ttu-id="3e38a-123"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="3e38a-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="3e38a-124">La colección contiene un puntero **IPortableDeviceValues** **nulo** .</span><span class="sxs-lookup"><span data-stu-id="3e38a-124">The collection contains a **NULL** **IPortableDeviceValues** pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e38a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e38a-125">Remarks</span></span>

<span data-ttu-id="3e38a-126">Los cambios que se realicen en los valores de la interfaz recuperada se realizarán en la versión almacenada en la colección.</span><span class="sxs-lookup"><span data-stu-id="3e38a-126">Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e38a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e38a-127">Requirements</span></span>



| <span data-ttu-id="3e38a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e38a-128">Requirement</span></span> | <span data-ttu-id="3e38a-129">Value</span><span class="sxs-lookup"><span data-stu-id="3e38a-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e38a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e38a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3e38a-131"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e38a-131"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e38a-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e38a-132">Library</span></span><br/> | <dl> <span data-ttu-id="3e38a-133"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e38a-133"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e38a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e38a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e38a-135">**Interfaz IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="3e38a-135">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




