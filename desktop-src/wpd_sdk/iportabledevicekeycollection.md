---
description: La interfaz IPortableDeviceKeyCollection contiene una colección de valores PROPERTYKEY. Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamar a CoCreate con CLSID \_ PortableDeviceKeyCollection.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Interfaz IPortableDeviceKeyCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708996"
---
# <a name="iportabledevicekeycollection-interface"></a><span data-ttu-id="1ea50-104">Interfaz IPortableDeviceKeyCollection</span><span class="sxs-lookup"><span data-stu-id="1ea50-104">IPortableDeviceKeyCollection interface</span></span>

<span data-ttu-id="1ea50-105">La interfaz **IPortableDeviceKeyCollection** contiene una colección de valores **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="1ea50-105">The **IPortableDeviceKeyCollection** interface holds a collection of **PROPERTYKEY** values.</span></span> <span data-ttu-id="1ea50-106">Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamar a **CoCreate** con **CLSID \_ PortableDeviceKeyCollection**.</span><span class="sxs-lookup"><span data-stu-id="1ea50-106">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceKeyCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="1ea50-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1ea50-107">Members</span></span>

<span data-ttu-id="1ea50-108">La interfaz **IPortableDeviceKeyCollection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1ea50-108">The **IPortableDeviceKeyCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1ea50-109">**IPortableDeviceKeyCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1ea50-109">**IPortableDeviceKeyCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="1ea50-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1ea50-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1ea50-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1ea50-111">Methods</span></span>

<span data-ttu-id="1ea50-112">La interfaz **IPortableDeviceKeyCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1ea50-112">The **IPortableDeviceKeyCollection** interface has these methods.</span></span>



| <span data-ttu-id="1ea50-113">Método</span><span class="sxs-lookup"><span data-stu-id="1ea50-113">Method</span></span>                                                    | <span data-ttu-id="1ea50-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ea50-114">Description</span></span>                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ea50-115">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="1ea50-115">**Add**</span></span>](iportabledevicekeycollection-add.md)           | <span data-ttu-id="1ea50-116">Agrega una clave de propiedad a la colección.</span><span class="sxs-lookup"><span data-stu-id="1ea50-116">Adds a property key to the collection.</span></span><br/>                                   |
| [<span data-ttu-id="1ea50-117">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="1ea50-117">**Clear**</span></span>](iportabledevicekeycollection-clear.md)       | <span data-ttu-id="1ea50-118">Elimina todos los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="1ea50-118">Deletes all items from the collection.</span></span><br/>                                   |
| [<span data-ttu-id="1ea50-119">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="1ea50-119">**GetAt**</span></span>](iportabledevicekeycollection-getat.md)       | <span data-ttu-id="1ea50-120">Recupera un **PROPERTYKEY** de la colección por índice.</span><span class="sxs-lookup"><span data-stu-id="1ea50-120">Retrieves a **PROPERTYKEY** from the collection by index.</span></span><br/>                |
| [<span data-ttu-id="1ea50-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="1ea50-121">**GetCount**</span></span>](iportabledevicekeycollection-getcount.md) | <span data-ttu-id="1ea50-122">Recupera el número de claves de esta colección.</span><span class="sxs-lookup"><span data-stu-id="1ea50-122">Retrieves the number of keys in this collection.</span></span><br/>                         |
| [<span data-ttu-id="1ea50-123">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="1ea50-123">**RemoveAt**</span></span>](iportabledevicekeycollection-removeat.md) | <span data-ttu-id="1ea50-124">Quita el elemento almacenado en la ubicación especificada por el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="1ea50-124">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1ea50-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ea50-125">Requirements</span></span>



| <span data-ttu-id="1ea50-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ea50-126">Requirement</span></span> | <span data-ttu-id="1ea50-127">Value</span><span class="sxs-lookup"><span data-stu-id="1ea50-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea50-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ea50-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1ea50-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ea50-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ea50-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ea50-130">Library</span></span><br/> | <dl> <span data-ttu-id="1ea50-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ea50-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ea50-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ea50-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ea50-133">**Interfaces de colección**</span><span class="sxs-lookup"><span data-stu-id="1ea50-133">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

