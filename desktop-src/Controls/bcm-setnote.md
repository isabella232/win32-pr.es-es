---
title: Mensaje de BCM_SETNOTE (commctrl. h)
description: Establece el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button SetNote.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- BCM_SETNOTE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996380"
---
# <a name="bcm_setnote-message"></a><span data-ttu-id="242f1-105">\_Mensaje SETNOTE de BCM</span><span class="sxs-lookup"><span data-stu-id="242f1-105">BCM\_SETNOTE message</span></span>

<span data-ttu-id="242f1-106">Establece el texto de la nota asociada a un botón de vínculo de comando.</span><span class="sxs-lookup"><span data-stu-id="242f1-106">Sets the text of the note associated with a command link button.</span></span> <span data-ttu-id="242f1-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) .</span><span class="sxs-lookup"><span data-stu-id="242f1-107">You can send this message explicitly or use the [**Button\_SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="242f1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="242f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="242f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="242f1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="242f1-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="242f1-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="242f1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="242f1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="242f1-112">Puntero a una cadena **WCHAR** terminada en null que contiene la nota.</span><span class="sxs-lookup"><span data-stu-id="242f1-112">A pointer to a null-terminated **WCHAR** string that contains the note.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="242f1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="242f1-113">Return value</span></span>

<span data-ttu-id="242f1-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="242f1-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="242f1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="242f1-115">Remarks</span></span>

<span data-ttu-id="242f1-116">A partir de la versión 6,01 de comctl32 DLL, los botones de vínculo de comando pueden tener una nota.</span><span class="sxs-lookup"><span data-stu-id="242f1-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span>

<span data-ttu-id="242f1-117">El **mensaje \_ SETNOTE de BCM** solo funciona con los estilos de botón [**BS \_ COMMANDLINK**](button-styles.md) y [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="242f1-117">The **BCM\_SETNOTE** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="242f1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="242f1-118">Requirements</span></span>



| <span data-ttu-id="242f1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="242f1-119">Requirement</span></span> | <span data-ttu-id="242f1-120">Value</span><span class="sxs-lookup"><span data-stu-id="242f1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="242f1-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="242f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="242f1-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="242f1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="242f1-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="242f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="242f1-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="242f1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="242f1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="242f1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="242f1-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="242f1-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="242f1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="242f1-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="242f1-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="242f1-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="242f1-129">Estilos de botón</span><span class="sxs-lookup"><span data-stu-id="242f1-129">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="242f1-130">**Vista**</span><span class="sxs-lookup"><span data-stu-id="242f1-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="242f1-131">Tipos de botón</span><span class="sxs-lookup"><span data-stu-id="242f1-131">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





