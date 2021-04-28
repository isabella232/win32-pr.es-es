---
description: 'Método IPortableDeviceValuesCollection::Add: el método Add agrega un elemento a la colección.'
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: IPortableDeviceValuesCollection::Add (método, PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 765100e1272fc6766e9f305f37f3b699bd96beb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083257"
---
# <a name="iportabledevicevaluescollectionadd-method"></a><span data-ttu-id="05fa8-103">IPortableDeviceValuesCollection::Add (Método)</span><span class="sxs-lookup"><span data-stu-id="05fa8-103">IPortableDeviceValuesCollection::Add method</span></span>

<span data-ttu-id="05fa8-104">El **método Add** agrega un elemento a la colección.</span><span class="sxs-lookup"><span data-stu-id="05fa8-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="05fa8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05fa8-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a><span data-ttu-id="05fa8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05fa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05fa8-107">*pValues* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="05fa8-107">*pValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05fa8-108">Puntero a una **interfaz IPortableDeviceValues** que se agregará a la colección.</span><span class="sxs-lookup"><span data-stu-id="05fa8-108">Pointer to an **IPortableDeviceValues** interface to add to the collection.</span></span> <span data-ttu-id="05fa8-109">La interfaz no se copia realmente, pero se llama a **AddRef** en ella.</span><span class="sxs-lookup"><span data-stu-id="05fa8-109">The interface is not actually copied, but **AddRef** is called on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05fa8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05fa8-110">Return value</span></span>

<span data-ttu-id="05fa8-111">El método devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="05fa8-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="05fa8-112">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="05fa8-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="05fa8-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="05fa8-113">Return code</span></span>                                                                                   | <span data-ttu-id="05fa8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="05fa8-114">Description</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05fa8-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="05fa8-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="05fa8-116">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="05fa8-116">The method succeeded.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="05fa8-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="05fa8-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="05fa8-118">No hay suficiente memoria disponible para agregar el valor a la colección.</span><span class="sxs-lookup"><span data-stu-id="05fa8-118">There is not enough memory available to add the value to the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="05fa8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05fa8-119">Requirements</span></span>



| <span data-ttu-id="05fa8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="05fa8-120">Requirement</span></span> | <span data-ttu-id="05fa8-121">Value</span><span class="sxs-lookup"><span data-stu-id="05fa8-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05fa8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05fa8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="05fa8-123"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="05fa8-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="05fa8-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05fa8-124">Library</span></span><br/> | <dl> <span data-ttu-id="05fa8-125"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="05fa8-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05fa8-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="05fa8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05fa8-127">**IPortableDeviceValuesCollection (Interfaz)**</span><span class="sxs-lookup"><span data-stu-id="05fa8-127">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




