---
description: El método Clear elimina todos los elementos de la colección.
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: 'IPortableDeviceValues:: CLEAR (método) (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 45c04319b5691e3bbcfb56d5a447cf2eb60bfaac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660417"
---
# <a name="iportabledevicevaluesclear-method"></a><span data-ttu-id="cd05d-103">IPortableDeviceValues:: CLEAR (método)</span><span class="sxs-lookup"><span data-stu-id="cd05d-103">IPortableDeviceValues::Clear method</span></span>

<span data-ttu-id="cd05d-104">El método **Clear** elimina todos los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="cd05d-104">The **Clear** method deletes all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd05d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd05d-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="cd05d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd05d-106">Parameters</span></span>

<span data-ttu-id="cd05d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cd05d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd05d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd05d-108">Return value</span></span>

<span data-ttu-id="cd05d-109">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cd05d-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cd05d-110">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="cd05d-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cd05d-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cd05d-111">Return code</span></span>                                                                          | <span data-ttu-id="cd05d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd05d-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cd05d-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="cd05d-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cd05d-114">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="cd05d-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cd05d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd05d-115">Remarks</span></span>

<span data-ttu-id="cd05d-116">Este método libera la memoria de todos los elementos asignados dinámicamente en la colección.</span><span class="sxs-lookup"><span data-stu-id="cd05d-116">This method frees the memory for all dynamically allocated items in the collection.</span></span> <span data-ttu-id="cd05d-117">En el caso de las interfaces, llama a **Release**.</span><span class="sxs-lookup"><span data-stu-id="cd05d-117">For interfaces, it calls **Release**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd05d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd05d-118">Requirements</span></span>



| <span data-ttu-id="cd05d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd05d-119">Requirement</span></span> | <span data-ttu-id="cd05d-120">Value</span><span class="sxs-lookup"><span data-stu-id="cd05d-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd05d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd05d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cd05d-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd05d-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd05d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd05d-123">Library</span></span><br/> | <dl> <span data-ttu-id="cd05d-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd05d-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd05d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd05d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd05d-126">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="cd05d-126">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




