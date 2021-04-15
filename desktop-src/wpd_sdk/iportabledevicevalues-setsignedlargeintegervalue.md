---
description: El método SetSignedLargeIntegerValue agrega un nuevo valor de LONGLONG (Type VT \_ i8) o sobrescribe uno existente.
ms.assetid: 604b48ed-3e3f-4a06-91dd-7ece9f146824
title: 'IPortableDeviceValues:: SetSignedLargeIntegerValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f8c207a88e17c9a1ddf45d77e9da8b62a8396e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708685"
---
# <a name="iportabledevicevaluessetsignedlargeintegervalue-method"></a><span data-ttu-id="6ba55-103">IPortableDeviceValues:: SetSignedLargeIntegerValue (método)</span><span class="sxs-lookup"><span data-stu-id="6ba55-103">IPortableDeviceValues::SetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="6ba55-104">El método **SetSignedLargeIntegerValue** agrega un nuevo valor de **LONGLONG** (Type VT \_ i8) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="6ba55-104">The **SetSignedLargeIntegerValue** method adds a new **LONGLONG** value (type VT\_I8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ba55-105">Syntax</span></span>


```C++
HRESULT SetSignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONGLONG       Value
);
```



## <a name="parameters"></a><span data-ttu-id="6ba55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ba55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba55-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6ba55-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba55-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="6ba55-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="6ba55-109">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6ba55-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba55-110">**LONGLONG** que especifica el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="6ba55-110">A **LONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba55-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ba55-111">Return value</span></span>

<span data-ttu-id="6ba55-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6ba55-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6ba55-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="6ba55-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6ba55-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6ba55-114">Return code</span></span>                                                                          | <span data-ttu-id="6ba55-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ba55-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6ba55-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6ba55-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6ba55-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="6ba55-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6ba55-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ba55-118">Remarks</span></span>

<span data-ttu-id="6ba55-119">Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="6ba55-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba55-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ba55-120">Requirements</span></span>



| <span data-ttu-id="6ba55-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba55-121">Requirement</span></span> | <span data-ttu-id="6ba55-122">Value</span><span class="sxs-lookup"><span data-stu-id="6ba55-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba55-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ba55-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6ba55-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ba55-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ba55-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ba55-125">Library</span></span><br/> | <dl> <span data-ttu-id="6ba55-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ba55-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ba55-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ba55-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba55-128">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="6ba55-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="6ba55-129">**IPortableDeviceValues::GetSignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="6ba55-129">**IPortableDeviceValues::GetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-getsignedlargeintegervalue.md)
</dt> </dl>

 

 




