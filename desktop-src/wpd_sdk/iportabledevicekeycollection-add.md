---
description: El método Add agrega una clave de propiedad a la colección.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'IPortableDeviceKeyCollection:: Add (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e43fea25a08969b2ae8169884d51ddc46f8c7136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718957"
---
# <a name="iportabledevicekeycollectionadd-method"></a><span data-ttu-id="0b267-103">IPortableDeviceKeyCollection:: Add (método)</span><span class="sxs-lookup"><span data-stu-id="0b267-103">IPortableDeviceKeyCollection::Add method</span></span>

<span data-ttu-id="0b267-104">El método **Add** agrega una clave de propiedad a la colección.</span><span class="sxs-lookup"><span data-stu-id="0b267-104">The **Add** method adds a property key to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b267-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b267-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a><span data-ttu-id="0b267-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b267-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b267-107">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0b267-107">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b267-108">**REFPROPERTYKEY** que se va a agregar a la colección.</span><span class="sxs-lookup"><span data-stu-id="0b267-108">A **REFPROPERTYKEY** to add to the collection.</span></span> <span data-ttu-id="0b267-109">Este método copia la clave en la colección, por lo que puede liberar la variable local después de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="0b267-109">This method copies the key to the collection, so you can release the local variable after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b267-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b267-110">Return value</span></span>

<span data-ttu-id="0b267-111">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0b267-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0b267-112">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="0b267-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0b267-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0b267-113">Return code</span></span>                                                                                   | <span data-ttu-id="0b267-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b267-114">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b267-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0b267-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0b267-116">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="0b267-116">The method succeeded.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="0b267-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0b267-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0b267-118">No hay suficiente memoria disponible para agregar la clave a la colección.</span><span class="sxs-lookup"><span data-stu-id="0b267-118">There is not enough memory available to add the key to the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="0b267-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0b267-119">Examples</span></span>

<span data-ttu-id="0b267-120">Para obtener un ejemplo de cómo usar este método, vea [recuperar propiedades de un solo objeto](retrieving-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="0b267-120">For an example of how to use this method, see [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b267-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b267-121">Requirements</span></span>



| <span data-ttu-id="0b267-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b267-122">Requirement</span></span> | <span data-ttu-id="0b267-123">Value</span><span class="sxs-lookup"><span data-stu-id="0b267-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b267-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b267-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0b267-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b267-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b267-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b267-126">Library</span></span><br/> | <dl> <span data-ttu-id="0b267-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b267-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b267-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b267-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b267-129">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="0b267-129">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="0b267-130">Recuperación de propiedades de objetos de contenido</span><span class="sxs-lookup"><span data-stu-id="0b267-130">Retrieving Content-Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="0b267-131">Recuperación de propiedades para un solo objeto</span><span class="sxs-lookup"><span data-stu-id="0b267-131">Retrieving Properties for a Single Object</span></span>](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="0b267-132">Recuperación de las capacidades de representación admitidas por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="0b267-132">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




