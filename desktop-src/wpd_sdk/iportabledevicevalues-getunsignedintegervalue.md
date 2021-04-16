---
description: El método GetUnsignedIntegerValue recupera un valor ULONG (tipo VT \_ UI4) especificado por una clave.
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'IPortableDeviceValues:: GetUnsignedIntegerValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c7deb0b6ebfdb8feb90248f9d8e1cdf68411d9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649607"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a><span data-ttu-id="8ab47-103">IPortableDeviceValues:: GetUnsignedIntegerValue (método)</span><span class="sxs-lookup"><span data-stu-id="8ab47-103">IPortableDeviceValues::GetUnsignedIntegerValue method</span></span>

<span data-ttu-id="8ab47-104">El método **GetUnsignedIntegerValue** recupera un valor **ULong** (tipo VT \_ UI4) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="8ab47-104">The **GetUnsignedIntegerValue** method retrieves a **ULONG** value (type VT\_UI4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ab47-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ab47-105">Syntax</span></span>


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="8ab47-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ab47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ab47-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8ab47-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab47-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="8ab47-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="8ab47-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8ab47-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab47-110">Puntero al valor **ULong** recuperado.</span><span class="sxs-lookup"><span data-stu-id="8ab47-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ab47-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ab47-111">Return value</span></span>

<span data-ttu-id="8ab47-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8ab47-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8ab47-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="8ab47-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8ab47-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8ab47-114">Return code</span></span>                                                                                                            | <span data-ttu-id="8ab47-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ab47-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ab47-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8ab47-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="8ab47-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="8ab47-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="8ab47-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="8ab47-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="8ab47-119">La propiedad especificada por *key* no es un tipo **ULong** .</span><span class="sxs-lookup"><span data-stu-id="8ab47-119">The property specified by *key* is not a **ULONG** type.</span></span><br/>  |
| <dl> <span data-ttu-id="8ab47-120"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="8ab47-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="8ab47-121">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="8ab47-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="8ab47-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8ab47-122">Examples</span></span>

<span data-ttu-id="8ab47-123">Para obtener un ejemplo de cómo usar este método, vea [recuperar eventos de servicio admitidos](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="8ab47-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ab47-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ab47-124">Requirements</span></span>



| <span data-ttu-id="8ab47-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ab47-125">Requirement</span></span> | <span data-ttu-id="8ab47-126">Value</span><span class="sxs-lookup"><span data-stu-id="8ab47-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ab47-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ab47-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8ab47-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ab47-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ab47-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ab47-129">Library</span></span><br/> | <dl> <span data-ttu-id="8ab47-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ab47-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ab47-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ab47-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ab47-132">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="8ab47-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="8ab47-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="8ab47-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span></span>](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="8ab47-134">Recuperación de eventos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="8ab47-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="8ab47-135">Recuperando métodos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="8ab47-135">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="8ab47-136">Recuperación de las capacidades de representación admitidas por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="8ab47-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




