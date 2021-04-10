---
title: Mensaje de TB_GETBUTTONINFO (commctrl. h)
description: Recupera información extendida para un botón de una barra de herramientas.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- TB_GETBUTTONINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c7f6a8d1d36737d09cfb4d307129200a51180c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151259"
---
# <a name="tb_getbuttoninfo-message"></a><span data-ttu-id="55d10-104">\_Mensaje GETBUTTONINFO TB</span><span class="sxs-lookup"><span data-stu-id="55d10-104">TB\_GETBUTTONINFO message</span></span>

<span data-ttu-id="55d10-105">Recupera información extendida para un botón de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="55d10-105">Retrieves extended information for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="55d10-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55d10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55d10-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55d10-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55d10-108">Identificador de comando del botón.</span><span class="sxs-lookup"><span data-stu-id="55d10-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="55d10-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55d10-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55d10-110">Puntero a una estructura [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) que recibe la información del botón.</span><span class="sxs-lookup"><span data-stu-id="55d10-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that receives the button information.</span></span> <span data-ttu-id="55d10-111">Los miembros **cbSize** y **dwMask** de esta estructura se deben rellenar antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="55d10-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55d10-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55d10-112">Return value</span></span>

<span data-ttu-id="55d10-113">Devuelve el índice de base cero del botón o-1 si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="55d10-113">Returns the zero-based index of the button, or -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="55d10-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55d10-114">Remarks</span></span>

<span data-ttu-id="55d10-115">Al usar [**TB \_ ADDBUTTONS**](tb-addbuttons.md) o [**TB \_ INSERTBUTTON**](tb-insertbutton.md) para colocar botones en la barra de herramientas, el texto del botón se especifica normalmente mediante su índice de grupo de cadenas.</span><span class="sxs-lookup"><span data-stu-id="55d10-115">When you use [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) to place buttons on the toolbar, the button text is commonly specified by its string pool index.</span></span> <span data-ttu-id="55d10-116">**TB \_ GETBUTTONINFO** no recuperará esta cadena.</span><span class="sxs-lookup"><span data-stu-id="55d10-116">**TB\_GETBUTTONINFO** will not retrieve this string.</span></span> <span data-ttu-id="55d10-117">Para usar **TB \_ GETBUTTONINFO** para recuperar el texto del botón, primero debe establecer la cadena de texto con [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md).</span><span class="sxs-lookup"><span data-stu-id="55d10-117">To use **TB\_GETBUTTONINFO** to retrieve button text, you must first set the text string with [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md).</span></span> <span data-ttu-id="55d10-118">Una vez que haya establecido el texto del botón con **TB \_ SETBUTTONINFO**, ya no podrá usar el índice del grupo de cadenas.</span><span class="sxs-lookup"><span data-stu-id="55d10-118">Once you have set the button text with **TB\_SETBUTTONINFO**, you can no longer use the string pool index.</span></span>

## <a name="requirements"></a><span data-ttu-id="55d10-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55d10-119">Requirements</span></span>



| <span data-ttu-id="55d10-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="55d10-120">Requirement</span></span> | <span data-ttu-id="55d10-121">Value</span><span class="sxs-lookup"><span data-stu-id="55d10-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55d10-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55d10-122">Minimum supported client</span></span><br/> | <span data-ttu-id="55d10-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="55d10-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55d10-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55d10-124">Minimum supported server</span></span><br/> | <span data-ttu-id="55d10-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="55d10-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55d10-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55d10-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="55d10-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55d10-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="55d10-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="55d10-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="55d10-129">**TB \_ GETBUTTONINFOW** (Unicode) y **TB \_ GETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="55d10-129">**TB\_GETBUTTONINFOW** (Unicode) and **TB\_GETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="55d10-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="55d10-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="55d10-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="55d10-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="55d10-132">**TB \_ SETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="55d10-132">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="55d10-133">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="55d10-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> </dl>

 

 





