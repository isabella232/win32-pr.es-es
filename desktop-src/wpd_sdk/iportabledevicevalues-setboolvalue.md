---
description: El método SetBoolValue agrega un nuevo valor booleano (Type VT \_ bool) o sobrescribe uno existente.
ms.assetid: add30665-78f7-4037-801e-af51a4ab2f60
title: 'IPortableDeviceValues:: SetBoolValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7adf311e863c08873aa8300f9e940d4a5b49417f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718689"
---
# <a name="iportabledevicevaluessetboolvalue-method"></a><span data-ttu-id="e1449-103">IPortableDeviceValues:: SetBoolValue (método)</span><span class="sxs-lookup"><span data-stu-id="e1449-103">IPortableDeviceValues::SetBoolValue method</span></span>

<span data-ttu-id="e1449-104">El método **SetBoolValue** agrega un nuevo valor **BOOLEANO** (Type VT \_ bool) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="e1449-104">The **SetBoolValue** method adds a new **Boolean** value (type VT\_BOOL) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1449-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1449-105">Syntax</span></span>


```C++
HRESULT SetBoolValue(
  [in]       REFPROPERTYKEY key,
  [in] const BOOL           Value
);
```



## <a name="parameters"></a><span data-ttu-id="e1449-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1449-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1449-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e1449-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1449-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="e1449-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="e1449-109">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e1449-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1449-110">**Booleano** que especifica el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="e1449-110">A **BOOL** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1449-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1449-111">Return value</span></span>

<span data-ttu-id="e1449-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e1449-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e1449-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="e1449-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e1449-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e1449-114">Return code</span></span>                                                                          | <span data-ttu-id="e1449-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1449-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e1449-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e1449-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e1449-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="e1449-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e1449-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1449-118">Remarks</span></span>

<span data-ttu-id="e1449-119">Si un valor existente tiene la misma clave especificada por el parámetro *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="e1449-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="e1449-120">La memoria de clave existente se libera adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="e1449-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1449-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1449-121">Requirements</span></span>



| <span data-ttu-id="e1449-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1449-122">Requirement</span></span> | <span data-ttu-id="e1449-123">Value</span><span class="sxs-lookup"><span data-stu-id="e1449-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1449-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1449-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e1449-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1449-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1449-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1449-126">Library</span></span><br/> | <dl> <span data-ttu-id="e1449-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1449-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1449-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1449-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1449-129">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e1449-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e1449-130">**IPortableDeviceValues::GetBoolValue**</span><span class="sxs-lookup"><span data-stu-id="e1449-130">**IPortableDeviceValues::GetBoolValue**</span></span>](iportabledevicevalues-getboolvalue.md)
</dt> </dl>

 

 




