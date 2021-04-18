---
title: EDITBOX. getLineFromChar
description: El método getLineFromChar recupera el índice de línea para el índice de carácter especificado.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- GetLineFromChar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700411"
---
# <a name="editboxgetlinefromchar"></a><span data-ttu-id="4c833-104">EDITBOX. getLineFromChar</span><span class="sxs-lookup"><span data-stu-id="4c833-104">EDITBOX.getLineFromChar</span></span>

<span data-ttu-id="4c833-105">El método **getLineFromChar** recupera el índice de línea para el índice de carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="4c833-105">The **getLineFromChar** method retrieves the line index for the specified character index.</span></span>

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a><span data-ttu-id="4c833-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c833-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c833-107"><span id="index"></span><span id="INDEX"></span>*ajustar*</span><span class="sxs-lookup"><span data-stu-id="4c833-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="4c833-108">**Número** (**largo**) que contiene el índice del carácter cuyo índice de línea se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="4c833-108">**Number** (**long**) containing the index of the character whose line index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c833-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c833-109">Return Value</span></span>

<span data-ttu-id="4c833-110">Este método devuelve un **número** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="4c833-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c833-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c833-111">Remarks</span></span>

<span data-ttu-id="4c833-112">Si la posición de carácter especificada es 1, este método recupera el índice de línea de la línea actual.</span><span class="sxs-lookup"><span data-stu-id="4c833-112">If the specified character position is  1, this method retrieves the line index of the current line.</span></span>

<span data-ttu-id="4c833-113">Solo se puede llamar a este método después de que el control se vuelva visible.</span><span class="sxs-lookup"><span data-stu-id="4c833-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c833-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c833-114">Requirements</span></span>



| <span data-ttu-id="4c833-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c833-115">Requirement</span></span> | <span data-ttu-id="4c833-116">Value</span><span class="sxs-lookup"><span data-stu-id="4c833-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="4c833-117">Versión</span><span class="sxs-lookup"><span data-stu-id="4c833-117">Version</span></span><br/> | <span data-ttu-id="4c833-118">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="4c833-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c833-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c833-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c833-120">**Elemento EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="4c833-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="4c833-121">**EDITBOX. getLine**</span><span class="sxs-lookup"><span data-stu-id="4c833-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="4c833-122">**EDITBOX. getLineIndex**</span><span class="sxs-lookup"><span data-stu-id="4c833-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





