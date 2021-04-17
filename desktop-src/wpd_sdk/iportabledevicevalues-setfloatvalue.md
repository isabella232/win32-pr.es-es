---
description: El método SetFloatValue agrega un nuevo valor FLOAT (Type VT \_ R4) o sobrescribe uno existente.
ms.assetid: 1e0c9d19-47bf-4d93-a0c0-27e2c4897012
title: 'IPortableDeviceValues:: SetFloatValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 60b42217c925c83e96f2c893c7bc7f11449ebdd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708704"
---
# <a name="iportabledevicevaluessetfloatvalue-method"></a><span data-ttu-id="838dd-103">IPortableDeviceValues:: SetFloatValue (método)</span><span class="sxs-lookup"><span data-stu-id="838dd-103">IPortableDeviceValues::SetFloatValue method</span></span>

<span data-ttu-id="838dd-104">El método **SetFloatValue** agrega un nuevo valor **float** (Type VT \_ R4) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="838dd-104">The **SetFloatValue** method adds a new **FLOAT** value (type VT\_R4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="838dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="838dd-105">Syntax</span></span>


```C++
HRESULT SetFloatValue(
  [in]       REFPROPERTYKEY key,
  [in] const FLOAT          Value
);
```



## <a name="parameters"></a><span data-ttu-id="838dd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="838dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="838dd-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="838dd-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="838dd-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="838dd-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="838dd-109">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="838dd-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="838dd-110">Un valor de **tipo float** que contiene el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="838dd-110">A **FLOAT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="838dd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="838dd-111">Return value</span></span>

<span data-ttu-id="838dd-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="838dd-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="838dd-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="838dd-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="838dd-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="838dd-114">Return code</span></span>                                                                          | <span data-ttu-id="838dd-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="838dd-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="838dd-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="838dd-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="838dd-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="838dd-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="838dd-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="838dd-118">Remarks</span></span>

<span data-ttu-id="838dd-119">Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="838dd-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="838dd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="838dd-120">Requirements</span></span>



| <span data-ttu-id="838dd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="838dd-121">Requirement</span></span> | <span data-ttu-id="838dd-122">Value</span><span class="sxs-lookup"><span data-stu-id="838dd-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838dd-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="838dd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="838dd-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="838dd-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="838dd-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="838dd-125">Library</span></span><br/> | <dl> <span data-ttu-id="838dd-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="838dd-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="838dd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="838dd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="838dd-128">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="838dd-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="838dd-129">**IPortableDeviceValues::GetFloatValue**</span><span class="sxs-lookup"><span data-stu-id="838dd-129">**IPortableDeviceValues::GetFloatValue**</span></span>](iportabledevicevalues-getfloatvalue.md)
</dt> </dl>

 

 




