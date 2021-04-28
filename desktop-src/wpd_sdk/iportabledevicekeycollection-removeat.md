---
description: 'Método IPortableDeviceKeyCollection::RemoveAt: el método RemoveAt quita el elemento almacenado en la ubicación especificada por el índice especificado.'
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: Método IPortableDeviceKeyCollection::RemoveAt (PortableDeviceTypes.h)
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
ms.openlocfilehash: 3ec2b1137e7959a646c2943ab1aa7a5c3428d3c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109952"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a><span data-ttu-id="d81a6-103">IPortableDeviceKeyCollection::RemoveAt (Método)</span><span class="sxs-lookup"><span data-stu-id="d81a6-103">IPortableDeviceKeyCollection::RemoveAt method</span></span>

<span data-ttu-id="d81a6-104">El **método RemoveAt** quita el elemento almacenado en la ubicación especificada por el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="d81a6-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d81a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d81a6-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="d81a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d81a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d81a6-107">*dwIndex* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d81a6-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d81a6-108">Especifica el índice del elemento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="d81a6-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d81a6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d81a6-109">Return value</span></span>

<span data-ttu-id="d81a6-110">El método devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d81a6-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d81a6-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="d81a6-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d81a6-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d81a6-112">Return code</span></span>                                                                                  | <span data-ttu-id="d81a6-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d81a6-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d81a6-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d81a6-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d81a6-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="d81a6-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="d81a6-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d81a6-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d81a6-117">El índice especificado estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="d81a6-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d81a6-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d81a6-118">Remarks</span></span>

<span data-ttu-id="d81a6-119">Debe especificar un índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="d81a6-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="d81a6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d81a6-120">Requirements</span></span>



| <span data-ttu-id="d81a6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d81a6-121">Requirement</span></span> | <span data-ttu-id="d81a6-122">Value</span><span class="sxs-lookup"><span data-stu-id="d81a6-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81a6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d81a6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d81a6-124"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="d81a6-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d81a6-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d81a6-125">Library</span></span><br/> | <dl> <span data-ttu-id="d81a6-126"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d81a6-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d81a6-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d81a6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d81a6-128">**IPortableDeviceKeyCollection (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="d81a6-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> </dl>

 

 




