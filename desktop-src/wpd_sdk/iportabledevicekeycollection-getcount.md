---
description: El método GetCount recupera el número de claves de esta colección.
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
title: 'IPortableDeviceKeyCollection:: GetCount (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e867a171039a97cc0f83198f72eecaeb57ad3c16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709153"
---
# <a name="iportabledevicekeycollectiongetcount-method"></a><span data-ttu-id="bdcc7-103">IPortableDeviceKeyCollection:: GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="bdcc7-103">IPortableDeviceKeyCollection::GetCount method</span></span>

<span data-ttu-id="bdcc7-104">El método **getCount** recupera el número de claves de esta colección.</span><span class="sxs-lookup"><span data-stu-id="bdcc7-104">The **GetCount** method retrieves the number of keys in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdcc7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bdcc7-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="bdcc7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdcc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdcc7-107">*pcElems* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bdcc7-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcc7-108">Puntero a un **valor DWORD** que contiene el número de claves de la colección.</span><span class="sxs-lookup"><span data-stu-id="bdcc7-108">Pointer to a **DWORD** that contains the number of keys in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdcc7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bdcc7-109">Return value</span></span>

<span data-ttu-id="bdcc7-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bdcc7-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bdcc7-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="bdcc7-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bdcc7-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bdcc7-112">Return code</span></span>                                                                               | <span data-ttu-id="bdcc7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdcc7-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="bdcc7-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bdcc7-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="bdcc7-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="bdcc7-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="bdcc7-116"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="bdcc7-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="bdcc7-117">Un argumento de puntero necesario era **null**.</span><span class="sxs-lookup"><span data-stu-id="bdcc7-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="bdcc7-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bdcc7-118">Examples</span></span>

<span data-ttu-id="bdcc7-119">Para obtener un ejemplo de cómo usar este método, vea [recuperar eventos de servicio admitidos](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="bdcc7-119">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdcc7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdcc7-120">Requirements</span></span>



| <span data-ttu-id="bdcc7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdcc7-121">Requirement</span></span> | <span data-ttu-id="bdcc7-122">Value</span><span class="sxs-lookup"><span data-stu-id="bdcc7-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdcc7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdcc7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bdcc7-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdcc7-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdcc7-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdcc7-125">Library</span></span><br/> | <dl> <span data-ttu-id="bdcc7-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdcc7-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdcc7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdcc7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdcc7-128">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="bdcc7-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="bdcc7-129">Recuperación de eventos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="bdcc7-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="bdcc7-130">Recuperando métodos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="bdcc7-130">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




