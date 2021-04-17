---
description: El método SetBufferValue agrega un nuevo valor de BYTE \* (Type VT \_ Vector \| VT \_ UI1) o sobrescribe uno existente.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'IPortableDeviceValues:: SetBufferValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e04b41fdd397d8d03e7e0576d2ba8fb3b6ad1401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660968"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a><span data-ttu-id="3c453-103">IPortableDeviceValues:: SetBufferValue (método)</span><span class="sxs-lookup"><span data-stu-id="3c453-103">IPortableDeviceValues::SetBufferValue method</span></span>

<span data-ttu-id="3c453-104">El método **SetBufferValue** agrega un nuevo valor de **byte** \* (Type VT \_ Vector \| VT \_ UI1) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="3c453-104">The **SetBufferValue** method adds a new **BYTE**\* value (type VT\_VECTOR \| VT\_UI1) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c453-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c453-105">Syntax</span></span>


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
);
```



## <a name="parameters"></a><span data-ttu-id="3c453-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c453-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c453-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3c453-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c453-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="3c453-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="3c453-109">*pValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c453-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c453-110">**Byte \*** que contiene los datos que se van a escribir en el elemento.</span><span class="sxs-lookup"><span data-stu-id="3c453-110">A **BYTE\*** that contains the data to write to the item.</span></span> <span data-ttu-id="3c453-111">Los datos de búfer enviados se copian en la interfaz, por lo que el autor de la llamada puede liberar este búfer después de hacer esta llamada.</span><span class="sxs-lookup"><span data-stu-id="3c453-111">The submitted buffer data is copied to the interface, so the caller can free this buffer after making this call.</span></span>

</dd> <dt>

<span data-ttu-id="3c453-112">*cbValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c453-112">*cbValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c453-113">Tamaño del valor al que apunta *pValue*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3c453-113">The size of the value pointed to by *pValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c453-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c453-114">Return value</span></span>

<span data-ttu-id="3c453-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3c453-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3c453-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="3c453-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3c453-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3c453-117">Return code</span></span>                                                                          | <span data-ttu-id="3c453-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c453-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3c453-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3c453-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3c453-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="3c453-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c453-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c453-121">Remarks</span></span>

<span data-ttu-id="3c453-122">Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="3c453-122">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="3c453-123">La memoria de clave existente se libera adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="3c453-123">The existing key memory is released appropriately.</span></span>

<span data-ttu-id="3c453-124">No se admite el establecimiento de un valor **null** o un búfer de tamaño cero.</span><span class="sxs-lookup"><span data-stu-id="3c453-124">Setting a **NULL** or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c453-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c453-125">Requirements</span></span>



| <span data-ttu-id="3c453-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c453-126">Requirement</span></span> | <span data-ttu-id="3c453-127">Value</span><span class="sxs-lookup"><span data-stu-id="3c453-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c453-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c453-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3c453-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c453-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c453-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c453-130">Library</span></span><br/> | <dl> <span data-ttu-id="3c453-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c453-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c453-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c453-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c453-133">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="3c453-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="3c453-134">**IPortableDeviceValues::GetBufferValue**</span><span class="sxs-lookup"><span data-stu-id="3c453-134">**IPortableDeviceValues::GetBufferValue**</span></span>](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




