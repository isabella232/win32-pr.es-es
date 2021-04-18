---
title: EDITBOX. getLineIndex
description: El método getLineIndex recupera el índice de carácter del primer carácter de la línea con el índice de línea especificado.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- GetLineIndex Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700412"
---
# <a name="editboxgetlineindex"></a><span data-ttu-id="e886d-104">EDITBOX. getLineIndex</span><span class="sxs-lookup"><span data-stu-id="e886d-104">EDITBOX.getLineIndex</span></span>

<span data-ttu-id="e886d-105">El método **getLineIndex** recupera el índice de carácter del primer carácter de la línea con el índice de línea especificado.</span><span class="sxs-lookup"><span data-stu-id="e886d-105">The **getLineIndex** method retrieves the character index of the first character on the line with the specified line index.</span></span>

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a><span data-ttu-id="e886d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e886d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e886d-107"><span id="index"></span><span id="INDEX"></span>*ajustar*</span><span class="sxs-lookup"><span data-stu-id="e886d-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="e886d-108">**Número** (**largo**) que contiene el índice de la línea cuyo índice de caracteres se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="e886d-108">**Number** (**long**) containing the index of the line whose character index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e886d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e886d-109">Return Value</span></span>

<span data-ttu-id="e886d-110">Este método devuelve un **número** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="e886d-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e886d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e886d-111">Remarks</span></span>

<span data-ttu-id="e886d-112">Si el índice de línea especificado es 1, se usa la línea que contiene el punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="e886d-112">If the specified line index is  1, the line containing the insertion point is used.</span></span>

<span data-ttu-id="e886d-113">Solo se puede llamar a este método después de que el control se vuelva visible.</span><span class="sxs-lookup"><span data-stu-id="e886d-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="e886d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e886d-114">Requirements</span></span>



| <span data-ttu-id="e886d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e886d-115">Requirement</span></span> | <span data-ttu-id="e886d-116">Value</span><span class="sxs-lookup"><span data-stu-id="e886d-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="e886d-117">Versión</span><span class="sxs-lookup"><span data-stu-id="e886d-117">Version</span></span><br/> | <span data-ttu-id="e886d-118">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="e886d-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e886d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e886d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e886d-120">**Elemento EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="e886d-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="e886d-121">**EDITBOX. getLine**</span><span class="sxs-lookup"><span data-stu-id="e886d-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="e886d-122">**EDITBOX. getLineFromChar**</span><span class="sxs-lookup"><span data-stu-id="e886d-122">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> </dl>

 

 





