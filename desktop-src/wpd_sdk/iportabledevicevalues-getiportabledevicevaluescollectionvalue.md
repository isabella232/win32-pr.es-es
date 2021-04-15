---
description: El método GetIPortableDeviceValuesCollectionValue recupera un valor de IPortableDeviceValuesCollection (tipo VT \_ desconocido) especificado por una clave.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: 'IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3db3b8410ca82a97a41fdf45ee3f866cb8d2e4b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708705"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="f8317-103">IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue (método)</span><span class="sxs-lookup"><span data-stu-id="f8317-103">IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="f8317-104">El método **GetIPortableDeviceValuesCollectionValue** recupera un valor de **IPORTABLEDEVICEVALUESCOLLECTION** (tipo VT \_ desconocido) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="f8317-104">The **GetIPortableDeviceValuesCollectionValue** method retrieves an **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8317-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8317-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="f8317-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8317-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8317-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f8317-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8317-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="f8317-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f8317-109">*ppValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f8317-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8317-110">Dirección de una variable que recibe un puntero a la interfaz [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) recuperada.</span><span class="sxs-lookup"><span data-stu-id="f8317-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) interface.</span></span> <span data-ttu-id="f8317-111">El autor de la llamada es responsable de llamar a **Release** en la interfaz recuperada.</span><span class="sxs-lookup"><span data-stu-id="f8317-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8317-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8317-112">Return value</span></span>

<span data-ttu-id="f8317-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f8317-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f8317-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="f8317-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f8317-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f8317-115">Return code</span></span>                                                                                                            | <span data-ttu-id="f8317-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8317-116">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8317-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f8317-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="f8317-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="f8317-118">The method succeeded.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="f8317-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="f8317-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="f8317-120">La propiedad especificada por *key* no es una interfaz **IPortableDeviceValuesCollection** .</span><span class="sxs-lookup"><span data-stu-id="f8317-120">The property specified by *key* is not an **IPortableDeviceValuesCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="f8317-121"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="f8317-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="f8317-122">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="f8317-122">The property specified by *key* is not in the collection.</span></span><br/>                                |



 

## <a name="examples"></a><span data-ttu-id="f8317-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f8317-123">Examples</span></span>

<span data-ttu-id="f8317-124">Para obtener un ejemplo de cómo usar este método, consulte [recuperación de las capacidades de representación admitidas por un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="f8317-124">For an example of how to use this method, see [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8317-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8317-125">Requirements</span></span>



| <span data-ttu-id="f8317-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8317-126">Requirement</span></span> | <span data-ttu-id="f8317-127">Value</span><span class="sxs-lookup"><span data-stu-id="f8317-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8317-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8317-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f8317-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8317-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8317-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8317-130">Library</span></span><br/> | <dl> <span data-ttu-id="f8317-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8317-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8317-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8317-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8317-133">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f8317-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f8317-134">Recuperación de las capacidades de representación admitidas por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="f8317-134">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="f8317-135">**SetIPortableDeviceValuesCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="f8317-135">**SetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




