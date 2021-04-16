---
description: El método GetFloatValue recupera un valor FLOAT (tipo VT \_ R4) especificado por una clave.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'IPortableDeviceValues:: GetFloatValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649788"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a><span data-ttu-id="4a446-103">IPortableDeviceValues:: GetFloatValue (método)</span><span class="sxs-lookup"><span data-stu-id="4a446-103">IPortableDeviceValues::GetFloatValue method</span></span>

<span data-ttu-id="4a446-104">El método **GetFloatValue** recupera un valor **float** (tipo VT \_ R4) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="4a446-104">The **GetFloatValue** method retrieves a **FLOAT** value (type VT\_R4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a446-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a446-105">Syntax</span></span>


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="4a446-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a446-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a446-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4a446-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a446-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="4a446-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="4a446-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4a446-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a446-110">Puntero al valor de **punto flotante** recuperado.</span><span class="sxs-lookup"><span data-stu-id="4a446-110">Pointer to the retrieved **FLOAT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a446-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a446-111">Return value</span></span>

<span data-ttu-id="4a446-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4a446-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4a446-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="4a446-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4a446-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4a446-114">Return code</span></span>                                                                                             | <span data-ttu-id="4a446-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a446-115">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a446-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4a446-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="4a446-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="4a446-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4a446-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="4a446-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>    | <span data-ttu-id="4a446-119">La propiedad especificada por *key* no es un tipo **float** .</span><span class="sxs-lookup"><span data-stu-id="4a446-119">The property specified by *key* is not a **FLOAT** type.</span></span><br/>  |
| <dl> <span data-ttu-id="4a446-120"><dt>**E \_ \_ ID. de prop \_ no compatible**</dt></span><span class="sxs-lookup"><span data-stu-id="4a446-120"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="4a446-121">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="4a446-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4a446-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a446-122">Requirements</span></span>



| <span data-ttu-id="4a446-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a446-123">Requirement</span></span> | <span data-ttu-id="4a446-124">Value</span><span class="sxs-lookup"><span data-stu-id="4a446-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a446-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a446-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4a446-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a446-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a446-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a446-127">Library</span></span><br/> | <dl> <span data-ttu-id="4a446-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a446-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a446-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a446-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a446-130">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="4a446-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="4a446-131">**IPortableDeviceValues::SetFloatValue**</span><span class="sxs-lookup"><span data-stu-id="4a446-131">**IPortableDeviceValues::SetFloatValue**</span></span>](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




