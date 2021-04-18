---
description: El método GetAd recupera un valor de la colección utilizando el índice de base cero proporcionado.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'IPortableDeviceValues:: GetAt (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44126b69dc4e8720fde687d47dc70dd97e104c72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649881"
---
# <a name="iportabledevicevaluesgetat-method"></a><span data-ttu-id="4e9b1-103">IPortableDeviceValues:: GetAt (método)</span><span class="sxs-lookup"><span data-stu-id="4e9b1-103">IPortableDeviceValues::GetAt method</span></span>

<span data-ttu-id="4e9b1-104">El método **GetAd** recupera un valor de la colección utilizando el índice de base cero proporcionado.</span><span class="sxs-lookup"><span data-stu-id="4e9b1-104">The **GetAt** method retrieves a value from the collection using the supplied zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e9b1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e9b1-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="4e9b1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e9b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e9b1-107">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4e9b1-107">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e9b1-108">**DWORD** que especifica un índice basado en cero en la colección.</span><span class="sxs-lookup"><span data-stu-id="4e9b1-108">A **DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="4e9b1-109">*pKey* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4e9b1-109">*pKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e9b1-110">Un puntero **PROPERTYKEY** opcional que recupera la clave del elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="4e9b1-110">An optional **PROPERTYKEY** pointer that retrieves the key of the specified item.</span></span>

</dd> <dt>

<span data-ttu-id="4e9b1-111">*pValue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4e9b1-111">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e9b1-112">**PROPVARIANT** opcional que recupera el valor del elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="4e9b1-112">An optional **PROPVARIANT** that retrieves the value of the specified item.</span></span> <span data-ttu-id="4e9b1-113">El autor de la llamada debe liberar la memoria mediante una llamada a **PropVariantClear** cuando se realiza con ella.</span><span class="sxs-lookup"><span data-stu-id="4e9b1-113">The caller must free the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e9b1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e9b1-114">Return value</span></span>

<span data-ttu-id="4e9b1-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4e9b1-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4e9b1-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="4e9b1-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4e9b1-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4e9b1-117">Return code</span></span>                                                                                  | <span data-ttu-id="4e9b1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e9b1-118">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="4e9b1-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4e9b1-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4e9b1-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="4e9b1-120">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="4e9b1-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4e9b1-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4e9b1-122">Se ha especificado un número de índice no válido.</span><span class="sxs-lookup"><span data-stu-id="4e9b1-122">An invalid index number was specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e9b1-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e9b1-123">Remarks</span></span>

<span data-ttu-id="4e9b1-124">Si una propiedad indica un valor de tipo VT \_ Unknown, la propiedad será uno de los dispositivos portátiles de Windows ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) o [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span><span class="sxs-lookup"><span data-stu-id="4e9b1-124">If a property indicates a value of type VT\_UNKNOWN, the property will be one of the Windows Portable Devices ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) or [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span></span> <span data-ttu-id="4e9b1-125">Los dispositivos portátiles de Windows no pueden devolver otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="4e9b1-125">No other interfaces can be returned by Windows Portable Devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e9b1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e9b1-126">Requirements</span></span>



| <span data-ttu-id="4e9b1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e9b1-127">Requirement</span></span> | <span data-ttu-id="4e9b1-128">Value</span><span class="sxs-lookup"><span data-stu-id="4e9b1-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e9b1-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e9b1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4e9b1-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e9b1-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e9b1-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e9b1-131">Library</span></span><br/> | <dl> <span data-ttu-id="4e9b1-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e9b1-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e9b1-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e9b1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e9b1-134">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="4e9b1-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="4e9b1-135">**IPortableDeviceValues:: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="4e9b1-135">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




