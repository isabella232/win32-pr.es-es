---
description: 'Método IPortableDeviceValuesCollection::RemoveAt: el método RemoveAt quita el elemento almacenado en la ubicación especificada por el índice especificado.'
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: Método IPortableDeviceValuesCollection::RemoveAt (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7db15480906bee8181bb0fc589c4f3e30ce4753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083173"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a><span data-ttu-id="f522a-103">IPortableDeviceValuesCollection::RemoveAt (Método)</span><span class="sxs-lookup"><span data-stu-id="f522a-103">IPortableDeviceValuesCollection::RemoveAt method</span></span>

<span data-ttu-id="f522a-104">El **método RemoveAt** quita el elemento almacenado en la ubicación especificada por el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="f522a-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f522a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f522a-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="f522a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f522a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f522a-107">*dwIndex* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f522a-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f522a-108">Especifica el índice del elemento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="f522a-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f522a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f522a-109">Return value</span></span>

<span data-ttu-id="f522a-110">El método devuelve un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f522a-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f522a-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="f522a-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f522a-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f522a-112">Return code</span></span>                                                                                  | <span data-ttu-id="f522a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f522a-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="f522a-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f522a-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f522a-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="f522a-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="f522a-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f522a-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f522a-117">El índice especificado estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="f522a-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f522a-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f522a-118">Remarks</span></span>

<span data-ttu-id="f522a-119">Debe especificar un índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="f522a-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="f522a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f522a-120">Requirements</span></span>



| <span data-ttu-id="f522a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f522a-121">Requirement</span></span> | <span data-ttu-id="f522a-122">Value</span><span class="sxs-lookup"><span data-stu-id="f522a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f522a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f522a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f522a-124"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="f522a-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f522a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f522a-125">Library</span></span><br/> | <dl> <span data-ttu-id="f522a-126"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f522a-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f522a-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f522a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f522a-128">**IPortableDeviceValuesCollection (Interfaz)**</span><span class="sxs-lookup"><span data-stu-id="f522a-128">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




