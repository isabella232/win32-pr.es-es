---
description: El método GetSignedIntegerValue recupera un valor LONG (Type VT \_ I4) especificado por una clave.
ms.assetid: d2291a64-d0b3-4a30-a37c-2b6cd9880a11
title: 'IPortableDeviceValues:: GetSignedIntegerValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2fe0c2f8714d3fa28f61624924eba169f9f1c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650177"
---
# <a name="iportabledevicevaluesgetsignedintegervalue-method"></a><span data-ttu-id="e284b-103">IPortableDeviceValues:: GetSignedIntegerValue (método)</span><span class="sxs-lookup"><span data-stu-id="e284b-103">IPortableDeviceValues::GetSignedIntegerValue method</span></span>

<span data-ttu-id="e284b-104">El método **GetSignedIntegerValue** recupera un valor **Long** (Type VT \_ I4) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="e284b-104">The **GetSignedIntegerValue** method retrieves a **LONG** value (type VT\_I4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="e284b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e284b-105">Syntax</span></span>


```C++
HRESULT GetSignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONG           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e284b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e284b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e284b-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e284b-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e284b-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="e284b-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e284b-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e284b-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e284b-110">Puntero al valor **Long** recuperado.</span><span class="sxs-lookup"><span data-stu-id="e284b-110">Pointer to the retrieved **LONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e284b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e284b-111">Return value</span></span>

<span data-ttu-id="e284b-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e284b-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e284b-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="e284b-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e284b-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e284b-114">Return code</span></span>                                                                                                            | <span data-ttu-id="e284b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e284b-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="e284b-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e284b-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="e284b-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="e284b-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="e284b-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="e284b-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="e284b-119">La propiedad especificada por *key* no es de tipo **Long** .</span><span class="sxs-lookup"><span data-stu-id="e284b-119">The property specified by *key* is not a **LONG** type.</span></span><br/>   |
| <dl> <span data-ttu-id="e284b-120"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="e284b-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="e284b-121">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="e284b-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e284b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e284b-122">Requirements</span></span>



| <span data-ttu-id="e284b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e284b-123">Requirement</span></span> | <span data-ttu-id="e284b-124">Value</span><span class="sxs-lookup"><span data-stu-id="e284b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e284b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e284b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e284b-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e284b-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e284b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e284b-127">Library</span></span><br/> | <dl> <span data-ttu-id="e284b-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e284b-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e284b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e284b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e284b-130">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e284b-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e284b-131">**IPortableDeviceValues::SetSignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="e284b-131">**IPortableDeviceValues::SetSignedIntegerValue**</span></span>](iportabledevicevalues-setsignedintegervalue.md)
</dt> </dl>

 

 




