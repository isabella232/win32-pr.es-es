---
description: El método GetIPortableDeviceValuesValue recupera un valor de IPortableDeviceValues (tipo VT \_ desconocido) especificado por una clave.
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: 'IPortableDeviceValues:: GetIPortableDeviceValuesValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9583ea157c1e3395fd9814b1a2e78af3f1985b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650129"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a><span data-ttu-id="6d52a-103">IPortableDeviceValues:: GetIPortableDeviceValuesValue (método)</span><span class="sxs-lookup"><span data-stu-id="6d52a-103">IPortableDeviceValues::GetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="6d52a-104">El método **GetIPortableDeviceValuesValue** recupera un valor de **IPORTABLEDEVICEVALUES** (tipo VT \_ desconocido) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="6d52a-104">The **GetIPortableDeviceValuesValue** method retrieves an **IPortableDeviceValues** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d52a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d52a-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="6d52a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d52a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d52a-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6d52a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d52a-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="6d52a-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6d52a-109">*ppValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6d52a-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d52a-110">Dirección de una variable que recibe un puntero a la interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) recuperada.</span><span class="sxs-lookup"><span data-stu-id="6d52a-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span> <span data-ttu-id="6d52a-111">El autor de la llamada es responsable de llamar a **Release** en la interfaz recuperada.</span><span class="sxs-lookup"><span data-stu-id="6d52a-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d52a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d52a-112">Return value</span></span>

<span data-ttu-id="6d52a-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6d52a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6d52a-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="6d52a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6d52a-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6d52a-115">Return code</span></span>                                                                                                            | <span data-ttu-id="6d52a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d52a-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d52a-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6d52a-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="6d52a-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="6d52a-118">The method succeeded.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="6d52a-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="6d52a-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="6d52a-120">La propiedad especificada por *key* no es una interfaz **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="6d52a-120">The property specified by *key* is not an **IPortableDeviceValues** interface.</span></span><br/> |
| <dl> <span data-ttu-id="6d52a-121"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="6d52a-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="6d52a-122">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="6d52a-122">The property specified by *key* is not in the collection.</span></span><br/>                      |



 

## <a name="examples"></a><span data-ttu-id="6d52a-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6d52a-123">Examples</span></span>

<span data-ttu-id="6d52a-124">Para obtener un ejemplo de cómo usar este método, vea [recuperar eventos de servicio admitidos](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="6d52a-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d52a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d52a-125">Requirements</span></span>



| <span data-ttu-id="6d52a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d52a-126">Requirement</span></span> | <span data-ttu-id="6d52a-127">Value</span><span class="sxs-lookup"><span data-stu-id="6d52a-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d52a-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d52a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6d52a-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d52a-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d52a-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d52a-130">Library</span></span><br/> | <dl> <span data-ttu-id="6d52a-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d52a-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d52a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d52a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d52a-133">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="6d52a-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="6d52a-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span><span class="sxs-lookup"><span data-stu-id="6d52a-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[<span data-ttu-id="6d52a-135">Recuperación de eventos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="6d52a-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="6d52a-136">Recuperación de las capacidades de representación admitidas por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="6d52a-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




