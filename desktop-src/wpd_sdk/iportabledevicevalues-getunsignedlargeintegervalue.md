---
description: El método GetUnsignedLargeIntegerValue recupera un valor de ULONGLONG (tipo VT \_ UI8) especificado por una clave.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: 'IPortableDeviceValues:: GetUnsignedLargeIntegerValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 48f6093f32d43737b1999c3474f74569ecd3f8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649606"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a><span data-ttu-id="ec62f-103">IPortableDeviceValues:: GetUnsignedLargeIntegerValue (método)</span><span class="sxs-lookup"><span data-stu-id="ec62f-103">IPortableDeviceValues::GetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="ec62f-104">El método **GetUnsignedLargeIntegerValue** recupera un valor de **ULONGLONG** (tipo VT \_ UI8) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="ec62f-104">The **GetUnsignedLargeIntegerValue** method retrieves a **ULONGLONG** value (type VT\_UI8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec62f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec62f-105">Syntax</span></span>


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="ec62f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec62f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec62f-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ec62f-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec62f-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="ec62f-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="ec62f-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ec62f-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec62f-110">Puntero al valor de **ULONGLONG** recuperado.</span><span class="sxs-lookup"><span data-stu-id="ec62f-110">Pointer to the retrieved **ULONGLONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec62f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec62f-111">Return value</span></span>

<span data-ttu-id="ec62f-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ec62f-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ec62f-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="ec62f-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ec62f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ec62f-114">Return code</span></span>                                                                                                            | <span data-ttu-id="ec62f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec62f-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec62f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ec62f-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="ec62f-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="ec62f-117">The method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="ec62f-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="ec62f-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="ec62f-119">La propiedad especificada por *key* no es un tipo **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="ec62f-119">The property specified by *key* is not a **ULONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="ec62f-120"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="ec62f-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="ec62f-121">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="ec62f-121">The property specified by *key* is not in the collection.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="ec62f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec62f-122">Requirements</span></span>



| <span data-ttu-id="ec62f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec62f-123">Requirement</span></span> | <span data-ttu-id="ec62f-124">Value</span><span class="sxs-lookup"><span data-stu-id="ec62f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec62f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec62f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ec62f-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec62f-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec62f-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec62f-127">Library</span></span><br/> | <dl> <span data-ttu-id="ec62f-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec62f-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec62f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec62f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec62f-130">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="ec62f-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ec62f-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="ec62f-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




