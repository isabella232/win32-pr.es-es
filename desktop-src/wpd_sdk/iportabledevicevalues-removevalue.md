---
description: El método RemoveValue quita un elemento de la colección.
ms.assetid: 864c23ee-5a4e-4e06-add0-f6aef5562430
title: 'IPortableDeviceValues:: RemoveValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.RemoveValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f65160cc2798524d88471382c855f65dea2e6033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718690"
---
# <a name="iportabledevicevaluesremovevalue-method"></a><span data-ttu-id="ec3e2-103">IPortableDeviceValues:: RemoveValue (método)</span><span class="sxs-lookup"><span data-stu-id="ec3e2-103">IPortableDeviceValues::RemoveValue method</span></span>

<span data-ttu-id="ec3e2-104">El método **RemoveValue** quita un elemento de la colección.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-104">The **RemoveValue** method removes an item from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec3e2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec3e2-105">Syntax</span></span>


```C++
HRESULT RemoveValue(
  [in] REFPROPERTYKEY key
);
```



## <a name="parameters"></a><span data-ttu-id="ec3e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec3e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec3e2-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ec3e2-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3e2-108">**REFPROPERTYKEY** que especifica el elemento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-108">A **REFPROPERTYKEY** that specifies the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec3e2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec3e2-109">Return value</span></span>

<span data-ttu-id="ec3e2-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ec3e2-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ec3e2-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ec3e2-112">Return code</span></span>                                                                          | <span data-ttu-id="ec3e2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec3e2-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ec3e2-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ec3e2-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ec3e2-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ec3e2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec3e2-116">Requirements</span></span>



| <span data-ttu-id="ec3e2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec3e2-117">Requirement</span></span> | <span data-ttu-id="ec3e2-118">Value</span><span class="sxs-lookup"><span data-stu-id="ec3e2-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3e2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec3e2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ec3e2-120"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec3e2-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec3e2-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec3e2-121">Library</span></span><br/> | <dl> <span data-ttu-id="ec3e2-122"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec3e2-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec3e2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec3e2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec3e2-124">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="ec3e2-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ec3e2-125">**IPortableDeviceValues:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="ec3e2-125">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="ec3e2-126">**IPortableDeviceValues:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="ec3e2-126">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




