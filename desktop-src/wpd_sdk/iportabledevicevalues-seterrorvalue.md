---
description: El método SetErrorValue agrega un nuevo valor HRESULT (tipo VT \_ error) o sobrescribe uno existente.
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'IPortableDeviceValues:: SetErrorValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 19c7ca57d325e31fd9cd8e0bf5130dc594b0b8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660967"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a><span data-ttu-id="d2bd3-103">IPortableDeviceValues:: SetErrorValue (método)</span><span class="sxs-lookup"><span data-stu-id="d2bd3-103">IPortableDeviceValues::SetErrorValue method</span></span>

<span data-ttu-id="d2bd3-104">El método **SetErrorValue** agrega un nuevo valor **HRESULT** (tipo VT \_ error) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-104">The **SetErrorValue** method adds a new **HRESULT** value (type VT\_ERROR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2bd3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2bd3-105">Syntax</span></span>


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
);
```



## <a name="parameters"></a><span data-ttu-id="d2bd3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2bd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2bd3-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d2bd3-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2bd3-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="d2bd3-109">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d2bd3-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2bd3-110">**HRESULT** que contiene el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-110">An **HRESULT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2bd3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2bd3-111">Return value</span></span>

<span data-ttu-id="d2bd3-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d2bd3-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d2bd3-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d2bd3-114">Return code</span></span>                                                                          | <span data-ttu-id="d2bd3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2bd3-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d2bd3-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d2bd3-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d2bd3-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d2bd3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2bd3-118">Remarks</span></span>

<span data-ttu-id="d2bd3-119">Si un valor existente tiene la misma clave especificada por el parámetro *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2bd3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2bd3-120">Requirements</span></span>



| <span data-ttu-id="d2bd3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2bd3-121">Requirement</span></span> | <span data-ttu-id="d2bd3-122">Value</span><span class="sxs-lookup"><span data-stu-id="d2bd3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2bd3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2bd3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d2bd3-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2bd3-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2bd3-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2bd3-125">Library</span></span><br/> | <dl> <span data-ttu-id="d2bd3-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2bd3-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2bd3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2bd3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2bd3-128">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d2bd3-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d2bd3-129">**IPortableDeviceValues::GetErrorValue**</span><span class="sxs-lookup"><span data-stu-id="d2bd3-129">**IPortableDeviceValues::GetErrorValue**</span></span>](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




