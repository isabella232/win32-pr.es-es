---
title: Mensaje de LVM_GETSTRINGWIDTH (commctrl. h)
description: Determina el ancho de una cadena especificada utilizando la fuente actual del control de vista de lista especificada. Puede enviar este mensaje explícitamente o mediante la \_ macro GetStringWidth de ListView.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- LVM_GETSTRINGWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535038"
---
# <a name="lvm_getstringwidth-message"></a><span data-ttu-id="2c088-105">\_Mensaje GETSTRINGWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="2c088-105">LVM\_GETSTRINGWIDTH message</span></span>

<span data-ttu-id="2c088-106">Determina el ancho de una cadena especificada utilizando la fuente actual del control de vista de lista especificada.</span><span class="sxs-lookup"><span data-stu-id="2c088-106">Determines the width of a specified string using the specified list-view control's current font.</span></span> <span data-ttu-id="2c088-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetStringWidth de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) .</span><span class="sxs-lookup"><span data-stu-id="2c088-107">You can send this message explicitly or by using the [**ListView\_GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c088-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c088-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c088-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c088-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2c088-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2c088-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2c088-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c088-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c088-112">Puntero a una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="2c088-112">Pointer to a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c088-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c088-113">Return value</span></span>

<span data-ttu-id="2c088-114">Devuelve el ancho de la cadena si se realiza correctamente o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2c088-114">Returns the string width if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c088-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c088-115">Remarks</span></span>

<span data-ttu-id="2c088-116">El \_ mensaje LVM GETSTRINGWIDTH devuelve el ancho exacto, en píxeles, de la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="2c088-116">The LVM\_GETSTRINGWIDTH message returns the exact width, in pixels, of the specified string.</span></span> <span data-ttu-id="2c088-117">Si usa el ancho de cadena devuelto como el ancho de columna en el mensaje [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) , la cadena se truncará.</span><span class="sxs-lookup"><span data-stu-id="2c088-117">If you use the returned string width as the column width in the [**LVM\_SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) message, the string will be truncated.</span></span> <span data-ttu-id="2c088-118">Para recuperar el ancho de columna que puede contener la cadena sin truncarla, debe agregar relleno al ancho de la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="2c088-118">To retrieve the column width that can contain the string without truncating it, you must add padding to the returned string width.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c088-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c088-119">Requirements</span></span>



| <span data-ttu-id="2c088-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c088-120">Requirement</span></span> | <span data-ttu-id="2c088-121">Value</span><span class="sxs-lookup"><span data-stu-id="2c088-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c088-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c088-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2c088-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2c088-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c088-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c088-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2c088-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c088-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c088-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c088-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c088-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c088-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2c088-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="2c088-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2c088-129">**LVM \_ GETSTRINGWIDTHW** (Unicode) y **\_ GETSTRINGWIDTHA de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2c088-129">**LVM\_GETSTRINGWIDTHW** (Unicode) and **LVM\_GETSTRINGWIDTHA** (ANSI)</span></span><br/>     |



 

 





