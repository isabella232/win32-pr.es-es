---
description: El método Clear libera y, a continuación, quita todos los elementos de la colección. La colección se considera vacía después de llamar a este método.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'IPortableDevicePropVariantCollection:: CLEAR (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fa7c2a8dddeb74b5ac666da2561bd6ee6536821a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718898"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a><span data-ttu-id="ad2da-104">IPortableDevicePropVariantCollection:: CLEAR (método)</span><span class="sxs-lookup"><span data-stu-id="ad2da-104">IPortableDevicePropVariantCollection::Clear method</span></span>

<span data-ttu-id="ad2da-105">El método **Clear** libera y, a continuación, quita todos los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="ad2da-105">The **Clear** method frees, and then removes, all items from the collection.</span></span> <span data-ttu-id="ad2da-106">La colección se considera vacía después de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="ad2da-106">The collection is considered empty after calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad2da-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad2da-107">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="ad2da-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad2da-108">Parameters</span></span>

<span data-ttu-id="ad2da-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ad2da-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad2da-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad2da-110">Return value</span></span>

<span data-ttu-id="ad2da-111">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ad2da-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ad2da-112">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="ad2da-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ad2da-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ad2da-113">Return code</span></span>                                                                          | <span data-ttu-id="ad2da-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad2da-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ad2da-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ad2da-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ad2da-116">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="ad2da-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ad2da-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad2da-117">Remarks</span></span>

<span data-ttu-id="ad2da-118">Después de llamar a **Clear**, la colección se considera de tipo menos, lo que significa que el VARTYPE en el que se estableció previamente ya no restringe las operaciones de **adición** .</span><span class="sxs-lookup"><span data-stu-id="ad2da-118">After calling **Clear**, the collection is considered type-less, meaning that the VARTYPE it was previously set to is no longer restricting **Add** operations.</span></span> <span data-ttu-id="ad2da-119">Una llamada a **Add** después de llamar a **Clear** se considera la **suma** "First" para esta colección.</span><span class="sxs-lookup"><span data-stu-id="ad2da-119">A call to **Add** after calling **Clear** is considered the "first" **Add** for this collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad2da-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad2da-120">Requirements</span></span>



| <span data-ttu-id="ad2da-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad2da-121">Requirement</span></span> | <span data-ttu-id="ad2da-122">Value</span><span class="sxs-lookup"><span data-stu-id="ad2da-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad2da-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad2da-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ad2da-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad2da-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad2da-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad2da-125">Library</span></span><br/> | <dl> <span data-ttu-id="ad2da-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad2da-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad2da-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad2da-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad2da-128">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="ad2da-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




