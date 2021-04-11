---
title: Mensaje EM_GETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Devuelve el estado actual de las opciones tipográficas de un control Rich Edit.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- EM_GETTYPOGRAPHYOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150761"
---
# <a name="em_gettypographyoptions-message"></a><span data-ttu-id="ad5f7-104">\_Mensaje GETTYPOGRAPHYOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="ad5f7-104">EM\_GETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="ad5f7-105">Devuelve el estado actual de las opciones tipográficas de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-105">Returns the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad5f7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad5f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad5f7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad5f7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad5f7-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ad5f7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad5f7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad5f7-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad5f7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad5f7-111">Return value</span></span>

<span data-ttu-id="ad5f7-112">Devuelve las opciones de tipografía actuales.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-112">Returns the current typography options.</span></span> <span data-ttu-id="ad5f7-113">Para obtener una lista de opciones, consulte [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).</span><span class="sxs-lookup"><span data-stu-id="ad5f7-113">For a list of options, see [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad5f7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad5f7-114">Remarks</span></span>

<span data-ttu-id="ad5f7-115">Puede activar el salto de línea avanzado enviando el mensaje [**\_ SETTYPOGRAPHYOPTIONS em**](em-settypographyoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="ad5f7-115">You can turn on advanced line breaking by sending the [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) message.</span></span> <span data-ttu-id="ad5f7-116">El control Rich Edit también puede activar el salto de línea avanzado y normal automáticamente si es necesario para determinados idiomas.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-116">Advanced and normal line breaking may also be turned on automatically by the rich edit control if it is needed for certain languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad5f7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad5f7-117">Requirements</span></span>



| <span data-ttu-id="ad5f7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad5f7-118">Requirement</span></span> | <span data-ttu-id="ad5f7-119">Value</span><span class="sxs-lookup"><span data-stu-id="ad5f7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad5f7-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad5f7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ad5f7-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ad5f7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad5f7-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad5f7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ad5f7-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad5f7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad5f7-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ad5f7-124">Redistributable</span></span><br/>          | <span data-ttu-id="ad5f7-125">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="ad5f7-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="ad5f7-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad5f7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad5f7-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad5f7-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad5f7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad5f7-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad5f7-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ad5f7-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad5f7-130">**\_SETTYPOGRAPHYOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="ad5f7-130">**EM\_SETTYPOGRAPHYOPTIONS**</span></span>](em-settypographyoptions.md)
</dt> <dt>

<span data-ttu-id="ad5f7-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ad5f7-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ad5f7-132">Acerca de los controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="ad5f7-132">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





