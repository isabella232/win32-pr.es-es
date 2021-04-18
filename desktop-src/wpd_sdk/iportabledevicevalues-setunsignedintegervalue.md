---
description: El método SetUnsignedIntegerValue agrega un nuevo valor ULONG (tipo VT \_ UI4) o sobrescribe uno existente.
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: 'IPortableDeviceValues:: SetUnsignedIntegerValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7dc237e5cdba120a08899035dc20f6fb6b2b63f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708683"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a><span data-ttu-id="72333-103">IPortableDeviceValues:: SetUnsignedIntegerValue (método)</span><span class="sxs-lookup"><span data-stu-id="72333-103">IPortableDeviceValues::SetUnsignedIntegerValue method</span></span>

<span data-ttu-id="72333-104">El método **SetUnsignedIntegerValue** agrega un nuevo valor **ULong** (tipo VT \_ UI4) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="72333-104">The **SetUnsignedIntegerValue** method adds a new **ULONG** value (type VT\_UI4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="72333-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72333-105">Syntax</span></span>


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
);
```



## <a name="parameters"></a><span data-ttu-id="72333-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72333-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72333-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="72333-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72333-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="72333-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="72333-109">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="72333-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72333-110">**ULong** que especifica el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="72333-110">A **ULONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72333-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72333-111">Return value</span></span>

<span data-ttu-id="72333-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="72333-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="72333-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="72333-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="72333-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="72333-114">Return code</span></span>                                                                          | <span data-ttu-id="72333-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="72333-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="72333-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="72333-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="72333-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="72333-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="72333-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72333-118">Remarks</span></span>

<span data-ttu-id="72333-119">Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="72333-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="examples"></a><span data-ttu-id="72333-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="72333-120">Examples</span></span>

<span data-ttu-id="72333-121">Para obtener un ejemplo de cómo usar este método, vea [**especificar la información del cliente**](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="72333-121">For an example of how to use this method, see [**Specifying Client Information**](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72333-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72333-122">Requirements</span></span>



| <span data-ttu-id="72333-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="72333-123">Requirement</span></span> | <span data-ttu-id="72333-124">Value</span><span class="sxs-lookup"><span data-stu-id="72333-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72333-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72333-125">Header</span></span><br/>  | <dl> <span data-ttu-id="72333-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="72333-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="72333-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72333-127">Library</span></span><br/> | <dl> <span data-ttu-id="72333-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72333-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72333-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="72333-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72333-130">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="72333-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="72333-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="72333-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span></span>](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="72333-132">**Especificar información de cliente**</span><span class="sxs-lookup"><span data-stu-id="72333-132">**Specifying Client Information**</span></span>](specifying-client-information.md)
</dt> </dl>

 

 




