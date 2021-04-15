---
description: El método SetGuidValue agrega un nuevo valor GUID (Type VT \_ CLSID) o sobrescribe uno existente.
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
title: 'IPortableDeviceValues:: SetGuidValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9d9f85def6ba487163f7c4c7d7441a89e0747ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708892"
---
# <a name="iportabledevicevaluessetguidvalue-method"></a><span data-ttu-id="39f6f-103">IPortableDeviceValues:: SetGuidValue (método)</span><span class="sxs-lookup"><span data-stu-id="39f6f-103">IPortableDeviceValues::SetGuidValue method</span></span>

<span data-ttu-id="39f6f-104">El método **SetGuidValue** agrega un nuevo valor **GUID** (Type VT \_ CLSID) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="39f6f-104">The **SetGuidValue** method adds a new **GUID** value (type VT\_CLSID) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f6f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39f6f-105">Syntax</span></span>


```C++
HRESULT SetGuidValue(
  [in] REFPROPERTYKEY key,
  [in] REFGUID        Value
);
```



## <a name="parameters"></a><span data-ttu-id="39f6f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39f6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39f6f-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="39f6f-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39f6f-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="39f6f-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="39f6f-109">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="39f6f-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39f6f-110">**REFGUID** que contiene el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="39f6f-110">A **REFGUID** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39f6f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39f6f-111">Return value</span></span>

<span data-ttu-id="39f6f-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="39f6f-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="39f6f-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="39f6f-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="39f6f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="39f6f-114">Return code</span></span>                                                                          | <span data-ttu-id="39f6f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="39f6f-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="39f6f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="39f6f-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="39f6f-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="39f6f-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="39f6f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39f6f-118">Remarks</span></span>

<span data-ttu-id="39f6f-119">Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="39f6f-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f6f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39f6f-120">Requirements</span></span>



| <span data-ttu-id="39f6f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="39f6f-121">Requirement</span></span> | <span data-ttu-id="39f6f-122">Value</span><span class="sxs-lookup"><span data-stu-id="39f6f-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39f6f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39f6f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="39f6f-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="39f6f-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="39f6f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39f6f-125">Library</span></span><br/> | <dl> <span data-ttu-id="39f6f-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39f6f-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f6f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="39f6f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f6f-128">Agregar un recurso a un objeto</span><span class="sxs-lookup"><span data-stu-id="39f6f-128">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="39f6f-129">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="39f6f-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="39f6f-130">**IPortableDeviceValues::GetGuidValue**</span><span class="sxs-lookup"><span data-stu-id="39f6f-130">**IPortableDeviceValues::GetGuidValue**</span></span>](iportabledevicevalues-getguidvalue.md)
</dt> </dl>

 

 




