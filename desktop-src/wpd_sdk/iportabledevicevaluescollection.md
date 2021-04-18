---
description: La interfaz IPortableDeviceValuesCollection contiene una colección de interfaces IPortableDeviceValues indizadas basadas en cero.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Interfaz IPortableDeviceValuesCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718628"
---
# <a name="iportabledevicevaluescollection-interface"></a><span data-ttu-id="8c562-103">Interfaz IPortableDeviceValuesCollection</span><span class="sxs-lookup"><span data-stu-id="8c562-103">IPortableDeviceValuesCollection interface</span></span>

<span data-ttu-id="8c562-104">La interfaz **IPortableDeviceValuesCollection** contiene una colección de interfaces **IPortableDeviceValues** indizadas basadas en cero.</span><span class="sxs-lookup"><span data-stu-id="8c562-104">The **IPortableDeviceValuesCollection** interface holds a collection of zero-based indexed **IPortableDeviceValues** interfaces.</span></span> <span data-ttu-id="8c562-105">Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamar a **CoCreate** con **CLSID \_ PortableDeviceValuesCollection**.</span><span class="sxs-lookup"><span data-stu-id="8c562-105">This interface can be retrieved from a method, or if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceValuesCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="8c562-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c562-106">Members</span></span>

<span data-ttu-id="8c562-107">La interfaz **IPortableDeviceValuesCollection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8c562-107">The **IPortableDeviceValuesCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8c562-108">**IPortableDeviceValuesCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8c562-108">**IPortableDeviceValuesCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="8c562-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="8c562-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8c562-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8c562-110">Methods</span></span>

<span data-ttu-id="8c562-111">La interfaz **IPortableDeviceValuesCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8c562-111">The **IPortableDeviceValuesCollection** interface has these methods.</span></span>



| <span data-ttu-id="8c562-112">Método</span><span class="sxs-lookup"><span data-stu-id="8c562-112">Method</span></span>                                                       | <span data-ttu-id="8c562-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c562-113">Description</span></span>                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c562-114">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="8c562-114">**Add**</span></span>](iportabledevicevaluescollection-add.md)           | <span data-ttu-id="8c562-115">Agrega un elemento a la colección.</span><span class="sxs-lookup"><span data-stu-id="8c562-115">Adds an item to the collection</span></span><br/>                                           |
| [<span data-ttu-id="8c562-116">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="8c562-116">**Clear**</span></span>](iportabledevicevaluescollection-clear.md)       | <span data-ttu-id="8c562-117">Libera todos los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="8c562-117">Releases all items from the collection.</span></span><br/>                                  |
| [<span data-ttu-id="8c562-118">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="8c562-118">**GetAt**</span></span>](iportabledevicevaluescollection-getat.md)       | <span data-ttu-id="8c562-119">Recupera un elemento de la colección mediante un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="8c562-119">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="8c562-120">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="8c562-120">**GetCount**</span></span>](iportabledevicevaluescollection-getcount.md) | <span data-ttu-id="8c562-121">Recupera el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="8c562-121">Retrieves the number of items in the collection.</span></span><br/>                         |
| [<span data-ttu-id="8c562-122">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="8c562-122">**RemoveAt**</span></span>](iportabledevicevaluescollection-removeat.md) | <span data-ttu-id="8c562-123">Quita el elemento almacenado en la ubicación especificada por el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="8c562-123">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8c562-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c562-124">Requirements</span></span>



| <span data-ttu-id="8c562-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c562-125">Requirement</span></span> | <span data-ttu-id="8c562-126">Value</span><span class="sxs-lookup"><span data-stu-id="8c562-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c562-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c562-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8c562-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c562-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c562-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c562-129">Library</span></span><br/> | <dl> <span data-ttu-id="8c562-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c562-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c562-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c562-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c562-132">**Interfaces de colección**</span><span class="sxs-lookup"><span data-stu-id="8c562-132">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

