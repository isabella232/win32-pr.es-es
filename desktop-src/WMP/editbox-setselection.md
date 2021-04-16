---
title: EDITBOX. setSelection
description: El método setSelection selecciona el texto del control de cuadro de edición desde el índice de inicio especificado hasta el índice final especificado.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- SetSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699390"
---
# <a name="editboxsetselection"></a><span data-ttu-id="e21f8-104">EDITBOX. setSelection</span><span class="sxs-lookup"><span data-stu-id="e21f8-104">EDITBOX.setSelection</span></span>

<span data-ttu-id="e21f8-105">El método **setSelection** selecciona el texto del control de cuadro de edición desde el índice de inicio especificado hasta el índice final especificado.</span><span class="sxs-lookup"><span data-stu-id="e21f8-105">The **setSelection** method selects the text in the edit box control from the specified start index to the specified end index.</span></span>

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a><span data-ttu-id="e21f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e21f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e21f8-107"><span id="start"></span><span id="START"></span>*iniciales*</span><span class="sxs-lookup"><span data-stu-id="e21f8-107"><span id="start"></span><span id="START"></span>*start*</span></span>
</dt> <dd>

<span data-ttu-id="e21f8-108">**Número** (**largo**) que contiene el índice de carácter de la posición inicial del texto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e21f8-108">**Number** (**long**) containing the character index of the starting position of the selected text.</span></span>

</dd> <dt>

<span data-ttu-id="e21f8-109"><span id="end"></span><span id="END"></span>*extremo*</span><span class="sxs-lookup"><span data-stu-id="e21f8-109"><span id="end"></span><span id="END"></span>*end*</span></span>
</dt> <dd>

<span data-ttu-id="e21f8-110">**Número** (**largo**) que contiene el índice de carácter de la posición final del texto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e21f8-110">**Number** (**long**) containing the character index of the ending position of the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e21f8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e21f8-111">Return Value</span></span>

<span data-ttu-id="e21f8-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e21f8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e21f8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e21f8-113">Remarks</span></span>

<span data-ttu-id="e21f8-114">Si el inicio es 0 y el final es 1, se selecciona todo el texto del control cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="e21f8-114">If the start is 0 and the end is  1, all of the text in the edit box control is selected.</span></span> <span data-ttu-id="e21f8-115">Si el inicio es 1, se anula la selección de cualquier selección actual.</span><span class="sxs-lookup"><span data-stu-id="e21f8-115">If the start is  1, any current selection is deselected.</span></span>

<span data-ttu-id="e21f8-116">Solo se puede llamar a este método después de que el control se vuelva visible.</span><span class="sxs-lookup"><span data-stu-id="e21f8-116">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="e21f8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e21f8-117">Requirements</span></span>



| <span data-ttu-id="e21f8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e21f8-118">Requirement</span></span> | <span data-ttu-id="e21f8-119">Value</span><span class="sxs-lookup"><span data-stu-id="e21f8-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="e21f8-120">Versión</span><span class="sxs-lookup"><span data-stu-id="e21f8-120">Version</span></span><br/> | <span data-ttu-id="e21f8-121">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="e21f8-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e21f8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e21f8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e21f8-123">**Elemento EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="e21f8-123">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="e21f8-124">**EDITBOX. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="e21f8-124">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="e21f8-125">**EDITBOX. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="e21f8-125">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="e21f8-126">**EDITBOX. replaceSelection**</span><span class="sxs-lookup"><span data-stu-id="e21f8-126">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> </dl>

 

 





