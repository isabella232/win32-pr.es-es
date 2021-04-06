---
title: Mensaje de CBEM_SETITEM (commctrl. h)
description: Establece los atributos de un elemento en un control ComboBoxEx.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- CBEM_SETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803698"
---
# <a name="cbem_setitem-message"></a><span data-ttu-id="b847a-104">CBEM \_ SETITEM</span><span class="sxs-lookup"><span data-stu-id="b847a-104">CBEM\_SETITEM message</span></span>

<span data-ttu-id="b847a-105">Establece los atributos de un elemento en un control ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="b847a-105">Sets the attributes for an item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b847a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b847a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b847a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b847a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b847a-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b847a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b847a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b847a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b847a-110">Puntero a una estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que contiene la información del elemento que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="b847a-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains the item information to be set.</span></span> <span data-ttu-id="b847a-111">Cuando se envía el mensaje, se debe establecer el miembro de **máscara** de la estructura para indicar qué atributos son válidos y el miembro **iItem** debe especificar el índice de base cero del elemento que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="b847a-111">When the message is sent, the **mask** member of the structure must be set to indicate which attributes are valid and the **iItem** member must specify the zero-based index of the item to be modified.</span></span> <span data-ttu-id="b847a-112">Si se establece el miembro **iItem** en-1, se modificará el elemento mostrado en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="b847a-112">Setting the **iItem** member to -1 will modify the item displayed in the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b847a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b847a-113">Return value</span></span>

<span data-ttu-id="b847a-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="b847a-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b847a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b847a-115">Requirements</span></span>



| <span data-ttu-id="b847a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b847a-116">Requirement</span></span> | <span data-ttu-id="b847a-117">Value</span><span class="sxs-lookup"><span data-stu-id="b847a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b847a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b847a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b847a-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b847a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b847a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b847a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b847a-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b847a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b847a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b847a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b847a-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b847a-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b847a-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="b847a-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b847a-125">**CBEM \_ SETITEMW** (Unicode) y **CBEM \_ SETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b847a-125">**CBEM\_SETITEMW** (Unicode) and **CBEM\_SETITEMA** (ANSI)</span></span><br/>                 |



 

 





