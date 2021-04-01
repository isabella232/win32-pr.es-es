---
title: Mensaje de LVM_SETCOLUMN (commctrl. h)
description: Establece los atributos de una columna de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetColumn de ListView.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- LVM_SETCOLUMN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996428"
---
# <a name="lvm_setcolumn-message"></a><span data-ttu-id="ea126-105">\_Mensaje SETCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="ea126-105">LVM\_SETCOLUMN message</span></span>

<span data-ttu-id="ea126-106">Establece los atributos de una columna de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="ea126-106">Sets the attributes of a list-view column.</span></span> <span data-ttu-id="ea126-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetColumn de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) .</span><span class="sxs-lookup"><span data-stu-id="ea126-107">You can send this message explicitly or by using the [**ListView\_SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea126-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea126-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea126-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea126-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea126-110">Índice de la columna.</span><span class="sxs-lookup"><span data-stu-id="ea126-110">Index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="ea126-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea126-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea126-112">Puntero a una estructura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contiene los nuevos atributos de columna.</span><span class="sxs-lookup"><span data-stu-id="ea126-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the new column attributes.</span></span> <span data-ttu-id="ea126-113">El miembro **Mask** especifica los atributos de columna que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="ea126-113">The **mask** member specifies which column attributes to set.</span></span> <span data-ttu-id="ea126-114">Si el miembro **Mask** especifica el \_ valor de texto LVCF, el miembro **miembros pszText** es la dirección de una cadena terminada en NULL y se omite el miembro **cchTextMax** .</span><span class="sxs-lookup"><span data-stu-id="ea126-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea126-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea126-115">Return value</span></span>

<span data-ttu-id="ea126-116">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ea126-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea126-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea126-117">Requirements</span></span>



| <span data-ttu-id="ea126-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea126-118">Requirement</span></span> | <span data-ttu-id="ea126-119">Value</span><span class="sxs-lookup"><span data-stu-id="ea126-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea126-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea126-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ea126-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ea126-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea126-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea126-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ea126-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea126-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea126-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea126-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea126-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea126-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ea126-126">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ea126-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ea126-127">**LVM \_ SETCOLUMNW** (Unicode) y **\_ SETCOLUMNW de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ea126-127">**LVM\_SETCOLUMNW** (Unicode) and **LVM\_SETCOLUMNW** (ANSI)</span></span><br/>               |



 

 





