---
description: El método SetIUnknownValue agrega un nuevo valor IUnknown (tipo VT \_ desconocido) o sobrescribe uno existente.
ms.assetid: 292adf45-439c-4aae-9b17-e4d9ed701eda
title: 'IPortableDeviceValues:: SetIUnknownValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2c3a27fe5ea89359884d70162000b5164b7c1aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708690"
---
# <a name="iportabledevicevaluessetiunknownvalue-method"></a><span data-ttu-id="8bfe1-103">IPortableDeviceValues:: SetIUnknownValue (método)</span><span class="sxs-lookup"><span data-stu-id="8bfe1-103">IPortableDeviceValues::SetIUnknownValue method</span></span>

<span data-ttu-id="8bfe1-104">El método **SetIUnknownValue** agrega un nuevo valor **IUNKNOWN** (tipo VT \_ desconocido) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="8bfe1-104">The **SetIUnknownValue** method adds a new **IUnknown** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bfe1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bfe1-105">Syntax</span></span>


```C++
HRESULT SetIUnknownValue(
  [in] REFPROPERTYKEY key,
  [in] IUnknown       *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="8bfe1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bfe1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bfe1-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8bfe1-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bfe1-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="8bfe1-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="8bfe1-109">*pValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8bfe1-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bfe1-110">Puntero a una interfaz **IUnknown** que especifica el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="8bfe1-110">A pointer to an **IUnknown** interface that specifies the new value.</span></span> <span data-ttu-id="8bfe1-111">El SDK copia una referencia a la interfaz enviada y llama a **AddRef** en ella.</span><span class="sxs-lookup"><span data-stu-id="8bfe1-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bfe1-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bfe1-112">Return value</span></span>

<span data-ttu-id="8bfe1-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8bfe1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8bfe1-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="8bfe1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8bfe1-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8bfe1-115">Return code</span></span>                                                                          | <span data-ttu-id="8bfe1-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bfe1-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8bfe1-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8bfe1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8bfe1-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="8bfe1-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8bfe1-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bfe1-119">Remarks</span></span>

<span data-ttu-id="8bfe1-120">Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="8bfe1-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="8bfe1-121">La memoria de clave existente se libera adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="8bfe1-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bfe1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bfe1-122">Requirements</span></span>



| <span data-ttu-id="8bfe1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bfe1-123">Requirement</span></span> | <span data-ttu-id="8bfe1-124">Value</span><span class="sxs-lookup"><span data-stu-id="8bfe1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bfe1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bfe1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8bfe1-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bfe1-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bfe1-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8bfe1-127">Library</span></span><br/> | <dl> <span data-ttu-id="8bfe1-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bfe1-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bfe1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bfe1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bfe1-130">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="8bfe1-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="8bfe1-131">**IPortableDeviceValues::GetIUnknownValue**</span><span class="sxs-lookup"><span data-stu-id="8bfe1-131">**IPortableDeviceValues::GetIUnknownValue**</span></span>](iportabledevicevalues-getiunknownvalue.md)
</dt> </dl>

 

 




