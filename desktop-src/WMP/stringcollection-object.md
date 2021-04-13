---
title: StringCollection (objeto)
description: El objeto StringCollection proporciona una manera de manipular una colección de cadenas.
ms.assetid: bd4f82e7-1a6a-47c5-b019-7aff520e621a
keywords:
- Objeto StringCollection Media Player de Windows
topic_type:
- apiref
api_name:
- StringCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d1872bec7e00e87ada845f7518608ea4149f137
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104358343"
---
# <a name="stringcollection-object"></a><span data-ttu-id="ae22f-104">StringCollection (objeto)</span><span class="sxs-lookup"><span data-stu-id="ae22f-104">StringCollection Object</span></span>

<span data-ttu-id="ae22f-105">El objeto **StringCollection** proporciona una manera de manipular una colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="ae22f-105">The **StringCollection** object provides a way to manipulate a collection of strings.</span></span>

<span data-ttu-id="ae22f-106">El objeto **StringCollection** admite la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="ae22f-106">The **StringCollection** object supports the following property.</span></span>



| <span data-ttu-id="ae22f-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ae22f-107">Property</span></span>                            | <span data-ttu-id="ae22f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae22f-108">Description</span></span>                                             |
|-------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="ae22f-109">count</span><span class="sxs-lookup"><span data-stu-id="ae22f-109">count</span></span>](stringcollection-count.md) | <span data-ttu-id="ae22f-110">Recupera el número de elementos de la colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="ae22f-110">Retrieves the number of items in the string collection.</span></span> |



 

<span data-ttu-id="ae22f-111">El objeto **StringCollection** admite los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ae22f-111">The **StringCollection** object supports the following methods.</span></span>



| <span data-ttu-id="ae22f-112">Método</span><span class="sxs-lookup"><span data-stu-id="ae22f-112">Method</span></span>                                                                  | <span data-ttu-id="ae22f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae22f-113">Description</span></span>                                                                                                                     |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae22f-114">getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="ae22f-114">getAttributeCountByType</span></span>](stringcollection-getattributecountbytype.md) | <span data-ttu-id="ae22f-115">Recupera el número de atributos asociados con el índice del elemento **StringCollection** , el nombre de atributo y el idioma especificados.</span><span class="sxs-lookup"><span data-stu-id="ae22f-115">Retrieves the number of attributes associated with the specified **StringCollection** item index, attribute name, and language.</span></span> |
| [<span data-ttu-id="ae22f-116">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="ae22f-116">getItemInfo</span></span>](stringcollection-getiteminfo.md)                         | <span data-ttu-id="ae22f-117">Recupera la cadena correspondiente al índice y el nombre del elemento **StringCollection** especificado.</span><span class="sxs-lookup"><span data-stu-id="ae22f-117">Retrieves the string corresponding to the specified **StringCollection** item index and name.</span></span>                                   |
| [<span data-ttu-id="ae22f-118">getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="ae22f-118">getItemInfoByType</span></span>](stringcollection-getiteminfobytype.md)             | <span data-ttu-id="ae22f-119">Recupera la cadena correspondiente al índice del elemento **StringCollection** , el nombre, el idioma y el índice de atributo especificados.</span><span class="sxs-lookup"><span data-stu-id="ae22f-119">Retrieves the string corresponding to the specified **StringCollection** item index, name, language, and attribute index.</span></span>       |
| [<span data-ttu-id="ae22f-120">isIdentical</span><span class="sxs-lookup"><span data-stu-id="ae22f-120">isIdentical</span></span>](stringcollection-isidentical.md)                         | <span data-ttu-id="ae22f-121">Recupera un valor que indica si el objeto proporcionado es igual que el actual.</span><span class="sxs-lookup"><span data-stu-id="ae22f-121">Retrieves a value indicating whether the supplied object is the same as the current one.</span></span>                                        |
| [<span data-ttu-id="ae22f-122">item</span><span class="sxs-lookup"><span data-stu-id="ae22f-122">item</span></span>](stringcollection-item.md)                                       | <span data-ttu-id="ae22f-123">Recupera la cadena en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="ae22f-123">Retrieves the string at the specified index.</span></span>                                                                                    |



 

<span data-ttu-id="ae22f-124">Se tiene acceso al objeto **StringCollection** mediante el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="ae22f-124">The **StringCollection** object is accessed through the following method.</span></span>



| <span data-ttu-id="ae22f-125">Object</span><span class="sxs-lookup"><span data-stu-id="ae22f-125">Object</span></span>                                        | <span data-ttu-id="ae22f-126">Método</span><span class="sxs-lookup"><span data-stu-id="ae22f-126">Method</span></span>                                                                           |
|-----------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="ae22f-127">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="ae22f-127">MediaCollection</span></span>](mediacollection-object.md) | [<span data-ttu-id="ae22f-128">getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="ae22f-128">getAttributeStringCollection</span></span>](mediacollection-getattributestringcollection.md) |



 

<span data-ttu-id="ae22f-129">Para fines de Ilustración, *reproductor*. *mediaCollection*. **getAttributeStringCollection**(*Attribute*, *mediaType*) se usa en las secciones de sintaxis de referencia.</span><span class="sxs-lookup"><span data-stu-id="ae22f-129">For purposes of illustration, *player*.*mediaCollection*.**getAttributeStringCollection**(*attribute*, *mediaType*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae22f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae22f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae22f-131">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="ae22f-131">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




