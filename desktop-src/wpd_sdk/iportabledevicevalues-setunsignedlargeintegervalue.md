---
description: El método SetUnsignedLargeIntegerValue agrega un nuevo valor ULONGLONG (Type VT \_ UI8) o sobrescribe uno existente.
ms.assetid: 64874b86-7bf1-407a-8fff-a2c07c22f0cb
title: 'IPortableDeviceValues:: SetUnsignedLargeIntegerValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c1ade76b4242c7508cb325e90c567349afcdc9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708682"
---
# <a name="iportabledevicevaluessetunsignedlargeintegervalue-method"></a><span data-ttu-id="5dd0a-103">IPortableDeviceValues:: SetUnsignedLargeIntegerValue (método)</span><span class="sxs-lookup"><span data-stu-id="5dd0a-103">IPortableDeviceValues::SetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="5dd0a-104">El método **SetUnsignedLargeIntegerValue** agrega un nuevo valor **ULONGLONG** (Type VT \_ UI8) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-104">The **SetUnsignedLargeIntegerValue** method adds a new **ULONGLONG** value (type VT\_UI8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd0a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5dd0a-105">Syntax</span></span>


```C++
HRESULT SetUnsignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONGLONG      Value
);
```



## <a name="parameters"></a><span data-ttu-id="5dd0a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5dd0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dd0a-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5dd0a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd0a-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="5dd0a-109">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5dd0a-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd0a-110">**ULONGLONG** que especifica el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-110">A **ULONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dd0a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5dd0a-111">Return value</span></span>

<span data-ttu-id="5dd0a-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5dd0a-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5dd0a-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5dd0a-114">Return code</span></span>                                                                          | <span data-ttu-id="5dd0a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5dd0a-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5dd0a-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5dd0a-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5dd0a-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5dd0a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dd0a-118">Requirements</span></span>



| <span data-ttu-id="5dd0a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dd0a-119">Requirement</span></span> | <span data-ttu-id="5dd0a-120">Value</span><span class="sxs-lookup"><span data-stu-id="5dd0a-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd0a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5dd0a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5dd0a-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dd0a-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5dd0a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5dd0a-123">Library</span></span><br/> | <dl> <span data-ttu-id="5dd0a-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5dd0a-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dd0a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5dd0a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd0a-126">Agregar un recurso a un objeto</span><span class="sxs-lookup"><span data-stu-id="5dd0a-126">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="5dd0a-127">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="5dd0a-127">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="5dd0a-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="5dd0a-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-getunsignedlargeintegervalue.md)
</dt> </dl>

 

 




