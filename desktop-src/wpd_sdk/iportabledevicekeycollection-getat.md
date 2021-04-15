---
description: El método GetAd recupera un PROPERTYKEY de la colección por índice.
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'IPortableDeviceKeyCollection:: GetAt (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708997"
---
# <a name="iportabledevicekeycollectiongetat-method"></a><span data-ttu-id="ea259-103">IPortableDeviceKeyCollection:: GetAt (método)</span><span class="sxs-lookup"><span data-stu-id="ea259-103">IPortableDeviceKeyCollection::GetAt method</span></span>

<span data-ttu-id="ea259-104">El método **GetAd** recupera un **PROPERTYKEY** de la colección por índice.</span><span class="sxs-lookup"><span data-stu-id="ea259-104">The **GetAt** method retrieves a **PROPERTYKEY** from the collection by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea259-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea259-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a><span data-ttu-id="ea259-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea259-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea259-107">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea259-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea259-108">**DWORD** que contiene el índice de la clave que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="ea259-108">**DWORD** that contains the index of the key to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="ea259-109">*pKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ea259-109">*pKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea259-110">Puntero a un objeto **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="ea259-110">Pointer to a **PROPERTYKEY** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea259-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea259-111">Return value</span></span>

<span data-ttu-id="ea259-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ea259-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ea259-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="ea259-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ea259-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ea259-114">Return code</span></span>                                                                                  | <span data-ttu-id="ea259-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea259-115">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="ea259-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ea259-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ea259-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="ea259-117">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="ea259-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ea259-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ea259-119">El índice pasado estaba fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="ea259-119">The index passed in was out of range.</span></span><br/>     |
| <dl> <span data-ttu-id="ea259-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="ea259-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ea259-121">Un argumento de puntero necesario era **null**.</span><span class="sxs-lookup"><span data-stu-id="ea259-121">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="ea259-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ea259-122">Examples</span></span>

<span data-ttu-id="ea259-123">Para obtener un ejemplo de cómo usar este método, vea [recuperar eventos de servicio admitidos](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="ea259-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea259-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea259-124">Requirements</span></span>



| <span data-ttu-id="ea259-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea259-125">Requirement</span></span> | <span data-ttu-id="ea259-126">Value</span><span class="sxs-lookup"><span data-stu-id="ea259-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea259-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea259-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ea259-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea259-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea259-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea259-129">Library</span></span><br/> | <dl> <span data-ttu-id="ea259-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea259-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea259-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea259-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea259-132">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="ea259-132">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="ea259-133">Recuperación de eventos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="ea259-133">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="ea259-134">Recuperando métodos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="ea259-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




