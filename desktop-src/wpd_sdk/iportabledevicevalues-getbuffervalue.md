---
description: El método GetBufferValue recupera un valor de matriz de bytes (Type VT \_ Vector \| VT \_ UI1) especificado por una clave.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: 'IPortableDeviceValues:: GetBufferValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e5b98bb412ed648cf6ac74ec457b1e6032c009ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709126"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a><span data-ttu-id="6ae02-103">IPortableDeviceValues:: GetBufferValue (método)</span><span class="sxs-lookup"><span data-stu-id="6ae02-103">IPortableDeviceValues::GetBufferValue method</span></span>

<span data-ttu-id="6ae02-104">El método **GetBufferValue** recupera un valor de **matriz de bytes** (Type VT \_ Vector \| VT \_ UI1) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="6ae02-104">The **GetBufferValue** method retrieves a **byte array** value (type VT\_VECTOR \| VT\_UI1) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae02-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ae02-105">Syntax</span></span>


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
);
```



## <a name="parameters"></a><span data-ttu-id="6ae02-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ae02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae02-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6ae02-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae02-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="6ae02-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6ae02-109">*ppValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6ae02-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae02-110">Puntero al valor de **byte _ recuperado \* *. El autor de la llamada es responsable de liberar la memoria mediante una llamada a _* CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="6ae02-110">Pointer to the retrieved \**BYTE\**_ value. The caller is responsible for freeing the memory by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="6ae02-111">*pcbValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6ae02-111">*pcbValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae02-112">Puntero al tamaño de *ppValue*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="6ae02-112">Pointer to the size of *ppValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae02-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ae02-113">Return value</span></span>

<span data-ttu-id="6ae02-114">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6ae02-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6ae02-115">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="6ae02-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6ae02-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6ae02-116">Return code</span></span>                                                                                                            | <span data-ttu-id="6ae02-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ae02-117">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ae02-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6ae02-118"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="6ae02-119">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="6ae02-119">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="6ae02-120"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="6ae02-120"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="6ae02-121">La propiedad especificada por *key* no es un tipo **byte** \* .</span><span class="sxs-lookup"><span data-stu-id="6ae02-121">The property specified by *key* is not a **BYTE**\* type.</span></span><br/> |
| <dl> <span data-ttu-id="6ae02-122"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="6ae02-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="6ae02-123">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="6ae02-123">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6ae02-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ae02-124">Remarks</span></span>

<span data-ttu-id="6ae02-125">No se admite la recuperación de un búfer **nulo** ni de un búfer de tamaño cero.</span><span class="sxs-lookup"><span data-stu-id="6ae02-125">Retrieving a **NULL** buffer or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae02-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ae02-126">Requirements</span></span>



| <span data-ttu-id="6ae02-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ae02-127">Requirement</span></span> | <span data-ttu-id="6ae02-128">Value</span><span class="sxs-lookup"><span data-stu-id="6ae02-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae02-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ae02-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6ae02-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ae02-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ae02-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ae02-131">Library</span></span><br/> | <dl> <span data-ttu-id="6ae02-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ae02-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ae02-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ae02-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae02-134">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="6ae02-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="6ae02-135">**IPortableDeviceValues::SetBufferValue**</span><span class="sxs-lookup"><span data-stu-id="6ae02-135">**IPortableDeviceValues::SetBufferValue**</span></span>](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




