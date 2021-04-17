---
description: El método GetIPortableDevicePropVariantCollectionValue recupera un valor de IPortableDevicePropVariantCollection (tipo VT \_ desconocido) especificado por una clave.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: 'IPortableDeviceValues:: GetIPortableDevicePropVariantCollectionValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7deb73d10f2e2daa5d06d6cb4394c43778af2ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709220"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a><span data-ttu-id="be968-103">IPortableDeviceValues:: GetIPortableDevicePropVariantCollectionValue (método)</span><span class="sxs-lookup"><span data-stu-id="be968-103">IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue method</span></span>

<span data-ttu-id="be968-104">El método **GetIPortableDevicePropVariantCollectionValue** recupera un valor de **IPORTABLEDEVICEPROPVARIANTCOLLECTION** (tipo VT \_ desconocido) especificado por una clave.</span><span class="sxs-lookup"><span data-stu-id="be968-104">The **GetIPortableDevicePropVariantCollectionValue** method retrieves an **IPortableDevicePropVariantCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="be968-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be968-105">Syntax</span></span>


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="be968-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be968-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be968-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="be968-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be968-108">Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="be968-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="be968-109">*ppValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="be968-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be968-110">Dirección de una variable que recibe un puntero a la interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) recuperada.</span><span class="sxs-lookup"><span data-stu-id="be968-110">Address of a variable that receives a pointer to the retrieved [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface.</span></span> <span data-ttu-id="be968-111">El autor de la llamada es responsable de llamar a **Release** en la interfaz recuperada.</span><span class="sxs-lookup"><span data-stu-id="be968-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be968-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be968-112">Return value</span></span>

<span data-ttu-id="be968-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="be968-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="be968-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="be968-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="be968-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="be968-115">Return code</span></span>                                                                                                            | <span data-ttu-id="be968-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="be968-116">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="be968-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="be968-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="be968-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="be968-118">The method succeeded.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="be968-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="be968-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="be968-120">La propiedad especificada por *key* no es una interfaz **IPortableDevicePropVariantCollection** .</span><span class="sxs-lookup"><span data-stu-id="be968-120">The property specified by *key* is not an **IPortableDevicePropVariantCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="be968-121"><dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="be968-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="be968-122">La propiedad especificada por la *clave* no está en la colección.</span><span class="sxs-lookup"><span data-stu-id="be968-122">The property specified by *key* is not in the collection.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="be968-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be968-123">Requirements</span></span>



| <span data-ttu-id="be968-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="be968-124">Requirement</span></span> | <span data-ttu-id="be968-125">Value</span><span class="sxs-lookup"><span data-stu-id="be968-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be968-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be968-126">Header</span></span><br/>  | <dl> <span data-ttu-id="be968-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="be968-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="be968-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be968-128">Library</span></span><br/> | <dl> <span data-ttu-id="be968-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be968-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be968-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="be968-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be968-131">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="be968-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="be968-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="be968-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




