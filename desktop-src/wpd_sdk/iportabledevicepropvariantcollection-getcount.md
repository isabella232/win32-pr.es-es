---
description: El método GetCount recupera el número de elementos de esta colección.
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'IPortableDevicePropVariantCollection:: GetCount (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d3a06cb5d89bc09a35a58f9269ba19c488c11e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721583"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a><span data-ttu-id="94cf8-103">IPortableDevicePropVariantCollection:: GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="94cf8-103">IPortableDevicePropVariantCollection::GetCount method</span></span>

<span data-ttu-id="94cf8-104">El método **getCount** recupera el número de elementos de esta colección.</span><span class="sxs-lookup"><span data-stu-id="94cf8-104">The **GetCount** method retrieves the number of items in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="94cf8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94cf8-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="94cf8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94cf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94cf8-107">*pcElems* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="94cf8-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94cf8-108">Puntero a un **valor DWORD** que contiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="94cf8-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94cf8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94cf8-109">Return value</span></span>

<span data-ttu-id="94cf8-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="94cf8-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="94cf8-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="94cf8-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="94cf8-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="94cf8-112">Return code</span></span>                                                                               | <span data-ttu-id="94cf8-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="94cf8-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="94cf8-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="94cf8-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="94cf8-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="94cf8-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="94cf8-116"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="94cf8-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="94cf8-117">Un argumento de puntero necesario era **null**.</span><span class="sxs-lookup"><span data-stu-id="94cf8-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="94cf8-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="94cf8-118">Examples</span></span>

<span data-ttu-id="94cf8-119">Para obtener un ejemplo de cómo usar este método [, consulte recuperación de las categorías funcionales admitidas por un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="94cf8-119">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94cf8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94cf8-120">Requirements</span></span>



| <span data-ttu-id="94cf8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="94cf8-121">Requirement</span></span> | <span data-ttu-id="94cf8-122">Value</span><span class="sxs-lookup"><span data-stu-id="94cf8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94cf8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94cf8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="94cf8-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="94cf8-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="94cf8-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94cf8-125">Library</span></span><br/> | <dl> <span data-ttu-id="94cf8-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94cf8-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94cf8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="94cf8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94cf8-128">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="94cf8-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="94cf8-129">Recuperación de eventos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="94cf8-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="94cf8-130">Recuperando formatos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="94cf8-130">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="94cf8-131">Recuperando métodos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="94cf8-131">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="94cf8-132">Recuperación de las categorías funcionales admitidas por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="94cf8-132">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="94cf8-133">Establecer las propiedades de varios objetos</span><span class="sxs-lookup"><span data-stu-id="94cf8-133">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




