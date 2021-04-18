---
description: El método CopyValuesFromPropertyStore copia el contenido de un IPropertyStore en la colección.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'IPortableDeviceValues:: CopyValuesFromPropertyStore (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718901"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a><span data-ttu-id="962c0-103">IPortableDeviceValues:: CopyValuesFromPropertyStore (método)</span><span class="sxs-lookup"><span data-stu-id="962c0-103">IPortableDeviceValues::CopyValuesFromPropertyStore method</span></span>

<span data-ttu-id="962c0-104">El método **CopyValuesFromPropertyStore** copia el contenido de un **IPropertyStore** en la colección.</span><span class="sxs-lookup"><span data-stu-id="962c0-104">The **CopyValuesFromPropertyStore** method copies the contents of an **IPropertyStore** into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="962c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="962c0-105">Syntax</span></span>


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="962c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="962c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="962c0-107">*pStore* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="962c0-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="962c0-108">Puntero a un **IPropertyStore** que se va a copiar en la colección.</span><span class="sxs-lookup"><span data-stu-id="962c0-108">Pointer to an **IPropertyStore** to copy into the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="962c0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="962c0-109">Return value</span></span>

<span data-ttu-id="962c0-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="962c0-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="962c0-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="962c0-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="962c0-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="962c0-112">Return code</span></span>                                                                          | <span data-ttu-id="962c0-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="962c0-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="962c0-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="962c0-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="962c0-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="962c0-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="962c0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="962c0-116">Remarks</span></span>

<span data-ttu-id="962c0-117">Este método convierte automáticamente todos los **valores \_ BSTR de VT** en valores de **VT \_ LPWStr** .</span><span class="sxs-lookup"><span data-stu-id="962c0-117">This method automatically converts all **VT\_BSTR** values to **VT\_LPWSTR** values.</span></span>

<span data-ttu-id="962c0-118">Muchas aplicaciones o componentes externos que se comunican con la aplicación, como algunas aplicaciones de Shell, utilizan la interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="962c0-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="962c0-119">Este método proporciona una manera rápida y sencilla de intercambiar datos con estos programas.</span><span class="sxs-lookup"><span data-stu-id="962c0-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="962c0-120">Este método es compatible con Windows Vista y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="962c0-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="962c0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="962c0-121">Requirements</span></span>



| <span data-ttu-id="962c0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="962c0-122">Requirement</span></span> | <span data-ttu-id="962c0-123">Value</span><span class="sxs-lookup"><span data-stu-id="962c0-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="962c0-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="962c0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="962c0-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="962c0-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="962c0-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="962c0-126">Library</span></span><br/> | <dl> <span data-ttu-id="962c0-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="962c0-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="962c0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="962c0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="962c0-129">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="962c0-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="962c0-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="962c0-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span></span>](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




