---
description: El método GetSerializedSize calcula el tamaño del búfer necesario para contener una interfaz serializada de IPortableDeviceValues.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'IWpdSerializer:: GetSerializedSize (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7b50f7f6158145cd71125b5e5f26649712bb065b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670385"
---
# <a name="iwpdserializergetserializedsize-method"></a><span data-ttu-id="c45f1-103">IWpdSerializer:: GetSerializedSize (método)</span><span class="sxs-lookup"><span data-stu-id="c45f1-103">IWpdSerializer::GetSerializedSize method</span></span>

<span data-ttu-id="c45f1-104">El método **GetSerializedSize** calcula el tamaño del búfer necesario para contener una interfaz serializada de [**IPortableDeviceValues**](iportabledevicevalues.md) .</span><span class="sxs-lookup"><span data-stu-id="c45f1-104">The **GetSerializedSize** method calculates the buffer size that is required to hold a serialized [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c45f1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c45f1-105">Syntax</span></span>


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="c45f1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c45f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c45f1-107">*pSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c45f1-107">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c45f1-108">Puntero a una interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) cuyo tamaño se desea solicitar.</span><span class="sxs-lookup"><span data-stu-id="c45f1-108">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface whose size you want to request.</span></span>

</dd> <dt>

<span data-ttu-id="c45f1-109">*pdwSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c45f1-109">*pdwSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c45f1-110">Puntero a un **valor DWORD** que indica el tamaño del búfer necesario para serializar *pSource*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c45f1-110">Pointer to a **DWORD** that indicates the buffer size that is required to serialize *pSource*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c45f1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c45f1-111">Return value</span></span>

<span data-ttu-id="c45f1-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c45f1-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c45f1-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="c45f1-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c45f1-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c45f1-114">Return code</span></span>                                                                                   | <span data-ttu-id="c45f1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c45f1-115">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c45f1-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c45f1-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c45f1-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="c45f1-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="c45f1-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="c45f1-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c45f1-119">Un argumento de puntero necesario era **null**.</span><span class="sxs-lookup"><span data-stu-id="c45f1-119">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="c45f1-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c45f1-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c45f1-121">No había suficiente memoria disponible para crear el búfer.</span><span class="sxs-lookup"><span data-stu-id="c45f1-121">There was not enough available memory to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c45f1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c45f1-122">Requirements</span></span>



| <span data-ttu-id="c45f1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c45f1-123">Requirement</span></span> | <span data-ttu-id="c45f1-124">Value</span><span class="sxs-lookup"><span data-stu-id="c45f1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c45f1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c45f1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c45f1-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c45f1-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c45f1-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c45f1-127">Library</span></span><br/> | <dl> <span data-ttu-id="c45f1-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c45f1-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c45f1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c45f1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c45f1-130">**Interfaz IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="c45f1-130">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




