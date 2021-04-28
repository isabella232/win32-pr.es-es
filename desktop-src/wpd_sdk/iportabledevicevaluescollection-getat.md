---
description: 'Método IPortableDeviceValuesCollection::GetAt: el método GetAt recupera un elemento de la colección mediante un índice de base cero.'
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: Método IPortableDeviceValuesCollection::GetAt (PortableDeviceTypes.h)
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
ms.openlocfilehash: 2ad10a7b9cc3c252a0cee4cb71df05cb108e0a18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083263"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a><span data-ttu-id="f9fe4-103">IPortableDeviceValuesCollection::GetAt (método)</span><span class="sxs-lookup"><span data-stu-id="f9fe4-103">IPortableDeviceValuesCollection::GetAt method</span></span>

<span data-ttu-id="f9fe4-104">El **método GetAt** recupera un elemento de la colección mediante un índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="f9fe4-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fe4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9fe4-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a><span data-ttu-id="f9fe4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9fe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9fe4-107">*dwIndex* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f9fe4-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9fe4-108">**DWORD** que especifica un índice de base cero en la colección.</span><span class="sxs-lookup"><span data-stu-id="f9fe4-108">**DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="f9fe4-109">*ppValues* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f9fe4-109">*ppValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9fe4-110">Dirección de una variable que recibe un puntero a una [**interfaz IPortableDeviceValues**](iportabledevicevalues.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="f9fe4-110">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface from the collection.</span></span> <span data-ttu-id="f9fe4-111">El autor de la llamada es responsable de **llamar a Release** en esta interfaz cuando haya terminado con ella.</span><span class="sxs-lookup"><span data-stu-id="f9fe4-111">The caller is responsible for calling **Release** on this interface when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9fe4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9fe4-112">Return value</span></span>

<span data-ttu-id="f9fe4-113">El método devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="f9fe4-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f9fe4-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="f9fe4-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f9fe4-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f9fe4-115">Return code</span></span>                                                                                  | <span data-ttu-id="f9fe4-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9fe4-116">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9fe4-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fe4-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f9fe4-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="f9fe4-118">The method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="f9fe4-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fe4-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f9fe4-120">El índice de base cero que se pasó estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="f9fe4-120">The zero-based index that was passed in was out of range.</span></span><br/>             |
| <dl> <span data-ttu-id="f9fe4-121"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fe4-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="f9fe4-122">Un argumento de puntero necesario era **NULL.**</span><span class="sxs-lookup"><span data-stu-id="f9fe4-122">A required pointer argument was **NULL**.</span></span><br/>                             |
| <dl> <span data-ttu-id="f9fe4-123"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fe4-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="f9fe4-124">La colección contiene un **puntero NULL** **IPortableDeviceValues.**</span><span class="sxs-lookup"><span data-stu-id="f9fe4-124">The collection contains a **NULL** **IPortableDeviceValues** pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9fe4-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9fe4-125">Remarks</span></span>

<span data-ttu-id="f9fe4-126">Los cambios realizados en los valores de la interfaz recuperada se realizarán en la versión almacenada en la colección.</span><span class="sxs-lookup"><span data-stu-id="f9fe4-126">Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9fe4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9fe4-127">Requirements</span></span>



| <span data-ttu-id="f9fe4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9fe4-128">Requirement</span></span> | <span data-ttu-id="f9fe4-129">Value</span><span class="sxs-lookup"><span data-stu-id="f9fe4-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9fe4-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9fe4-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f9fe4-131"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="f9fe4-131"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9fe4-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9fe4-132">Library</span></span><br/> | <dl> <span data-ttu-id="f9fe4-133"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9fe4-133"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9fe4-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f9fe4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9fe4-135">**IPortableDeviceValuesCollection (Interfaz)**</span><span class="sxs-lookup"><span data-stu-id="f9fe4-135">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




