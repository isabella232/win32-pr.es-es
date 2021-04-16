---
description: El método SetKeyValue agrega un nuevo valor de REFPROPERTYKEY (tipo VT \_ desconocido) o sobrescribe uno existente.
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
title: 'IPortableDeviceValues:: SetKeyValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae55b47687043bba92afbab09f25de8a5fc679d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708688"
---
# <a name="iportabledevicevaluessetkeyvalue-method"></a><span data-ttu-id="b28c5-103">IPortableDeviceValues:: SetKeyValue (método)</span><span class="sxs-lookup"><span data-stu-id="b28c5-103">IPortableDeviceValues::SetKeyValue method</span></span>

<span data-ttu-id="b28c5-104">El método **SetKeyValue** agrega un nuevo valor de **REFPROPERTYKEY** (tipo VT \_ desconocido) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="b28c5-104">The **SetKeyValue** method adds a new **REFPROPERTYKEY** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="b28c5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b28c5-105">Syntax</span></span>


```C++
HRESULT SetKeyValue(
  [in] REFPROPERTYKEY key,
  [in] REFPROPERTYKEY Value
);
```



## <a name="parameters"></a><span data-ttu-id="b28c5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b28c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b28c5-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b28c5-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b28c5-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="b28c5-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="b28c5-109">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b28c5-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b28c5-110">**REFPROPERTYKEY** que especifica el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="b28c5-110">A **REFPROPERTYKEY** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b28c5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b28c5-111">Return value</span></span>

<span data-ttu-id="b28c5-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b28c5-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b28c5-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="b28c5-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b28c5-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b28c5-114">Return code</span></span>                                                                          | <span data-ttu-id="b28c5-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b28c5-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b28c5-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b28c5-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b28c5-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="b28c5-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b28c5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b28c5-118">Remarks</span></span>

<span data-ttu-id="b28c5-119">Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="b28c5-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="b28c5-120">La memoria de clave existente se libera adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="b28c5-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="b28c5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b28c5-121">Requirements</span></span>



| <span data-ttu-id="b28c5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b28c5-122">Requirement</span></span> | <span data-ttu-id="b28c5-123">Value</span><span class="sxs-lookup"><span data-stu-id="b28c5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b28c5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b28c5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b28c5-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b28c5-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b28c5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b28c5-126">Library</span></span><br/> | <dl> <span data-ttu-id="b28c5-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b28c5-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b28c5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b28c5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b28c5-129">Agregar un recurso a un objeto</span><span class="sxs-lookup"><span data-stu-id="b28c5-129">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="b28c5-130">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b28c5-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b28c5-131">**IPortableDeviceValues::GetKeyValue**</span><span class="sxs-lookup"><span data-stu-id="b28c5-131">**IPortableDeviceValues::GetKeyValue**</span></span>](iportabledevicevalues-getkeyvalue.md)
</dt> </dl>

 

 




