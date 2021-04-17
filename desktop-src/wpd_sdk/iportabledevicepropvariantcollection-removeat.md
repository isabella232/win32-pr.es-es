---
description: El método RemoveAt quita el elemento almacenado en la ubicación especificada por el índice especificado.
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'IPortableDevicePropVariantCollection:: RemoveAt (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 74c7900340caab6adfda1b4607df607a4f6f0811
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699406"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a><span data-ttu-id="183ad-103">IPortableDevicePropVariantCollection:: RemoveAt (método)</span><span class="sxs-lookup"><span data-stu-id="183ad-103">IPortableDevicePropVariantCollection::RemoveAt method</span></span>

<span data-ttu-id="183ad-104">El método **RemoveAt** quita el elemento almacenado en la ubicación especificada por el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="183ad-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="183ad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="183ad-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="183ad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="183ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="183ad-107">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="183ad-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="183ad-108">Especifica el índice del elemento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="183ad-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="183ad-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="183ad-109">Return value</span></span>

<span data-ttu-id="183ad-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="183ad-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="183ad-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="183ad-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="183ad-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="183ad-112">Return code</span></span>                                                                                  | <span data-ttu-id="183ad-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="183ad-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="183ad-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="183ad-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="183ad-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="183ad-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="183ad-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="183ad-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="183ad-117">El índice especificado estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="183ad-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="183ad-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="183ad-118">Remarks</span></span>

<span data-ttu-id="183ad-119">Debe especificar un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="183ad-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="183ad-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="183ad-120">Requirements</span></span>



| <span data-ttu-id="183ad-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="183ad-121">Requirement</span></span> | <span data-ttu-id="183ad-122">Value</span><span class="sxs-lookup"><span data-stu-id="183ad-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="183ad-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="183ad-123">Header</span></span><br/>  | <dl> <span data-ttu-id="183ad-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="183ad-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="183ad-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="183ad-125">Library</span></span><br/> | <dl> <span data-ttu-id="183ad-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="183ad-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="183ad-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="183ad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="183ad-128">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="183ad-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




