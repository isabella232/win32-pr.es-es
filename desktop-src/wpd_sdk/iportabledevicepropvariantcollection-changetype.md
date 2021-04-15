---
description: El método ChangeType convierte todos los elementos de la colección en el VARTYPE especificado.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'IPortableDevicePropVariantCollection:: ChangeType (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d843b62d273b28f7a694c37358742e4f3365be21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708994"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a><span data-ttu-id="2f895-103">IPortableDevicePropVariantCollection:: ChangeType (método)</span><span class="sxs-lookup"><span data-stu-id="2f895-103">IPortableDevicePropVariantCollection::ChangeType method</span></span>

<span data-ttu-id="2f895-104">El método **ChangeType** convierte todos los elementos de la colección en el VARTYPE especificado.</span><span class="sxs-lookup"><span data-stu-id="2f895-104">The **ChangeType** method converts all items in the collection to the specified VARTYPE.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f895-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f895-105">Syntax</span></span>


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a><span data-ttu-id="2f895-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f895-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f895-107">*VT* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f895-107">*vt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f895-108">Especifica el **VARTYPE** en el que desea convertir todos los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="2f895-108">Specifies the **VARTYPE** to which you want to convert all items in the collection.</span></span> <span data-ttu-id="2f895-109">Los tipos de ejemplo incluyen VT \_ UI4 y VT \_ UI8.</span><span class="sxs-lookup"><span data-stu-id="2f895-109">Example types include VT\_UI4 and VT\_UI8.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f895-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f895-110">Return value</span></span>

<span data-ttu-id="2f895-111">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2f895-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2f895-112">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="2f895-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2f895-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2f895-113">Return code</span></span>                                                                          | <span data-ttu-id="2f895-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f895-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2f895-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2f895-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2f895-116">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="2f895-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f895-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f895-117">Remarks</span></span>

<span data-ttu-id="2f895-118">Si se produce un error en este método, la colección puede quedar en un estado intermedio, con algunos miembros convertidos y otros no convertidos.</span><span class="sxs-lookup"><span data-stu-id="2f895-118">If this method fails, the collection may be left in an intermediate state, with some members converted and some not converted.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f895-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f895-119">Requirements</span></span>



| <span data-ttu-id="2f895-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f895-120">Requirement</span></span> | <span data-ttu-id="2f895-121">Value</span><span class="sxs-lookup"><span data-stu-id="2f895-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f895-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f895-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2f895-123"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f895-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f895-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f895-124">Library</span></span><br/> | <dl> <span data-ttu-id="2f895-125"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f895-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f895-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f895-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f895-127">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="2f895-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




