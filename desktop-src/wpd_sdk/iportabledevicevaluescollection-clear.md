---
description: El método Clear libera todos los elementos de la colección.
ms.assetid: 151d1f61-11f0-40f0-8da1-79e9eb2001ce
title: 'IPortableDeviceValuesCollection:: CLEAR (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bf826b8e8a2035a0d84aec76979616fcccee9948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698566"
---
# <a name="iportabledevicevaluescollectionclear-method"></a><span data-ttu-id="9073c-103">IPortableDeviceValuesCollection:: CLEAR (método)</span><span class="sxs-lookup"><span data-stu-id="9073c-103">IPortableDeviceValuesCollection::Clear method</span></span>

<span data-ttu-id="9073c-104">El método **Clear** libera todos los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="9073c-104">The **Clear** method releases all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9073c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9073c-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="9073c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9073c-106">Parameters</span></span>

<span data-ttu-id="9073c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9073c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9073c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9073c-108">Return value</span></span>

<span data-ttu-id="9073c-109">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9073c-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9073c-110">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="9073c-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9073c-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9073c-111">Return code</span></span>                                                                          | <span data-ttu-id="9073c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9073c-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9073c-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9073c-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9073c-114">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="9073c-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9073c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9073c-115">Remarks</span></span>

<span data-ttu-id="9073c-116">El método libera toda la memoria asignada a los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="9073c-116">The method releases all memory that is allocated for the items in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="9073c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9073c-117">Requirements</span></span>



| <span data-ttu-id="9073c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9073c-118">Requirement</span></span> | <span data-ttu-id="9073c-119">Value</span><span class="sxs-lookup"><span data-stu-id="9073c-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9073c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9073c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9073c-121"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9073c-121"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9073c-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9073c-122">Library</span></span><br/> | <dl> <span data-ttu-id="9073c-123"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9073c-123"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9073c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9073c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9073c-125">**Interfaz IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="9073c-125">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




