---
title: Mensaje de LVM_GETBKIMAGE (commctrl. h)
description: Obtiene la imagen de fondo de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetBkImage de ListView.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- LVM_GETBKIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801118"
---
# <a name="lvm_getbkimage-message"></a><span data-ttu-id="eea6f-105">\_Mensaje GETBKIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="eea6f-105">LVM\_GETBKIMAGE message</span></span>

<span data-ttu-id="eea6f-106">Obtiene la imagen de fondo de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="eea6f-106">Gets the background image in a list-view control.</span></span> <span data-ttu-id="eea6f-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetBkImage de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) .</span><span class="sxs-lookup"><span data-stu-id="eea6f-107">You can send this message explicitly or by using the [**ListView\_GetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eea6f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eea6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea6f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eea6f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eea6f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="eea6f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eea6f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eea6f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eea6f-112">Puntero a una estructura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) que recibirá la información de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="eea6f-112">A pointer to an [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that will receive the background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eea6f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eea6f-113">Return value</span></span>

<span data-ttu-id="eea6f-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="eea6f-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea6f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eea6f-115">Requirements</span></span>



| <span data-ttu-id="eea6f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea6f-116">Requirement</span></span> | <span data-ttu-id="eea6f-117">Value</span><span class="sxs-lookup"><span data-stu-id="eea6f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eea6f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eea6f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eea6f-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eea6f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eea6f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eea6f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eea6f-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="eea6f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eea6f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eea6f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eea6f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eea6f-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="eea6f-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="eea6f-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="eea6f-125">**LVM \_ GETBKIMAGEW** (Unicode) y **\_ GETBKIMAGEA de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="eea6f-125">**LVM\_GETBKIMAGEW** (Unicode) and **LVM\_GETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="eea6f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="eea6f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea6f-127">**\_SETBKIMAGE LVM**</span><span class="sxs-lookup"><span data-stu-id="eea6f-127">**LVM\_SETBKIMAGE**</span></span>](lvm-setbkimage.md)
</dt> </dl>

 

 





