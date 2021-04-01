---
title: Mensaje EM_SETLANGOPTIONS (RichEdit. h)
description: Establece opciones para la compatibilidad con el editor de métodos de entrada (IME) y idiomas asiáticos en un control Rich Edit.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- EM_SETLANGOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996290"
---
# <a name="em_setlangoptions-message"></a><span data-ttu-id="3dbfa-104">\_Mensaje SETLANGOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="3dbfa-104">EM\_SETLANGOPTIONS message</span></span>

<span data-ttu-id="3dbfa-105">Establece opciones para la compatibilidad con el editor de métodos de entrada (IME) y idiomas asiáticos en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-105">Sets options for Input Method Editor (IME) and Asian language support in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3dbfa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3dbfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dbfa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3dbfa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3dbfa-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3dbfa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3dbfa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3dbfa-110">Especifica las opciones de idioma.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-110">Specifies the language options.</span></span> <span data-ttu-id="3dbfa-111">Para obtener una lista de los valores posibles, vea [**em \_ GETLANGOPTIONS**](em-getlangoptions.md).</span><span class="sxs-lookup"><span data-stu-id="3dbfa-111">For a list of possible values, see [**EM\_GETLANGOPTIONS**](em-getlangoptions.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dbfa-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3dbfa-112">Return value</span></span>

<span data-ttu-id="3dbfa-113">Este mensaje devuelve un valor de 1.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-113">This message returns a value of 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dbfa-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3dbfa-114">Remarks</span></span>

<span data-ttu-id="3dbfa-115">El **mensaje \_ SETLANGOPTIONS em** controla lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3dbfa-115">The **EM\_SETLANGOPTIONS** message controls the following:</span></span>

-   <span data-ttu-id="3dbfa-116">Enlace de fuente automático.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-116">Automatic font binding.</span></span>
-   <span data-ttu-id="3dbfa-117">Cambio automático de teclado.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-117">Automatic keyboard switching.</span></span>
-   <span data-ttu-id="3dbfa-118">Ajuste automático de tamaño de fuente.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-118">Automatic font size adjustment.</span></span>
-   <span data-ttu-id="3dbfa-119">Uso de las fuentes predeterminadas de la interfaz de usuario en lugar de las fuentes predeterminadas del documento.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-119">Use of user-interface default fonts instead of document default fonts.</span></span>
-   <span data-ttu-id="3dbfa-120">Notificaciones al cliente durante la composición del IME.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-120">Notifications to client during IME composition.</span></span>
-   <span data-ttu-id="3dbfa-121">Cómo el IME anula el modo de composición.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-121">How IME aborts composition mode.</span></span>
-   <span data-ttu-id="3dbfa-122">Revisión ortográfica, Autocorrección y predicción táctil de teclado.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-122">Spell checking, autocorrect, and touch keyboard prediction.</span></span>

<span data-ttu-id="3dbfa-123">Este mensaje establece los valores de todas las marcas de opciones de lenguaje.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-123">This message sets the values of all language option flags.</span></span> <span data-ttu-id="3dbfa-124">Para cambiar un subconjunto de las marcas, envíe el mensaje [**em \_ GETLANGOPTIONS**](em-getlangoptions.md) para obtener las marcas de opciones actuales, cambie las marcas que debe cambiar y, a continuación, envíe el mensaje **\_ SETLANGOPTIONS em** con el resultado.</span><span class="sxs-lookup"><span data-stu-id="3dbfa-124">To change a subset of the flags, send the [**EM\_GETLANGOPTIONS**](em-getlangoptions.md) message to get the current option flags, change the flags that you need to change, and then send the **EM\_SETLANGOPTIONS** message with the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dbfa-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dbfa-125">Requirements</span></span>



| <span data-ttu-id="3dbfa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dbfa-126">Requirement</span></span> | <span data-ttu-id="3dbfa-127">Value</span><span class="sxs-lookup"><span data-stu-id="3dbfa-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3dbfa-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dbfa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3dbfa-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3dbfa-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3dbfa-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dbfa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3dbfa-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3dbfa-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3dbfa-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3dbfa-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dbfa-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dbfa-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dbfa-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3dbfa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dbfa-135">**\_GETLANGOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="3dbfa-135">**EM\_GETLANGOPTIONS**</span></span>](em-getlangoptions.md)
</dt> </dl>

 

 





