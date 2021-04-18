---
description: El método GetAd recupera un elemento de la colección mediante un índice basado en cero.
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'IPortableDevicePropVariantCollection:: GetAt (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0833c69b537fa230320ef69707a6f4302a8ca1ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721584"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a><span data-ttu-id="9c21f-103">IPortableDevicePropVariantCollection:: GetAt (método)</span><span class="sxs-lookup"><span data-stu-id="9c21f-103">IPortableDevicePropVariantCollection::GetAt method</span></span>

<span data-ttu-id="9c21f-104">El método **GetAd** recupera un elemento de la colección mediante un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="9c21f-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c21f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c21f-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="9c21f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c21f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c21f-107">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c21f-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c21f-108">**DWORD** que contiene el índice de base cero del elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="9c21f-108">**DWORD** that contains the zero-based index of the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9c21f-109">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9c21f-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c21f-110">Puntero a una estructura **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="9c21f-110">Pointer to a **PROPVARIANT** structure.</span></span> <span data-ttu-id="9c21f-111">El autor de la llamada es responsable de liberar esta memoria mediante una llamada a **PropVariantClear**.</span><span class="sxs-lookup"><span data-stu-id="9c21f-111">The caller is responsible for freeing this memory by calling **PropVariantClear**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c21f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c21f-112">Return value</span></span>

<span data-ttu-id="9c21f-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9c21f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9c21f-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="9c21f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9c21f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9c21f-115">Return code</span></span>                                                                                  | <span data-ttu-id="9c21f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c21f-116">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="9c21f-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9c21f-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9c21f-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="9c21f-118">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="9c21f-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="9c21f-119"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="9c21f-120">Un argumento de puntero necesario era **null**.</span><span class="sxs-lookup"><span data-stu-id="9c21f-120">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="9c21f-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9c21f-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9c21f-122">El índice que se pasó estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="9c21f-122">The index that was passed in was out of range.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="9c21f-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9c21f-123">Examples</span></span>

<span data-ttu-id="9c21f-124">Para obtener un ejemplo de cómo usar este método [, consulte recuperación de las categorías funcionales admitidas por un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="9c21f-124">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c21f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c21f-125">Requirements</span></span>



| <span data-ttu-id="9c21f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c21f-126">Requirement</span></span> | <span data-ttu-id="9c21f-127">Value</span><span class="sxs-lookup"><span data-stu-id="9c21f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c21f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c21f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9c21f-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c21f-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c21f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c21f-130">Library</span></span><br/> | <dl> <span data-ttu-id="9c21f-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c21f-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c21f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c21f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c21f-133">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="9c21f-133">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="9c21f-134">Recuperar un identificador de objeto de un identificador único persistente</span><span class="sxs-lookup"><span data-stu-id="9c21f-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[<span data-ttu-id="9c21f-135">Recuperación de eventos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="9c21f-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="9c21f-136">Recuperando formatos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="9c21f-136">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="9c21f-137">Recuperando métodos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="9c21f-137">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="9c21f-138">Recuperación de los tipos de contenido admitidos por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c21f-138">Retrieving the Content Types Supported by a Device</span></span>](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="9c21f-139">Recuperación de las categorías funcionales admitidas por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c21f-139">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="9c21f-140">Recuperación de los identificadores de objetos funcionales de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c21f-140">Retrieving the Functional Object Identifiers for a Device</span></span>](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[<span data-ttu-id="9c21f-141">Recuperación de las capacidades de representación admitidas por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c21f-141">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="9c21f-142">Establecer las propiedades de varios objetos</span><span class="sxs-lookup"><span data-stu-id="9c21f-142">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




