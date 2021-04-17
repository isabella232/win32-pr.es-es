---
description: El método SetValue agrega un nuevo valor PROPVARIANT o sobrescribe uno existente.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'IPortableDeviceValues:: SetValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690256"
---
# <a name="iportabledevicevaluessetvalue-method"></a><span data-ttu-id="04419-103">IPortableDeviceValues:: SetValue (método)</span><span class="sxs-lookup"><span data-stu-id="04419-103">IPortableDeviceValues::SetValue method</span></span>

<span data-ttu-id="04419-104">El método **SetValue** agrega un nuevo valor **PROPVARIANT** o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="04419-104">The **SetValue** method adds a new **PROPVARIANT** value or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="04419-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04419-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="04419-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04419-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04419-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="04419-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04419-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="04419-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="04419-109">*pValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="04419-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04419-110">**PROPVARIANT** que especifica el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="04419-110">A **PROPVARIANT** that specifies the new value.</span></span> <span data-ttu-id="04419-111">El SDK copia el valor, de modo que el llamador pueda liberar la variable local llamando a **PropVariantClear** después de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="04419-111">The SDK copies the value, so the caller can release the local variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04419-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04419-112">Return value</span></span>

<span data-ttu-id="04419-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="04419-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="04419-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="04419-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="04419-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="04419-115">Return code</span></span>                                                                          | <span data-ttu-id="04419-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="04419-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="04419-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="04419-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="04419-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="04419-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="04419-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04419-119">Remarks</span></span>

<span data-ttu-id="04419-120">Cuando el valor de VARTYPE para *pValue* es VT \_ Vector o VT \_ UI1, no se admite la configuración de un búfer **nulo** o de tamaño cero.</span><span class="sxs-lookup"><span data-stu-id="04419-120">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="04419-121">Por ejemplo, no se permite ningún pValue. Caub. pElems = **null** ni pvalue. Caub. cElems = 0.</span><span class="sxs-lookup"><span data-stu-id="04419-121">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="04419-122">Este método se puede utilizar para recuperar un valor de cualquier tipo de la colección.</span><span class="sxs-lookup"><span data-stu-id="04419-122">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="04419-123">Sin embargo, si conoce el tipo de valor de antemano, use uno de los métodos de **set especializados...** de esta interfaz para evitar la sobrecarga de trabajar directamente con los valores de PROPVARIANT.</span><span class="sxs-lookup"><span data-stu-id="04419-123">However, if you know the value type in advance, use one of the specialized **Set...** methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

<span data-ttu-id="04419-124">Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="04419-124">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="04419-125">La memoria de clave existente se libera adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="04419-125">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="04419-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04419-126">Requirements</span></span>



| <span data-ttu-id="04419-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="04419-127">Requirement</span></span> | <span data-ttu-id="04419-128">Value</span><span class="sxs-lookup"><span data-stu-id="04419-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04419-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04419-129">Header</span></span><br/>  | <dl> <span data-ttu-id="04419-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="04419-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="04419-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04419-131">Library</span></span><br/> | <dl> <span data-ttu-id="04419-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04419-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04419-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="04419-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04419-134">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="04419-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="04419-135">**IPortableDeviceValues:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="04419-135">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="04419-136">**IPortableDeviceValues::RemoveValue**</span><span class="sxs-lookup"><span data-stu-id="04419-136">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




