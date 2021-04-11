---
title: Mensaje de TB_GETSTRING (commctrl. h)
description: Recupera una cadena del grupo de cadenas de una barra de herramientas.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- TB_GETSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079129"
---
# <a name="tb_getstring-message"></a><span data-ttu-id="1b0b1-104">TB \_ mensaje de GETSTRING</span><span class="sxs-lookup"><span data-stu-id="1b0b1-104">TB\_GETSTRING message</span></span>

<span data-ttu-id="1b0b1-105">Recupera una cadena del grupo de cadenas de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="1b0b1-105">Retrieves a string from a toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b0b1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b0b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b0b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b0b1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b0b1-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la longitud del búfer *lParam* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="1b0b1-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the length of the *lParam* buffer, in bytes.</span></span> <span data-ttu-id="1b0b1-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el índice de la cadena.</span><span class="sxs-lookup"><span data-stu-id="1b0b1-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="1b0b1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b0b1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b0b1-111">Puntero a un búfer que se usa para devolver la cadena.</span><span class="sxs-lookup"><span data-stu-id="1b0b1-111">Pointer to a buffer used to return the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b0b1-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b0b1-112">Return value</span></span>

<span data-ttu-id="1b0b1-113">Devuelve la longitud de la cadena si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1b0b1-113">Returns the string length if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b0b1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b0b1-114">Remarks</span></span>

<span data-ttu-id="1b0b1-115">Este mensaje devuelve la cadena especificada del grupo de cadenas de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="1b0b1-115">This message returns the specified string from the toolbar's string pool.</span></span> <span data-ttu-id="1b0b1-116">No se corresponde necesariamente con la cadena de texto que se muestra actualmente en un botón.</span><span class="sxs-lookup"><span data-stu-id="1b0b1-116">It does not necessarily correspond to the text string currently being displayed by a button.</span></span> <span data-ttu-id="1b0b1-117">Para recuperar la cadena de texto actual de un botón, envíe la barra de herramientas a un mensaje [**\_ GETBUTTONTEXT TB**](tb-getbuttontext.md) .</span><span class="sxs-lookup"><span data-stu-id="1b0b1-117">To retrieve a button's current text string, send the toolbar a [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b0b1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b0b1-118">Requirements</span></span>



| <span data-ttu-id="1b0b1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b0b1-119">Requirement</span></span> | <span data-ttu-id="1b0b1-120">Value</span><span class="sxs-lookup"><span data-stu-id="1b0b1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b0b1-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b0b1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1b0b1-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1b0b1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b0b1-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b0b1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1b0b1-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b0b1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b0b1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b0b1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b0b1-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b0b1-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1b0b1-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1b0b1-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1b0b1-128">**TB \_ GETSTRINGW** (Unicode) y **TB \_ GETSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1b0b1-128">**TB\_GETSTRINGW** (Unicode) and **TB\_GETSTRINGA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1b0b1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b0b1-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="1b0b1-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1b0b1-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1b0b1-131">**TB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="1b0b1-131">**TB\_ADDSTRING**</span></span>](tb-addstring.md)
</dt> <dt>

[<span data-ttu-id="1b0b1-132">**TB \_ ADDBUTTONS**</span><span class="sxs-lookup"><span data-stu-id="1b0b1-132">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="1b0b1-133">**TB \_ INSERTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="1b0b1-133">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

