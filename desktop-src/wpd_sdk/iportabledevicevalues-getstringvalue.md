---
description: El método GetStringValue recupera un valor de cadena (Type VT \_ LPWStr) especificado por una clave.
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: 'IPortableDeviceValues:: GetStringValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fdb4741c36445af686b7721e1f5f04dd3e45f1e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700100"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a><span data-ttu-id="69798-103">IPortableDeviceValues:: GetStringValue (método)</span><span class="sxs-lookup"><span data-stu-id="69798-103">IPortableDeviceValues::GetStringValue method</span></span>

<span data-ttu-id="69798-104">El método **GetStringValue** recupera un valor de cadena (Type VT \_ LPWStr) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="69798-104">The **GetStringValue** method retrieves a string value (type VT\_LPWSTR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="69798-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69798-105">Syntax</span></span>


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="69798-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69798-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69798-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="69798-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69798-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="69798-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="69798-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="69798-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69798-110">Puntero al valor **LPWStr** recuperado.</span><span class="sxs-lookup"><span data-stu-id="69798-110">Pointer to the retrieved **LPWSTR** value.</span></span> <span data-ttu-id="69798-111">El autor de la llamada es responsable de llamar a **CoTaskMemFree** para liberar la memoria.</span><span class="sxs-lookup"><span data-stu-id="69798-111">The caller is responsible for calling **CoTaskMemFree** to release the memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69798-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69798-112">Return value</span></span>

<span data-ttu-id="69798-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="69798-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="69798-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="69798-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="69798-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="69798-115">Return code</span></span>                                                                                                            | <span data-ttu-id="69798-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="69798-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="69798-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="69798-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="69798-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="69798-118">The method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="69798-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="69798-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="69798-120">La propiedad especificada por *key* no es un tipo **LPWStr** .</span><span class="sxs-lookup"><span data-stu-id="69798-120">The property specified by *key* is not an **LPWSTR** type.</span></span><br/> |
| <dl> <span data-ttu-id="69798-121"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="69798-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="69798-122">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="69798-122">The property specified by *key* is not in the collection.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="69798-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="69798-123">Examples</span></span>

<span data-ttu-id="69798-124">Para obtener un ejemplo de cómo usar este método, vea [recuperar eventos de servicio admitidos](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="69798-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69798-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69798-125">Requirements</span></span>



| <span data-ttu-id="69798-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="69798-126">Requirement</span></span> | <span data-ttu-id="69798-127">Value</span><span class="sxs-lookup"><span data-stu-id="69798-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69798-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69798-128">Header</span></span><br/>  | <dl> <span data-ttu-id="69798-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="69798-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="69798-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69798-130">Library</span></span><br/> | <dl> <span data-ttu-id="69798-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69798-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69798-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="69798-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69798-133">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="69798-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="69798-134">**IPortableDeviceValues:: GetAt**</span><span class="sxs-lookup"><span data-stu-id="69798-134">**IPortableDeviceValues::GetAt**</span></span>](iportabledevicevalues-getat.md)
</dt> <dt>

[<span data-ttu-id="69798-135">**IPortableDeviceValues:: SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="69798-135">**IPortableDeviceValues::SetStringValue**</span></span>](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[<span data-ttu-id="69798-136">Recuperación de eventos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="69798-136">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="69798-137">Recuperando formatos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="69798-137">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="69798-138">Recuperando métodos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="69798-138">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




