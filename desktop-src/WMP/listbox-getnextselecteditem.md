---
title: LISTBOX. getNextSelectedItem
description: El método getNextSelectedItem recupera el siguiente elemento seleccionado en el control de cuadro de lista a partir del elemento situado después del objeto con el índice especificado.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- LISTBOX. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699632"
---
# <a name="listboxgetnextselecteditem"></a><span data-ttu-id="764c4-104">LISTBOX. getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="764c4-104">LISTBOX.getNextSelectedItem</span></span>

<span data-ttu-id="764c4-105">El método **getNextSelectedItem** recupera el siguiente elemento seleccionado en el control de cuadro de lista a partir del elemento situado después del objeto con el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="764c4-105">The **getNextSelectedItem** method retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a><span data-ttu-id="764c4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="764c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="764c4-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Super*</span><span class="sxs-lookup"><span data-stu-id="764c4-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="764c4-108">**Número** (**largo**) que contiene el índice del elemento que precede al elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="764c4-108">**Number** (**long**) containing the index of the item that precedes the item being retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="764c4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="764c4-109">Return Value</span></span>

<span data-ttu-id="764c4-110">Este método devuelve un **número** (**largo**) que contiene el índice del siguiente elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="764c4-110">This method returns a **Number** (**long**) containing the index of the next selected item.</span></span>

## <a name="remarks"></a><span data-ttu-id="764c4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="764c4-111">Remarks</span></span>

<span data-ttu-id="764c4-112">Para iniciar la búsqueda desde el principio, use 1 para el índice de inicio.</span><span class="sxs-lookup"><span data-stu-id="764c4-112">To start search from the beginning, use  1 for the start index.</span></span>

## <a name="requirements"></a><span data-ttu-id="764c4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="764c4-113">Requirements</span></span>



| <span data-ttu-id="764c4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="764c4-114">Requirement</span></span> | <span data-ttu-id="764c4-115">Value</span><span class="sxs-lookup"><span data-stu-id="764c4-115">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="764c4-116">Versión</span><span class="sxs-lookup"><span data-stu-id="764c4-116">Version</span></span><br/> | <span data-ttu-id="764c4-117">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="764c4-117">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="764c4-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="764c4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="764c4-119">**Elemento LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="764c4-119">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





