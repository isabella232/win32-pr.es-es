---
title: EDITBOX. getSelectionEnd
description: El método getSelectionEnd recupera la posición final del texto seleccionado en el control EditBox.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- GetSelectionEnd Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700410"
---
# <a name="editboxgetselectionend"></a><span data-ttu-id="fe3b2-104">EDITBOX. getSelectionEnd</span><span class="sxs-lookup"><span data-stu-id="fe3b2-104">EDITBOX.getSelectionEnd</span></span>

<span data-ttu-id="fe3b2-105">El método **getSelectionEnd** recupera la posición final del texto seleccionado en el control EditBox.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-105">The **getSelectionEnd** method retrieves the ending position of the selected text in the editbox control.</span></span>

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a><span data-ttu-id="fe3b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe3b2-106">Parameters</span></span>

<span data-ttu-id="fe3b2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe3b2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe3b2-108">Return Value</span></span>

<span data-ttu-id="fe3b2-109">Este método devuelve un **número** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="fe3b2-109">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe3b2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe3b2-110">Remarks</span></span>

<span data-ttu-id="fe3b2-111">Si no hay texto seleccionado, este método devuelve la posición del punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-111">If no text is selected, this method returns the position of the insertion point.</span></span>

<span data-ttu-id="fe3b2-112">Si el control es multilínea, este método devuelve el índice de carácter del control, no el índice de línea.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-112">If the control is multiline, this method returns the character index in the control, not the line index.</span></span>

<span data-ttu-id="fe3b2-113">Solo se puede llamar a este método después de que el control se vuelva visible.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe3b2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe3b2-114">Requirements</span></span>



| <span data-ttu-id="fe3b2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe3b2-115">Requirement</span></span> | <span data-ttu-id="fe3b2-116">Value</span><span class="sxs-lookup"><span data-stu-id="fe3b2-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="fe3b2-117">Versión</span><span class="sxs-lookup"><span data-stu-id="fe3b2-117">Version</span></span><br/> | <span data-ttu-id="fe3b2-118">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="fe3b2-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe3b2-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe3b2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3b2-120">**Elemento EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="fe3b2-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="fe3b2-121">**EDITBOX. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="fe3b2-121">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="fe3b2-122">**EDITBOX. replaceSelection**</span><span class="sxs-lookup"><span data-stu-id="fe3b2-122">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> <dt>

[<span data-ttu-id="fe3b2-123">**EDITBOX. setSelection**</span><span class="sxs-lookup"><span data-stu-id="fe3b2-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





