---
description: El método RemoveAt quita el elemento almacenado en la ubicación especificada por el índice especificado.
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: 'IPortableDeviceKeyCollection:: RemoveAt (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f4e126ef5fcad74b7cee5f748322f15e75481e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709152"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a><span data-ttu-id="095d5-103">IPortableDeviceKeyCollection:: RemoveAt (método)</span><span class="sxs-lookup"><span data-stu-id="095d5-103">IPortableDeviceKeyCollection::RemoveAt method</span></span>

<span data-ttu-id="095d5-104">El método **RemoveAt** quita el elemento almacenado en la ubicación especificada por el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="095d5-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="095d5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="095d5-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="095d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="095d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="095d5-107">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="095d5-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="095d5-108">Especifica el índice del elemento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="095d5-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="095d5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="095d5-109">Return value</span></span>

<span data-ttu-id="095d5-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="095d5-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="095d5-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="095d5-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="095d5-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="095d5-112">Return code</span></span>                                                                                  | <span data-ttu-id="095d5-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="095d5-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="095d5-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="095d5-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="095d5-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="095d5-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="095d5-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="095d5-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="095d5-117">El índice especificado estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="095d5-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="095d5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="095d5-118">Remarks</span></span>

<span data-ttu-id="095d5-119">Debe especificar un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="095d5-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="095d5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="095d5-120">Requirements</span></span>



| <span data-ttu-id="095d5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="095d5-121">Requirement</span></span> | <span data-ttu-id="095d5-122">Value</span><span class="sxs-lookup"><span data-stu-id="095d5-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="095d5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="095d5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="095d5-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="095d5-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="095d5-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="095d5-125">Library</span></span><br/> | <dl> <span data-ttu-id="095d5-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="095d5-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="095d5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="095d5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="095d5-128">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="095d5-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> </dl>

 

 




