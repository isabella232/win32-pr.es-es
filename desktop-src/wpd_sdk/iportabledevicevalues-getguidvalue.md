---
description: El método GetGuidValue recupera un valor GUID (tipo VT \_ CLSID) especificado por una clave.
ms.assetid: 1cfa75e8-2c3b-4893-954e-dae25a6b8220
title: 'IPortableDeviceValues:: GetGuidValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 362672daad835a2e843edeaf6dc517884c25f1ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650111"
---
# <a name="iportabledevicevaluesgetguidvalue-method"></a><span data-ttu-id="867af-103">IPortableDeviceValues:: GetGuidValue (método)</span><span class="sxs-lookup"><span data-stu-id="867af-103">IPortableDeviceValues::GetGuidValue method</span></span>

<span data-ttu-id="867af-104">El método **GetGuidValue** recupera un valor **GUID** (tipo VT \_ CLSID) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="867af-104">The **GetGuidValue** method retrieves a **GUID** value (type VT\_CLSID) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="867af-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="867af-105">Syntax</span></span>


```C++
HRESULT GetGuidValue(
  [in]  REFPROPERTYKEY key,
  [out] GUID           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="867af-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="867af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="867af-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="867af-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="867af-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="867af-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="867af-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="867af-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="867af-110">Puntero al valor **GUID** recuperado.</span><span class="sxs-lookup"><span data-stu-id="867af-110">Pointer to the retrieved **GUID** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="867af-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="867af-111">Return value</span></span>

<span data-ttu-id="867af-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="867af-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="867af-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="867af-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="867af-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="867af-114">Return code</span></span>                                                                                                            | <span data-ttu-id="867af-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="867af-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="867af-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="867af-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="867af-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="867af-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="867af-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="867af-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="867af-119">La propiedad especificada por *key* no es un tipo **GUID** .</span><span class="sxs-lookup"><span data-stu-id="867af-119">The property specified by *key* is not a **GUID** type.</span></span><br/>   |
| <dl> <span data-ttu-id="867af-120"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="867af-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="867af-121">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="867af-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="867af-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="867af-122">Examples</span></span>

<span data-ttu-id="867af-123">Para obtener un ejemplo de cómo usar este método, vea [recuperar métodos de servicio admitidos](retrieving-supported-methods.md).</span><span class="sxs-lookup"><span data-stu-id="867af-123">For an example of how to use this method, see [Retrieving Supported Service Methods](retrieving-supported-methods.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="867af-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="867af-124">Requirements</span></span>



| <span data-ttu-id="867af-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="867af-125">Requirement</span></span> | <span data-ttu-id="867af-126">Value</span><span class="sxs-lookup"><span data-stu-id="867af-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="867af-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="867af-127">Header</span></span><br/>  | <dl> <span data-ttu-id="867af-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="867af-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="867af-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="867af-129">Library</span></span><br/> | <dl> <span data-ttu-id="867af-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="867af-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="867af-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="867af-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="867af-132">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="867af-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="867af-133">**IPortableDeviceValues::SetGuidValue**</span><span class="sxs-lookup"><span data-stu-id="867af-133">**IPortableDeviceValues::SetGuidValue**</span></span>](iportabledevicevalues-setguidvalue.md)
</dt> <dt>

[<span data-ttu-id="867af-134">Recuperando métodos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="867af-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="867af-135">Recuperación de las capacidades de representación admitidas por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="867af-135">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




