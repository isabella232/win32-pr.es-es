---
description: El método GetIPortableDeviceKeyCollectionValue recupera un valor de IPortableDeviceKeyCollection (tipo VT \_ desconocido) especificado por una clave.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: 'IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7868b71790f6dbb7525fcd1be49b197042a196f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680188"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="6746d-103">IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue (método)</span><span class="sxs-lookup"><span data-stu-id="6746d-103">IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="6746d-104">El método **GetIPortableDeviceKeyCollectionValue** recupera un valor de **IPORTABLEDEVICEKEYCOLLECTION** (tipo VT \_ desconocido) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="6746d-104">The **GetIPortableDeviceKeyCollectionValue** method retrieves an **IPortableDeviceKeyCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="6746d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6746d-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="6746d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6746d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6746d-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6746d-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6746d-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="6746d-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6746d-109">*ppValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6746d-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6746d-110">Puntero al puntero de la interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) recuperada.</span><span class="sxs-lookup"><span data-stu-id="6746d-110">Pointer to the retrieved [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface pointer.</span></span> <span data-ttu-id="6746d-111">El autor de la llamada es responsable de llamar a **Release** en la interfaz recuperada.</span><span class="sxs-lookup"><span data-stu-id="6746d-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6746d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6746d-112">Return value</span></span>

<span data-ttu-id="6746d-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6746d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6746d-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="6746d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6746d-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6746d-115">Return code</span></span>                                                                                                            | <span data-ttu-id="6746d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6746d-116">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6746d-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6746d-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="6746d-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="6746d-118">The method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="6746d-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="6746d-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="6746d-120">La propiedad especificada por *key* no es una interfaz **IPortableDeviceKeyCollection** .</span><span class="sxs-lookup"><span data-stu-id="6746d-120">The property specified by *key* is not an **IPortableDeviceKeyCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="6746d-121"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="6746d-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="6746d-122">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="6746d-122">The property specified by *key* is not in the collection.</span></span><br/>                             |



 

## <a name="examples"></a><span data-ttu-id="6746d-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6746d-123">Examples</span></span>

<span data-ttu-id="6746d-124">Para obtener un ejemplo de cómo usar este método, vea [recuperar eventos de servicio admitidos](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="6746d-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6746d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6746d-125">Requirements</span></span>



| <span data-ttu-id="6746d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6746d-126">Requirement</span></span> | <span data-ttu-id="6746d-127">Value</span><span class="sxs-lookup"><span data-stu-id="6746d-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6746d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6746d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6746d-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="6746d-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6746d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6746d-130">Library</span></span><br/> | <dl> <span data-ttu-id="6746d-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6746d-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6746d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6746d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6746d-133">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="6746d-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="6746d-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="6746d-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[<span data-ttu-id="6746d-135">Recuperación de eventos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="6746d-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="6746d-136">Recuperando métodos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="6746d-136">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




