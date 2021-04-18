---
description: La interfaz IPortableDevicePropVariantCollection contiene una colección de valores PROPVARIANT indizados del mismo VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Interfaz IPortableDevicePropVariantCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718723"
---
# <a name="iportabledevicepropvariantcollection-interface"></a><span data-ttu-id="cdee5-103">Interfaz IPortableDevicePropVariantCollection</span><span class="sxs-lookup"><span data-stu-id="cdee5-103">IPortableDevicePropVariantCollection interface</span></span>

<span data-ttu-id="cdee5-104">La interfaz **IPortableDevicePropVariantCollection** contiene una colección de valores **PROPVARIANT** indizados del mismo VARTYPE.</span><span class="sxs-lookup"><span data-stu-id="cdee5-104">The **IPortableDevicePropVariantCollection** interface holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="cdee5-105">El VARTYPE del primer elemento que se agrega a la colección determina el VARTYPE de la colección.</span><span class="sxs-lookup"><span data-stu-id="cdee5-105">The VARTYPE of the first item that is added to the collection determines the VARTYPE of the collection.</span></span> <span data-ttu-id="cdee5-106">Se puede producir un error al intentar agregar un elemento de un VARTYPE diferente si el valor de **PROPVARIANT** no se puede cambiar al VARTYPE actual de la colección.</span><span class="sxs-lookup"><span data-stu-id="cdee5-106">An attempt to add an item of a different VARTYPE may fail if the **PROPVARIANT** value cannot be changed to the collection's current VARTYPE.</span></span> <span data-ttu-id="cdee5-107">Para cambiar el VARTYPE de la colección, llame a **ChangeType**.</span><span class="sxs-lookup"><span data-stu-id="cdee5-107">To change the VARTYPE of the collection, call **ChangeType**.</span></span>

<span data-ttu-id="cdee5-108">Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamar a **CoCreate** con **CLSID \_ PortableDevicePropVariantCollection**.</span><span class="sxs-lookup"><span data-stu-id="cdee5-108">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDevicePropVariantCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="cdee5-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cdee5-109">Members</span></span>

<span data-ttu-id="cdee5-110">La interfaz **IPortableDevicePropVariantCollection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cdee5-110">The **IPortableDevicePropVariantCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cdee5-111">**IPortableDevicePropVariantCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cdee5-111">**IPortableDevicePropVariantCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="cdee5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="cdee5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cdee5-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="cdee5-113">Methods</span></span>

<span data-ttu-id="cdee5-114">La interfaz **IPortableDevicePropVariantCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cdee5-114">The **IPortableDevicePropVariantCollection** interface has these methods.</span></span>



| <span data-ttu-id="cdee5-115">Método</span><span class="sxs-lookup"><span data-stu-id="cdee5-115">Method</span></span>                                                                | <span data-ttu-id="cdee5-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdee5-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdee5-117">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="cdee5-117">**Add**</span></span>](iportabledevicepropvariantcollection-add.md)               | <span data-ttu-id="cdee5-118">Agrega un elemento a la colección.</span><span class="sxs-lookup"><span data-stu-id="cdee5-118">Adds an item to the collection.</span></span><br/>                                          |
| [<span data-ttu-id="cdee5-119">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="cdee5-119">**ChangeType**</span></span>](iportabledevicepropvariantcollection-changetype.md) | <span data-ttu-id="cdee5-120">Convierte todos los elementos de la colección en el VARTYPE especificado.</span><span class="sxs-lookup"><span data-stu-id="cdee5-120">Converts all items in the collection to the specified VARTYPE.</span></span><br/>           |
| [<span data-ttu-id="cdee5-121">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="cdee5-121">**Clear**</span></span>](iportabledevicepropvariantcollection-clear.md)           | <span data-ttu-id="cdee5-122">Libera y, a continuación, quita todos los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="cdee5-122">Frees, and then removes, all items from the collection.</span></span><br/>                  |
| [<span data-ttu-id="cdee5-123">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="cdee5-123">**GetAt**</span></span>](iportabledevicepropvariantcollection-getat.md)           | <span data-ttu-id="cdee5-124">Recupera un elemento de la colección mediante un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="cdee5-124">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="cdee5-125">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="cdee5-125">**GetCount**</span></span>](iportabledevicepropvariantcollection-getcount.md)     | <span data-ttu-id="cdee5-126">Recupera el número de elementos de esta colección.</span><span class="sxs-lookup"><span data-stu-id="cdee5-126">Retrieves the number of items in this collection.</span></span><br/>                        |
| [<span data-ttu-id="cdee5-127">**GetType**</span><span class="sxs-lookup"><span data-stu-id="cdee5-127">**GetType**</span></span>](iportabledevicepropvariantcollection-gettype.md)       | <span data-ttu-id="cdee5-128">Recupera el tipo de datos de los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="cdee5-128">Retrieves the data type of the items in the collection.</span></span><br/>                  |
| [<span data-ttu-id="cdee5-129">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="cdee5-129">**RemoveAt**</span></span>](iportabledevicepropvariantcollection-removeat.md)     | <span data-ttu-id="cdee5-130">Quita el elemento almacenado en la ubicación especificada por el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="cdee5-130">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cdee5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdee5-131">Requirements</span></span>



| <span data-ttu-id="cdee5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdee5-132">Requirement</span></span> | <span data-ttu-id="cdee5-133">Value</span><span class="sxs-lookup"><span data-stu-id="cdee5-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdee5-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdee5-134">Header</span></span><br/>  | <dl> <span data-ttu-id="cdee5-135"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdee5-135"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="cdee5-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cdee5-136">Library</span></span><br/> | <dl> <span data-ttu-id="cdee5-137"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdee5-137"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdee5-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdee5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdee5-139">**Interfaces de colección**</span><span class="sxs-lookup"><span data-stu-id="cdee5-139">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

