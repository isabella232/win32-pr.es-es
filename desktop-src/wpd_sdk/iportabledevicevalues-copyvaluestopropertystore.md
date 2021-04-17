---
description: El método CopyValuesToPropertyStore copia todos los valores de una colección en una interfaz IPropertyStore.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'IPortableDeviceValues:: CopyValuesToPropertyStore (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709042"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a><span data-ttu-id="67d78-103">IPortableDeviceValues:: CopyValuesToPropertyStore (método)</span><span class="sxs-lookup"><span data-stu-id="67d78-103">IPortableDeviceValues::CopyValuesToPropertyStore method</span></span>

<span data-ttu-id="67d78-104">El método **CopyValuesToPropertyStore** copia todos los valores de una colección en una interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="67d78-104">The **CopyValuesToPropertyStore** method copies all the values from a collection into an **IPropertyStore** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="67d78-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67d78-105">Syntax</span></span>


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="67d78-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67d78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67d78-107">*pStore* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67d78-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67d78-108">Puntero a un objeto de almacén.</span><span class="sxs-lookup"><span data-stu-id="67d78-108">Pointer to a store object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67d78-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67d78-109">Return value</span></span>

<span data-ttu-id="67d78-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="67d78-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="67d78-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="67d78-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="67d78-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="67d78-112">Return code</span></span>                                                                          | <span data-ttu-id="67d78-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="67d78-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="67d78-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="67d78-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="67d78-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="67d78-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67d78-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67d78-116">Remarks</span></span>

<span data-ttu-id="67d78-117">Este método no convierte valores de VT \_ LPWStr en VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="67d78-117">This method does not convert values of VT\_LPWSTR into VT\_BSTR.</span></span> <span data-ttu-id="67d78-118">Muchas aplicaciones o componentes externos que se comunican con la aplicación, como algunas aplicaciones de Shell, utilizan la interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="67d78-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="67d78-119">Este método proporciona una manera rápida y sencilla de intercambiar datos con estos programas.</span><span class="sxs-lookup"><span data-stu-id="67d78-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="67d78-120">Este método es compatible con Windows Vista y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="67d78-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="67d78-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67d78-121">Requirements</span></span>



| <span data-ttu-id="67d78-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="67d78-122">Requirement</span></span> | <span data-ttu-id="67d78-123">Value</span><span class="sxs-lookup"><span data-stu-id="67d78-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67d78-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67d78-124">Header</span></span><br/>  | <dl> <span data-ttu-id="67d78-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="67d78-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="67d78-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67d78-126">Library</span></span><br/> | <dl> <span data-ttu-id="67d78-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67d78-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67d78-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="67d78-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67d78-129">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="67d78-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="67d78-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="67d78-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span></span>](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




