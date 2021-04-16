---
title: LISTBOX. findItem
description: El método findItem busca una cadena determinada empezando por el elemento que sigue al índice de elemento especificado.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- Media Player de Windows de LISTBOX. findItem
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699646"
---
# <a name="listboxfinditem"></a><span data-ttu-id="a2260-104">LISTBOX. findItem</span><span class="sxs-lookup"><span data-stu-id="a2260-104">LISTBOX.findItem</span></span>

<span data-ttu-id="a2260-105">El método **findItem** busca una cadena determinada empezando por el elemento que sigue al índice de elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="a2260-105">The **findItem** method searches for a given string starting with the item following the specified item index.</span></span>

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a><span data-ttu-id="a2260-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2260-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2260-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Super*</span><span class="sxs-lookup"><span data-stu-id="a2260-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="a2260-108">**Número** (**largo**) que contiene el índice del elemento en el que se va a iniciar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a2260-108">**Number** (**long**) containing the index of the item at which to start the search.</span></span>

</dd> <dt>

<span data-ttu-id="a2260-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span><span class="sxs-lookup"><span data-stu-id="a2260-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span></span>
</dt> <dd>

<span data-ttu-id="a2260-110">**Cadena** que contiene el texto que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="a2260-110">**String** containing the text to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2260-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2260-111">Return Value</span></span>

<span data-ttu-id="a2260-112">Este método devuelve un **número** (**Long**) que contiene el índice del elemento que contiene la cadena.</span><span class="sxs-lookup"><span data-stu-id="a2260-112">This method returns a **Number** (**long**) containing the index of the item that contains the string.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2260-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2260-113">Remarks</span></span>

<span data-ttu-id="a2260-114">Para iniciar la búsqueda en la primera línea del control de cuadro de lista, use 1 como *startIndex*.</span><span class="sxs-lookup"><span data-stu-id="a2260-114">To start the search at the first line of the list box control, use  1 as the *startIndex*.</span></span> <span data-ttu-id="a2260-115">Para continuar buscando texto después de encontrar la primera línea, use el índice de línea devuelto como *startIndex* y la búsqueda se iniciará en la línea siguiente.</span><span class="sxs-lookup"><span data-stu-id="a2260-115">To continue to search for text after the first line is found, use the returned line index as the *startIndex*, and the search will start at the next line.</span></span> <span data-ttu-id="a2260-116">Este método buscará subcadenas y no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a2260-116">This method will search for substrings and is not case-sensitive.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2260-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2260-117">Requirements</span></span>



| <span data-ttu-id="a2260-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2260-118">Requirement</span></span> | <span data-ttu-id="a2260-119">Value</span><span class="sxs-lookup"><span data-stu-id="a2260-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="a2260-120">Versión</span><span class="sxs-lookup"><span data-stu-id="a2260-120">Version</span></span><br/> | <span data-ttu-id="a2260-121">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="a2260-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2260-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2260-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2260-123">**Elemento LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="a2260-123">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





