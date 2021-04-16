---
description: El método GetIUnknownValue recupera un valor de interfaz IUnknown (tipo VT \_ desconocido) especificado por una clave.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: 'IPortableDeviceValues:: GetIUnknownValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bc7ecfdc699cfe5f572c303d2c8a9e71bafc026b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105719005"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a><span data-ttu-id="b3394-103">IPortableDeviceValues:: GetIUnknownValue (método)</span><span class="sxs-lookup"><span data-stu-id="b3394-103">IPortableDeviceValues::GetIUnknownValue method</span></span>

<span data-ttu-id="b3394-104">El método **GetIUnknownValue** recupera un valor de interfaz **IUNKNOWN** (tipo VT \_ desconocido) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="b3394-104">The **GetIUnknownValue** method retrieves an **IUnknown** interface value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3394-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3394-105">Syntax</span></span>


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="b3394-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3394-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3394-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b3394-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3394-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="b3394-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b3394-109">*ppValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b3394-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3394-110">Dirección de una variable que recibe un puntero a la interfaz **IUnknown** recuperada.</span><span class="sxs-lookup"><span data-stu-id="b3394-110">Address of a variable that receives a pointer to the retrieved **IUnknown** interface.</span></span> <span data-ttu-id="b3394-111">El autor de la llamada es responsable de llamar a **Release** en la interfaz recuperada.</span><span class="sxs-lookup"><span data-stu-id="b3394-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3394-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3394-112">Return value</span></span>

<span data-ttu-id="b3394-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b3394-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b3394-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="b3394-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b3394-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b3394-115">Return code</span></span>                                                                                                            | <span data-ttu-id="b3394-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3394-116">Description</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3394-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b3394-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="b3394-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="b3394-118">The method succeeded.</span></span><br/>                                             |
| <dl> <span data-ttu-id="b3394-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="b3394-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="b3394-120">La propiedad especificada por *key* no es una interfaz **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="b3394-120">The property specified by *key* is not an **IUnknown** interface.</span></span><br/> |
| <dl> <span data-ttu-id="b3394-121"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="b3394-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="b3394-122">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="b3394-122">The property specified by *key* is not in the collection.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="b3394-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3394-123">Requirements</span></span>



| <span data-ttu-id="b3394-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3394-124">Requirement</span></span> | <span data-ttu-id="b3394-125">Value</span><span class="sxs-lookup"><span data-stu-id="b3394-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3394-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3394-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b3394-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3394-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3394-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3394-128">Library</span></span><br/> | <dl> <span data-ttu-id="b3394-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3394-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3394-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3394-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3394-131">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b3394-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b3394-132">**IPortableDeviceValues::SetIUnknownValue**</span><span class="sxs-lookup"><span data-stu-id="b3394-132">**IPortableDeviceValues::SetIUnknownValue**</span></span>](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




