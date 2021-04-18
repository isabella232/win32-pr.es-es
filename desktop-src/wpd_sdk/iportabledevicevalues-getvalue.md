---
description: El método GetValue recupera un valor de PROPVARIANT especificado por una clave.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'IPortableDeviceValues:: GetValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6ab5ec24e67d5259eec86c6a33d32766a5426b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718691"
---
# <a name="iportabledevicevaluesgetvalue-method"></a><span data-ttu-id="d90b9-103">IPortableDeviceValues:: GetValue (método)</span><span class="sxs-lookup"><span data-stu-id="d90b9-103">IPortableDeviceValues::GetValue method</span></span>

<span data-ttu-id="d90b9-104">El método **GetValue** recupera un valor de **PROPVARIANT** especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="d90b9-104">The **GetValue** method retrieves a **PROPVARIANT** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="d90b9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d90b9-105">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="d90b9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d90b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d90b9-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d90b9-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d90b9-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d90b9-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d90b9-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d90b9-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d90b9-110">Puntero al valor de **PROPVARIANT** recuperado.</span><span class="sxs-lookup"><span data-stu-id="d90b9-110">Pointer to the retrieved **PROPVARIANT** value.</span></span> <span data-ttu-id="d90b9-111">El autor de la llamada debe liberar la memoria mediante una llamada a **PropVariantClear** cuando se realiza con ella.</span><span class="sxs-lookup"><span data-stu-id="d90b9-111">The caller must release the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d90b9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d90b9-112">Return value</span></span>

<span data-ttu-id="d90b9-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d90b9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d90b9-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="d90b9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d90b9-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d90b9-115">Return code</span></span>                                                                                                            | <span data-ttu-id="d90b9-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d90b9-116">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="d90b9-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d90b9-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="d90b9-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="d90b9-118">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d90b9-119"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="d90b9-119"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="d90b9-120">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="d90b9-120">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d90b9-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d90b9-121">Remarks</span></span>

<span data-ttu-id="d90b9-122">Cuando el valor de VARTYPE para *pValue* es VT \_ Vector o VT \_ UI1, no se admite la recuperación de un búfer **nulo** o de tamaño cero.</span><span class="sxs-lookup"><span data-stu-id="d90b9-122">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="d90b9-123">Por ejemplo, no se permite ningún pValue. Caub. pElems = **null** ni pvalue. Caub. cElems = 0.</span><span class="sxs-lookup"><span data-stu-id="d90b9-123">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="d90b9-124">Este método se puede utilizar para recuperar un valor de cualquier tipo de la colección.</span><span class="sxs-lookup"><span data-stu-id="d90b9-124">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="d90b9-125">Sin embargo, si conoce el tipo de valor de antemano, use uno de los métodos de recuperación especializados de esta interfaz para evitar la sobrecarga de trabajar directamente con los valores de PROPVARIANT.</span><span class="sxs-lookup"><span data-stu-id="d90b9-125">However, if you know the value type in advance, use one of the specialized retrieval methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="d90b9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d90b9-126">Requirements</span></span>



| <span data-ttu-id="d90b9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d90b9-127">Requirement</span></span> | <span data-ttu-id="d90b9-128">Value</span><span class="sxs-lookup"><span data-stu-id="d90b9-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d90b9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d90b9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d90b9-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d90b9-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d90b9-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d90b9-131">Library</span></span><br/> | <dl> <span data-ttu-id="d90b9-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d90b9-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d90b9-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d90b9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d90b9-134">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d90b9-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d90b9-135">**IPortableDeviceValues::RemoveValue**</span><span class="sxs-lookup"><span data-stu-id="d90b9-135">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> <dt>

[<span data-ttu-id="d90b9-136">**IPortableDeviceValues:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="d90b9-136">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




