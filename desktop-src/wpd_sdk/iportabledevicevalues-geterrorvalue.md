---
description: El método GetErrorValue recupera un valor HRESULT (tipo VT \_ error) especificado por una clave.
ms.assetid: af57ddbd-5503-4b9b-bd75-ba9c9c202b73
title: 'IPortableDeviceValues:: GetErrorValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 86e5dacfa398cfe2bb57bfd289e4c8e792f14a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649830"
---
# <a name="iportabledevicevaluesgeterrorvalue-method"></a><span data-ttu-id="c1948-103">IPortableDeviceValues:: GetErrorValue (método)</span><span class="sxs-lookup"><span data-stu-id="c1948-103">IPortableDeviceValues::GetErrorValue method</span></span>

<span data-ttu-id="c1948-104">El método **GetErrorValue** recupera un valor **HRESULT** (tipo VT \_ error) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="c1948-104">The **GetErrorValue** method retrieves an **HRESULT** value (type VT\_ERROR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1948-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1948-105">Syntax</span></span>


```C++
HRESULT GetErrorValue(
  [in]  REFPROPERTYKEY key,
  [out] HRESULT        *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="c1948-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1948-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1948-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c1948-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1948-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c1948-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c1948-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c1948-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1948-110">Puntero al valor **HRESULT** recuperado.</span><span class="sxs-lookup"><span data-stu-id="c1948-110">Pointer to the retrieved **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1948-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1948-111">Return value</span></span>

<span data-ttu-id="c1948-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c1948-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c1948-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="c1948-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c1948-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c1948-114">Return code</span></span>                                                                                                            | <span data-ttu-id="c1948-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1948-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1948-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c1948-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="c1948-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="c1948-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="c1948-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="c1948-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="c1948-119">La propiedad especificada por *key* no es un tipo **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1948-119">The property specified by *key* is not an **HRESULT** type.</span></span><br/> |
| <dl> <span data-ttu-id="c1948-120"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="c1948-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="c1948-121">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="c1948-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="c1948-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1948-122">Requirements</span></span>



| <span data-ttu-id="c1948-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1948-123">Requirement</span></span> | <span data-ttu-id="c1948-124">Value</span><span class="sxs-lookup"><span data-stu-id="c1948-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1948-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1948-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c1948-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1948-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1948-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1948-127">Library</span></span><br/> | <dl> <span data-ttu-id="c1948-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1948-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1948-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1948-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1948-130">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="c1948-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c1948-131">**IPortableDeviceValues::SetErrorValue**</span><span class="sxs-lookup"><span data-stu-id="c1948-131">**IPortableDeviceValues::SetErrorValue**</span></span>](iportabledevicevalues-seterrorvalue.md)
</dt> </dl>

 

 




