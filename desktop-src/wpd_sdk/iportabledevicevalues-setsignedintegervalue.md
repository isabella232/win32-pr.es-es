---
description: El método SetSignedIntegerValue agrega un nuevo valor LONG (Type VT \_ I4) o sobrescribe uno existente.
ms.assetid: b0bb2992-2906-446c-be9a-20bff13f8e1d
title: 'IPortableDeviceValues:: SetSignedIntegerValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 26a5d01ec69203c39008de394e3693acc833d262
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708686"
---
# <a name="iportabledevicevaluessetsignedintegervalue-method"></a><span data-ttu-id="ff133-103">IPortableDeviceValues:: SetSignedIntegerValue (método)</span><span class="sxs-lookup"><span data-stu-id="ff133-103">IPortableDeviceValues::SetSignedIntegerValue method</span></span>

<span data-ttu-id="ff133-104">El método **SetSignedIntegerValue** agrega un nuevo valor **Long** (Type VT \_ I4) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="ff133-104">The **SetSignedIntegerValue** method adds a new **LONG** value (type VT\_I4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff133-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff133-105">Syntax</span></span>


```C++
HRESULT SetSignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONG           Value
);
```



## <a name="parameters"></a><span data-ttu-id="ff133-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff133-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff133-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ff133-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff133-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="ff133-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="ff133-109">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ff133-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff133-110">Un valor de **tipo Long** que especifica el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="ff133-110">A **LONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff133-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff133-111">Return value</span></span>

<span data-ttu-id="ff133-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ff133-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ff133-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="ff133-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ff133-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ff133-114">Return code</span></span>                                                                          | <span data-ttu-id="ff133-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff133-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ff133-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ff133-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ff133-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="ff133-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ff133-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff133-118">Remarks</span></span>

<span data-ttu-id="ff133-119">Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="ff133-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff133-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff133-120">Requirements</span></span>



| <span data-ttu-id="ff133-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff133-121">Requirement</span></span> | <span data-ttu-id="ff133-122">Value</span><span class="sxs-lookup"><span data-stu-id="ff133-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff133-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff133-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ff133-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff133-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff133-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff133-125">Library</span></span><br/> | <dl> <span data-ttu-id="ff133-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff133-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff133-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff133-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff133-128">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="ff133-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ff133-129">**IPortableDeviceValues::GetSignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="ff133-129">**IPortableDeviceValues::GetSignedIntegerValue**</span></span>](iportabledevicevalues-getsignedintegervalue.md)
</dt> </dl>

 

 




