---
description: 'Método IPortableDeviceValues::Clear: el método Clear elimina todos los elementos de la colección.'
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: Método IPortableDeviceValues::Clear (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8e1df59cd972bc470607ac2b49d05f43dba8b3a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109903"
---
# <a name="iportabledevicevaluesclear-method"></a><span data-ttu-id="8a4e3-103">IPortableDeviceValues::Clear (Método)</span><span class="sxs-lookup"><span data-stu-id="8a4e3-103">IPortableDeviceValues::Clear method</span></span>

<span data-ttu-id="8a4e3-104">El **método Clear** elimina todos los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-104">The **Clear** method deletes all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a4e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a4e3-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="8a4e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a4e3-106">Parameters</span></span>

<span data-ttu-id="8a4e3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a4e3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a4e3-108">Return value</span></span>

<span data-ttu-id="8a4e3-109">El método devuelve un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8a4e3-110">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8a4e3-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8a4e3-111">Return code</span></span>                                                                          | <span data-ttu-id="8a4e3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a4e3-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8a4e3-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a4e3-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8a4e3-114">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8a4e3-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8a4e3-115">Remarks</span></span>

<span data-ttu-id="8a4e3-116">Este método libera la memoria de todos los elementos asignados dinámicamente en la colección.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-116">This method frees the memory for all dynamically allocated items in the collection.</span></span> <span data-ttu-id="8a4e3-117">Para las interfaces, llama a **Release**.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-117">For interfaces, it calls **Release**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a4e3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a4e3-118">Requirements</span></span>



| <span data-ttu-id="8a4e3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a4e3-119">Requirement</span></span> | <span data-ttu-id="8a4e3-120">Value</span><span class="sxs-lookup"><span data-stu-id="8a4e3-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a4e3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a4e3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8a4e3-122"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="8a4e3-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a4e3-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a4e3-123">Library</span></span><br/> | <dl> <span data-ttu-id="8a4e3-124"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a4e3-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a4e3-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8a4e3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a4e3-126">**IPortableDeviceValues (Interfaz)**</span><span class="sxs-lookup"><span data-stu-id="8a4e3-126">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




