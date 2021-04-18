---
description: El método GetBoolValue recupera un valor booleano (Type VT \_ bool) especificado por una clave.
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: 'IPortableDeviceValues:: GetBoolValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8554fc30a1b66226f6e4f8de4e5d8ac0e8abfabf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653535"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a><span data-ttu-id="86f94-103">IPortableDeviceValues:: GetBoolValue (método)</span><span class="sxs-lookup"><span data-stu-id="86f94-103">IPortableDeviceValues::GetBoolValue method</span></span>

<span data-ttu-id="86f94-104">El método **GetBoolValue** recupera un valor **BOOLEANO** (Type VT \_ bool) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="86f94-104">The **GetBoolValue** method retrieves a **Boolean** value (type VT\_BOOL) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="86f94-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86f94-105">Syntax</span></span>


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="86f94-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86f94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86f94-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="86f94-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86f94-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="86f94-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="86f94-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86f94-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86f94-110">Puntero al valor **bool** recuperado.</span><span class="sxs-lookup"><span data-stu-id="86f94-110">Pointer to the retrieved **BOOL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86f94-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86f94-111">Return value</span></span>

<span data-ttu-id="86f94-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="86f94-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="86f94-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="86f94-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="86f94-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="86f94-114">Return code</span></span>                                                                                                            | <span data-ttu-id="86f94-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="86f94-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="86f94-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="86f94-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="86f94-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="86f94-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="86f94-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="86f94-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="86f94-119">La propiedad especificada por *key* no es un tipo **bool** .</span><span class="sxs-lookup"><span data-stu-id="86f94-119">The property specified by *key* is not a **BOOL** type.</span></span><br/>   |
| <dl> <span data-ttu-id="86f94-120"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="86f94-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="86f94-121">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="86f94-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="86f94-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="86f94-122">Examples</span></span>

<span data-ttu-id="86f94-123">Para obtener un ejemplo de cómo usar este método, vea [establecer las propiedades de un único objeto](setting-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="86f94-123">For an example of how to use this method, see [Setting Properties for a Single Object](setting-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86f94-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86f94-124">Requirements</span></span>



| <span data-ttu-id="86f94-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="86f94-125">Requirement</span></span> | <span data-ttu-id="86f94-126">Value</span><span class="sxs-lookup"><span data-stu-id="86f94-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86f94-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86f94-127">Header</span></span><br/>  | <dl> <span data-ttu-id="86f94-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="86f94-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="86f94-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86f94-129">Library</span></span><br/> | <dl> <span data-ttu-id="86f94-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86f94-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86f94-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="86f94-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f94-132">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="86f94-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="86f94-133">**IPortableDeviceValues:: SetBoolValue**</span><span class="sxs-lookup"><span data-stu-id="86f94-133">**IPortableDeviceValues::SetBoolValue**</span></span>](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[<span data-ttu-id="86f94-134">Recuperación de eventos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="86f94-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="86f94-135">Establecer propiedades para un solo objeto</span><span class="sxs-lookup"><span data-stu-id="86f94-135">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="86f94-136">Escritura de propiedades de objetos de contenido</span><span class="sxs-lookup"><span data-stu-id="86f94-136">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




