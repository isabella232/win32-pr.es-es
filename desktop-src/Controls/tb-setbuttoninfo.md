---
title: Mensaje de TB_SETBUTTONINFO (commctrl. h)
description: Establece la información de un botón existente en una barra de herramientas.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- TB_SETBUTTONINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70612a90f245a25dde5a487917d7c3b669424ea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905589"
---
# <a name="tb_setbuttoninfo-message"></a><span data-ttu-id="7ef41-104">\_Mensaje SETBUTTONINFO TB</span><span class="sxs-lookup"><span data-stu-id="7ef41-104">TB\_SETBUTTONINFO message</span></span>

<span data-ttu-id="7ef41-105">Establece la información de un botón existente en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="7ef41-105">Sets the information for an existing button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ef41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ef41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ef41-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ef41-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ef41-108">Identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="7ef41-108">Button identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7ef41-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ef41-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ef41-110">Puntero a una estructura [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) que contiene la información del nuevo botón.</span><span class="sxs-lookup"><span data-stu-id="7ef41-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that contains the new button information.</span></span> <span data-ttu-id="7ef41-111">Los miembros **cbSize** y **dwMask** de esta estructura se deben rellenar antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="7ef41-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ef41-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ef41-112">Return value</span></span>

<span data-ttu-id="7ef41-113">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="7ef41-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ef41-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ef41-114">Remarks</span></span>

<span data-ttu-id="7ef41-115">Normalmente, el texto se asigna a los botones cuando se agregan a una barra de herramientas especificando el índice de una cadena en el grupo de cadenas de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="7ef41-115">Text is commonly assigned to buttons when they are added to a toolbar by specifying the index of a string in the toolbar's string pool.</span></span> <span data-ttu-id="7ef41-116">Si usa un **\_ SETBUTTONINFO TB** para asignar texto nuevo a un botón, invalidará permanentemente el texto del grupo de cadenas.</span><span class="sxs-lookup"><span data-stu-id="7ef41-116">If you use a **TB\_SETBUTTONINFO** to assign new text to a button, it will permanently override the text from the string pool.</span></span> <span data-ttu-id="7ef41-117">Puede cambiar el texto llamando a **TB \_ SETBUTTONINFO** de nuevo, pero no puede reasignar la cadena del grupo de cadenas.</span><span class="sxs-lookup"><span data-stu-id="7ef41-117">You can change the text by calling **TB\_SETBUTTONINFO** again, but you cannot reassign the string from the string pool.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ef41-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ef41-118">Requirements</span></span>



| <span data-ttu-id="7ef41-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ef41-119">Requirement</span></span> | <span data-ttu-id="7ef41-120">Value</span><span class="sxs-lookup"><span data-stu-id="7ef41-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef41-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ef41-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7ef41-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7ef41-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ef41-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ef41-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7ef41-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ef41-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ef41-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ef41-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ef41-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ef41-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7ef41-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="7ef41-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7ef41-128">**TB \_ SETBUTTONINFOW** (Unicode) y **TB \_ SETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7ef41-128">**TB\_SETBUTTONINFOW** (Unicode) and **TB\_SETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="7ef41-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ef41-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="7ef41-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7ef41-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7ef41-131">**TB \_ ADDBUTTONS**</span><span class="sxs-lookup"><span data-stu-id="7ef41-131">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="7ef41-132">**TB \_ GETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="7ef41-132">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="7ef41-133">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="7ef41-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> <dt>

[<span data-ttu-id="7ef41-134">**GETSTRING de TB \_**</span><span class="sxs-lookup"><span data-stu-id="7ef41-134">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="7ef41-135">**TB \_ INSERTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="7ef41-135">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

 





