---
title: EDITBOX. replaceSelection
description: El método replaceSelection reemplaza la selección actual por el texto especificado.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- EDITBOX. replaceSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699391"
---
# <a name="editboxreplaceselection"></a><span data-ttu-id="dc967-104">EDITBOX. replaceSelection</span><span class="sxs-lookup"><span data-stu-id="dc967-104">EDITBOX.replaceSelection</span></span>

<span data-ttu-id="dc967-105">El método **replaceSelection** reemplaza la selección actual por el texto especificado.</span><span class="sxs-lookup"><span data-stu-id="dc967-105">The **replaceSelection** method replaces the current selection with the specified text.</span></span>

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a><span data-ttu-id="dc967-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc967-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc967-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*Nuevovalor*</span><span class="sxs-lookup"><span data-stu-id="dc967-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span></span>
</dt> <dd>

<span data-ttu-id="dc967-108">**Cadena** que contiene el texto en el que se va a reemplazar el texto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="dc967-108">**String** containing the text to replace the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc967-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc967-109">Return Value</span></span>

<span data-ttu-id="dc967-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dc967-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc967-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc967-111">Remarks</span></span>

<span data-ttu-id="dc967-112">Si no hay texto seleccionado, el texto de sustitución se inserta en la ubicación actual del punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="dc967-112">If there is no text selected, the replacement text is inserted at the current location of the insertion point.</span></span>

<span data-ttu-id="dc967-113">Solo se puede llamar a este método después de que el control se vuelva visible.</span><span class="sxs-lookup"><span data-stu-id="dc967-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc967-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc967-114">Requirements</span></span>



| <span data-ttu-id="dc967-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc967-115">Requirement</span></span> | <span data-ttu-id="dc967-116">Value</span><span class="sxs-lookup"><span data-stu-id="dc967-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="dc967-117">Versión</span><span class="sxs-lookup"><span data-stu-id="dc967-117">Version</span></span><br/> | <span data-ttu-id="dc967-118">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="dc967-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc967-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc967-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc967-120">**Elemento EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="dc967-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="dc967-121">**EDITBOX. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="dc967-121">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="dc967-122">**EDITBOX. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="dc967-122">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="dc967-123">**EDITBOX. setSelection**</span><span class="sxs-lookup"><span data-stu-id="dc967-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





