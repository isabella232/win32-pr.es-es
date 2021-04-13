---
title: Mensaje EM_SETEDITSTYLE (RichEdit. h)
description: Establece las marcas de estilo de edición actuales para un control Rich Edit.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- EM_SETEDITSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535056"
---
# <a name="em_seteditstyle-message"></a><span data-ttu-id="f3a0c-104">\_Mensaje SETEDITSTYLE em</span><span class="sxs-lookup"><span data-stu-id="f3a0c-104">EM\_SETEDITSTYLE message</span></span>

<span data-ttu-id="f3a0c-105">Establece las marcas de estilo de edición actuales para un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f3a0c-105">Sets the current edit style flags for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3a0c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3a0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a0c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3a0c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3a0c-108">Especifica una o más marcas de estilo de edición.</span><span class="sxs-lookup"><span data-stu-id="f3a0c-108">Specifies one or more edit style flags.</span></span> <span data-ttu-id="f3a0c-109">Para obtener una lista de los valores posibles, consulte [**em \_ GETEDITSTYLE**](em-geteditstyle.md).</span><span class="sxs-lookup"><span data-stu-id="f3a0c-109">For a list of possible values, see [**EM\_GETEDITSTYLE**](em-geteditstyle.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3a0c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3a0c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3a0c-111">Máscara formada por uno o varios de los valores de *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f3a0c-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="f3a0c-112">Solo se establecerán o se borrarán los valores especificados en esta máscara.</span><span class="sxs-lookup"><span data-stu-id="f3a0c-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="f3a0c-113">Esto permite establecer o borrar una sola marca sin leer los Estados actuales de la marca.</span><span class="sxs-lookup"><span data-stu-id="f3a0c-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3a0c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3a0c-114">Return value</span></span>

<span data-ttu-id="f3a0c-115">El valor devuelto es el estado de las marcas de estilo de edición después de que el control Rich Edit ha intentado implementar los cambios de estilo de edición.</span><span class="sxs-lookup"><span data-stu-id="f3a0c-115">The return value is the state of the edit style flags after the rich edit control has attempted to implement your edit style changes.</span></span> <span data-ttu-id="f3a0c-116">Las marcas de estilo de edición son un conjunto de marcas que indican el estilo de edición actual.</span><span class="sxs-lookup"><span data-stu-id="f3a0c-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a0c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3a0c-117">Requirements</span></span>



| <span data-ttu-id="f3a0c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3a0c-118">Requirement</span></span> | <span data-ttu-id="f3a0c-119">Value</span><span class="sxs-lookup"><span data-stu-id="f3a0c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a0c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3a0c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a0c-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f3a0c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3a0c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3a0c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a0c-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3a0c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3a0c-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f3a0c-124">Redistributable</span></span><br/>          | <span data-ttu-id="f3a0c-125">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="f3a0c-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="f3a0c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3a0c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3a0c-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3a0c-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a0c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3a0c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a0c-129">**\_GETEDITSTYLE em**</span><span class="sxs-lookup"><span data-stu-id="f3a0c-129">**EM\_GETEDITSTYLE**</span></span>](em-geteditstyle.md)
</dt> </dl>

 

 





