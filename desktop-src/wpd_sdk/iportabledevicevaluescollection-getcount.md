---
description: El método GetCount recupera el número de elementos de la colección.
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: 'IPortableDeviceValuesCollection:: GetCount (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5d1eabdcf73d65b42ccff980b15bb15514c3b322
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718629"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a><span data-ttu-id="dd564-103">IPortableDeviceValuesCollection:: GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="dd564-103">IPortableDeviceValuesCollection::GetCount method</span></span>

<span data-ttu-id="dd564-104">El método **getCount** recupera el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="dd564-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd564-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd564-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="dd564-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd564-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd564-107">*pcElems* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd564-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd564-108">Puntero a un **valor DWORD** que contiene el número de interfaces **IPortableDeviceValues** de la colección.</span><span class="sxs-lookup"><span data-stu-id="dd564-108">Pointer to a **DWORD** that contains the number of **IPortableDeviceValues** interfaces in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd564-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd564-109">Return value</span></span>

<span data-ttu-id="dd564-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dd564-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dd564-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="dd564-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dd564-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dd564-112">Return code</span></span>                                                                               | <span data-ttu-id="dd564-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd564-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="dd564-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="dd564-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="dd564-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="dd564-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="dd564-116"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="dd564-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="dd564-117">Un argumento de puntero necesario era **null**.</span><span class="sxs-lookup"><span data-stu-id="dd564-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dd564-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd564-118">Requirements</span></span>



| <span data-ttu-id="dd564-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd564-119">Requirement</span></span> | <span data-ttu-id="dd564-120">Value</span><span class="sxs-lookup"><span data-stu-id="dd564-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd564-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd564-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dd564-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd564-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd564-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd564-123">Library</span></span><br/> | <dl> <span data-ttu-id="dd564-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd564-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd564-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd564-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd564-126">**Interfaz IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="dd564-126">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




