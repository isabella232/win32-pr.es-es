---
description: El método GetKeyValue recupera un valor PROPERTYKEY especificado por una clave.
ms.assetid: 2c92b1c0-3ea6-4a14-8b63-d57752b649b8
title: 'IPortableDeviceValues:: GetKeyValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3d5080a35faa5555d2813c6e419a1965def05bdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649732"
---
# <a name="iportabledevicevaluesgetkeyvalue-method"></a><span data-ttu-id="e7aeb-103">IPortableDeviceValues:: GetKeyValue (método)</span><span class="sxs-lookup"><span data-stu-id="e7aeb-103">IPortableDeviceValues::GetKeyValue method</span></span>

<span data-ttu-id="e7aeb-104">El método **GetKeyValue** recupera un valor **PROPERTYKEY** especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="e7aeb-104">The **GetKeyValue** method retrieves a **PROPERTYKEY** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7aeb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7aeb-105">Syntax</span></span>


```C++
HRESULT GetKeyValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPERTYKEY    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e7aeb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7aeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7aeb-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e7aeb-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7aeb-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="e7aeb-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e7aeb-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e7aeb-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7aeb-110">Puntero al valor de **PROPERTYKEY** recuperado.</span><span class="sxs-lookup"><span data-stu-id="e7aeb-110">Pointer to the retrieved **PROPERTYKEY** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7aeb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7aeb-111">Return value</span></span>

<span data-ttu-id="e7aeb-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e7aeb-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e7aeb-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="e7aeb-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e7aeb-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e7aeb-114">Return code</span></span>                                                                                                            | <span data-ttu-id="e7aeb-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7aeb-115">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7aeb-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e7aeb-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="e7aeb-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="e7aeb-117">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="e7aeb-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="e7aeb-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="e7aeb-119">La propiedad especificada por *key* no es un tipo **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="e7aeb-119">The property specified by *key* is not a **PROPERTYKEY** type.</span></span><br/> |
| <dl> <span data-ttu-id="e7aeb-120"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="e7aeb-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="e7aeb-121">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="e7aeb-121">The property specified by *key* is not in the collection.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="e7aeb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7aeb-122">Requirements</span></span>



| <span data-ttu-id="e7aeb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7aeb-123">Requirement</span></span> | <span data-ttu-id="e7aeb-124">Value</span><span class="sxs-lookup"><span data-stu-id="e7aeb-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7aeb-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7aeb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e7aeb-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7aeb-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7aeb-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7aeb-127">Library</span></span><br/> | <dl> <span data-ttu-id="e7aeb-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7aeb-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7aeb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7aeb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7aeb-130">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e7aeb-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e7aeb-131">**IPortableDeviceValues::SetKeyValue**</span><span class="sxs-lookup"><span data-stu-id="e7aeb-131">**IPortableDeviceValues::SetKeyValue**</span></span>](iportabledevicevalues-setkeyvalue.md)
</dt> </dl>

 

 




