---
title: Mensaje de BCM_GETNOTELENGTH (commctrl. h)
description: Obtiene la longitud del texto de la nota que se puede mostrar en la descripción de un botón de vínculo de comando. Envíe este mensaje explícitamente o mediante la \_ macro Button GetNoteLength.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- BCM_GETNOTELENGTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079275"
---
# <a name="bcm_getnotelength-message"></a><span data-ttu-id="e9bf0-105">\_Mensaje GETNOTELENGTH de BCM</span><span class="sxs-lookup"><span data-stu-id="e9bf0-105">BCM\_GETNOTELENGTH message</span></span>

<span data-ttu-id="e9bf0-106">Obtiene la longitud del texto de la nota que se puede mostrar en la descripción de un botón de vínculo de comando.</span><span class="sxs-lookup"><span data-stu-id="e9bf0-106">Gets the length of the note text that may be displayed in the description for a command link button.</span></span> <span data-ttu-id="e9bf0-107">Envíe este mensaje explícitamente o mediante la macro [**Button \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) .</span><span class="sxs-lookup"><span data-stu-id="e9bf0-107">Send this message explicitly or by using the [**Button\_GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9bf0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9bf0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9bf0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9bf0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9bf0-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e9bf0-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e9bf0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9bf0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9bf0-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e9bf0-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9bf0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9bf0-113">Return value</span></span>

<span data-ttu-id="e9bf0-114">Devuelve la longitud del texto de la nota en **WCHARs**, sin incluir el carácter **nulo** final, o cero si no hay texto de nota.</span><span class="sxs-lookup"><span data-stu-id="e9bf0-114">Returns the length of the note text in **WCHARs**, not including any terminating **NULL**, or zero if there is no note text.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9bf0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9bf0-115">Remarks</span></span>

<span data-ttu-id="e9bf0-116">A partir de la versión 6,01 de comctl32 DLL, los botones de vínculo de comando pueden tener una nota.</span><span class="sxs-lookup"><span data-stu-id="e9bf0-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span> <span data-ttu-id="e9bf0-117">Para obtener información sobre las versiones de DLL, vea [versiones de control comunes](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="e9bf0-117">For information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="e9bf0-118">El **mensaje \_ GETNOTELENGTH de BCM** solo funciona con los estilos de botón [**BS \_ COMMANDLINK**](button-styles.md) y [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e9bf0-118">The **BCM\_GETNOTELENGTH** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9bf0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9bf0-119">Requirements</span></span>



| <span data-ttu-id="e9bf0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9bf0-120">Requirement</span></span> | <span data-ttu-id="e9bf0-121">Value</span><span class="sxs-lookup"><span data-stu-id="e9bf0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bf0-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9bf0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e9bf0-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e9bf0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9bf0-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9bf0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e9bf0-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9bf0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9bf0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9bf0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9bf0-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9bf0-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9bf0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9bf0-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9bf0-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e9bf0-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e9bf0-130">Estilos de botón</span><span class="sxs-lookup"><span data-stu-id="e9bf0-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="e9bf0-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="e9bf0-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e9bf0-132">Tipos de botón</span><span class="sxs-lookup"><span data-stu-id="e9bf0-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





