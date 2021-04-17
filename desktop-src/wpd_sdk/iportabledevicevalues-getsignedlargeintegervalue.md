---
description: El método GetSignedLargeIntegerValue recupera un valor de LONGLONG (tipo VT \_ i8) especificado por una clave.
ms.assetid: b8d2a0b6-7ca3-4a56-a502-cc18b08df22a
title: 'IPortableDeviceValues:: GetSignedLargeIntegerValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5fc41c263ffdef540300a08f88665a6489fa9d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680658"
---
# <a name="iportabledevicevaluesgetsignedlargeintegervalue-method"></a><span data-ttu-id="c7b0a-103">IPortableDeviceValues:: GetSignedLargeIntegerValue (método)</span><span class="sxs-lookup"><span data-stu-id="c7b0a-103">IPortableDeviceValues::GetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="c7b0a-104">El método **GetSignedLargeIntegerValue** recupera un valor de **LONGLONG** (tipo VT \_ i8) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="c7b0a-104">The **GetSignedLargeIntegerValue** method retrieves a **LONGLONG** value (type VT\_I8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7b0a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7b0a-105">Syntax</span></span>


```C++
HRESULT GetSignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONGLONG       *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="c7b0a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7b0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7b0a-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c7b0a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b0a-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c7b0a-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c7b0a-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c7b0a-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b0a-110">Puntero al valor **ULong** recuperado.</span><span class="sxs-lookup"><span data-stu-id="c7b0a-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7b0a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7b0a-111">Return value</span></span>

<span data-ttu-id="c7b0a-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c7b0a-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c7b0a-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="c7b0a-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c7b0a-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c7b0a-114">Return code</span></span>                                                                                                            | <span data-ttu-id="c7b0a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7b0a-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7b0a-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c7b0a-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="c7b0a-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="c7b0a-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="c7b0a-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="c7b0a-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="c7b0a-119">La propiedad especificada por *key* no es un tipo **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="c7b0a-119">The property specified by *key* is not a **LONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="c7b0a-120"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="c7b0a-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="c7b0a-121">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="c7b0a-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="c7b0a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7b0a-122">Requirements</span></span>



| <span data-ttu-id="c7b0a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7b0a-123">Requirement</span></span> | <span data-ttu-id="c7b0a-124">Value</span><span class="sxs-lookup"><span data-stu-id="c7b0a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b0a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7b0a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c7b0a-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7b0a-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7b0a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7b0a-127">Library</span></span><br/> | <dl> <span data-ttu-id="c7b0a-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7b0a-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7b0a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7b0a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b0a-130">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="c7b0a-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c7b0a-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="c7b0a-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-setsignedlargeintegervalue.md)
</dt> </dl>

 

 




