---
title: EDITBOX. getLine
description: El método getLine recupera el texto de la línea con el índice especificado.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- GetLine Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0b9a15f9eff8c2612e7a242a205c1d9411a60c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698721"
---
# <a name="editboxgetline"></a><span data-ttu-id="5f932-104">EDITBOX. getLine</span><span class="sxs-lookup"><span data-stu-id="5f932-104">EDITBOX.getLine</span></span>

<span data-ttu-id="5f932-105">El método **getLine** recupera el texto de la línea con el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="5f932-105">The **getLine** method retrieves the text for the line with the specified index.</span></span>

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a><span data-ttu-id="5f932-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f932-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f932-107"><span id="index"></span><span id="INDEX"></span>*ajustar*</span><span class="sxs-lookup"><span data-stu-id="5f932-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="5f932-108">**Número** (**largo**) que contiene el índice de la línea que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="5f932-108">**Number** (**long**) containing the index of the line to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f932-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f932-109">Return Value</span></span>

<span data-ttu-id="5f932-110">Este método devuelve una **cadena**.</span><span class="sxs-lookup"><span data-stu-id="5f932-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f932-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f932-111">Remarks</span></span>

<span data-ttu-id="5f932-112">Si el índice no es válido, se devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="5f932-112">If the index is not valid, an empty string is returned.</span></span> <span data-ttu-id="5f932-113">Solo se puede llamar a este método después de que el control se vuelva visible.</span><span class="sxs-lookup"><span data-stu-id="5f932-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f932-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f932-114">Requirements</span></span>



| <span data-ttu-id="5f932-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f932-115">Requirement</span></span> | <span data-ttu-id="5f932-116">Value</span><span class="sxs-lookup"><span data-stu-id="5f932-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="5f932-117">Versión</span><span class="sxs-lookup"><span data-stu-id="5f932-117">Version</span></span><br/> | <span data-ttu-id="5f932-118">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="5f932-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f932-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f932-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f932-120">**Elemento EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="5f932-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="5f932-121">**EDITBOX. getLineFromChar**</span><span class="sxs-lookup"><span data-stu-id="5f932-121">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="5f932-122">**EDITBOX. getLineIndex**</span><span class="sxs-lookup"><span data-stu-id="5f932-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





