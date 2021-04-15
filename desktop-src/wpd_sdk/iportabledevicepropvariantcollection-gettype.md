---
description: El método GetType recupera el tipo de datos de los elementos de la colección.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'IPortableDevicePropVariantCollection:: GetType (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690150"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a><span data-ttu-id="50432-103">IPortableDevicePropVariantCollection:: GetType (método)</span><span class="sxs-lookup"><span data-stu-id="50432-103">IPortableDevicePropVariantCollection::GetType method</span></span>

<span data-ttu-id="50432-104">El método **GetType** recupera el tipo de datos de los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="50432-104">The **GetType** method retrieves the data type of the items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="50432-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50432-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a><span data-ttu-id="50432-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50432-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50432-107">*Pvt* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="50432-107">*pvt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50432-108">Un valor de enumeración **VARTYPE** del SDK de plataforma que indica el tipo de datos de todos los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="50432-108">A Platform SDK **VARTYPE** enumeration value that indicates the data type of all the items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50432-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50432-109">Return value</span></span>

<span data-ttu-id="50432-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="50432-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="50432-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="50432-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="50432-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="50432-112">Return code</span></span>                                                                               | <span data-ttu-id="50432-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="50432-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="50432-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="50432-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="50432-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="50432-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="50432-116"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="50432-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="50432-117">Un argumento de puntero necesario era **null**.</span><span class="sxs-lookup"><span data-stu-id="50432-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="50432-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50432-118">Remarks</span></span>

<span data-ttu-id="50432-119">Todos los elementos que se almacenan en un **IPortableDevicePropVariantCollection** son del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="50432-119">All items that are stored in an **IPortableDevicePropVariantCollection** are the same type.</span></span>

## <a name="requirements"></a><span data-ttu-id="50432-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50432-120">Requirements</span></span>



| <span data-ttu-id="50432-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="50432-121">Requirement</span></span> | <span data-ttu-id="50432-122">Value</span><span class="sxs-lookup"><span data-stu-id="50432-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50432-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50432-123">Header</span></span><br/>  | <dl> <span data-ttu-id="50432-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="50432-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="50432-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50432-125">Library</span></span><br/> | <dl> <span data-ttu-id="50432-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50432-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50432-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="50432-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50432-128">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="50432-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




