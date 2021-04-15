---
description: El método SetStringValue agrega un nuevo valor de cadena (Type VT \_ LPWStr) o sobrescribe uno existente.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'IPortableDeviceValues:: SetStringValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708684"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a><span data-ttu-id="079a0-103">IPortableDeviceValues:: SetStringValue (método)</span><span class="sxs-lookup"><span data-stu-id="079a0-103">IPortableDeviceValues::SetStringValue method</span></span>

<span data-ttu-id="079a0-104">El método **SetStringValue** agrega un nuevo valor de cadena (Type VT \_ LPWStr) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="079a0-104">The **SetStringValue** method adds a new string value (type VT\_LPWSTR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="079a0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="079a0-105">Syntax</span></span>


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a><span data-ttu-id="079a0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="079a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="079a0-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="079a0-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="079a0-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="079a0-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="079a0-109">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="079a0-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="079a0-110">**LPCWSTR** que especifica el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="079a0-110">A **LPCWSTR** that specifies the new value.</span></span> <span data-ttu-id="079a0-111">Se copia la cadena, por lo que el llamador puede liberar la memoria asignada para este valor después de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="079a0-111">The string is copied, so the caller can release the memory allocated for this value after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="079a0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="079a0-112">Return value</span></span>

<span data-ttu-id="079a0-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="079a0-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="079a0-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="079a0-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="079a0-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="079a0-115">Return code</span></span>                                                                          | <span data-ttu-id="079a0-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="079a0-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="079a0-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="079a0-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="079a0-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="079a0-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="079a0-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="079a0-119">Remarks</span></span>

<span data-ttu-id="079a0-120">Cualquier memoria de clave existente se liberará adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="079a0-120">Any existing key memory will be released appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="079a0-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="079a0-121">Examples</span></span>

<span data-ttu-id="079a0-122">Para obtener un ejemplo de cómo usar este método, vea [especificar la información del cliente](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="079a0-122">For an example of how to use this method, see [Specifying Client Information](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="079a0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="079a0-123">Requirements</span></span>



| <span data-ttu-id="079a0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="079a0-124">Requirement</span></span> | <span data-ttu-id="079a0-125">Value</span><span class="sxs-lookup"><span data-stu-id="079a0-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="079a0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="079a0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="079a0-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="079a0-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="079a0-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="079a0-128">Library</span></span><br/> | <dl> <span data-ttu-id="079a0-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="079a0-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="079a0-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="079a0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="079a0-131">Agregar un recurso a un objeto</span><span class="sxs-lookup"><span data-stu-id="079a0-131">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="079a0-132">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="079a0-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="079a0-133">**IPortableDeviceValues:: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="079a0-133">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[<span data-ttu-id="079a0-134">Establecer propiedades para un solo objeto</span><span class="sxs-lookup"><span data-stu-id="079a0-134">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="079a0-135">Establecer las propiedades de varios objetos</span><span class="sxs-lookup"><span data-stu-id="079a0-135">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> <dt>

[<span data-ttu-id="079a0-136">Especificar información de cliente</span><span class="sxs-lookup"><span data-stu-id="079a0-136">Specifying Client Information</span></span>](specifying-client-information.md)
</dt> <dt>

[<span data-ttu-id="079a0-137">Escritura de propiedades de objetos de contenido</span><span class="sxs-lookup"><span data-stu-id="079a0-137">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




