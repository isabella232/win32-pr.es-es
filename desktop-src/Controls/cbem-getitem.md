---
title: Mensaje de CBEM_GETITEM (commctrl. h)
description: Obtiene la información de un elemento ComboBoxEx determinado.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- CBEM_GETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940bbf7aea8ec93dd0f808937d959477c964df96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658341"
---
# <a name="cbem_getitem-message"></a><span data-ttu-id="db274-104">CBEM \_ mensaje GETITEM</span><span class="sxs-lookup"><span data-stu-id="db274-104">CBEM\_GETITEM message</span></span>

<span data-ttu-id="db274-105">Obtiene la información de un elemento ComboBoxEx determinado.</span><span class="sxs-lookup"><span data-stu-id="db274-105">Gets item information for a given ComboBoxEx item.</span></span>

## <a name="parameters"></a><span data-ttu-id="db274-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db274-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db274-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db274-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="db274-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="db274-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="db274-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db274-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db274-110">Puntero a una estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que recibe la información del elemento.</span><span class="sxs-lookup"><span data-stu-id="db274-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that receives the item information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db274-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db274-111">Return value</span></span>

<span data-ttu-id="db274-112">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="db274-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="db274-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db274-113">Remarks</span></span>

<span data-ttu-id="db274-114">Cuando se envía el mensaje, se deben establecer los miembros **iItem** y **Mask** de la estructura para indicar el índice del elemento de destino y el tipo de información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="db274-114">When the message is sent, the **iItem** and **mask** members of the structure must be set to indicate the index of the target item and the type of information to be retrieved.</span></span> <span data-ttu-id="db274-115">Otros miembros se establecen según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="db274-115">Other members are set as needed.</span></span> <span data-ttu-id="db274-116">Por ejemplo, para recuperar texto, debe establecer la \_ marca de texto CBEIF en **Mask** y asignar un valor a **cchTextMax**.</span><span class="sxs-lookup"><span data-stu-id="db274-116">For example, to retrieve text, you must set the CBEIF\_TEXT flag in **mask**, and assign a value to **cchTextMax**.</span></span> <span data-ttu-id="db274-117">Al establecer el miembro **iItem** en-1 se recuperará el elemento mostrado en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="db274-117">Setting the **iItem** member to -1 will retrieve the item displayed in the edit control.</span></span>

<span data-ttu-id="db274-118">Si la \_ marca de texto CBEIF se establece en el miembro **Mask** de la estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , el control puede cambiar el miembro **miembros pszText** de la estructura para que apunte al nuevo texto en lugar de llenar el búfer con el texto solicitado.</span><span class="sxs-lookup"><span data-stu-id="db274-118">If the CBEIF\_TEXT flag is set in the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="db274-119">Las aplicaciones no deben suponer que el texto siempre se colocará en el búfer solicitado.</span><span class="sxs-lookup"><span data-stu-id="db274-119">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="db274-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db274-120">Requirements</span></span>



| <span data-ttu-id="db274-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="db274-121">Requirement</span></span> | <span data-ttu-id="db274-122">Value</span><span class="sxs-lookup"><span data-stu-id="db274-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db274-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db274-123">Minimum supported client</span></span><br/> | <span data-ttu-id="db274-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="db274-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db274-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db274-125">Minimum supported server</span></span><br/> | <span data-ttu-id="db274-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="db274-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db274-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db274-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="db274-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db274-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="db274-129">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="db274-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="db274-130">**CBEM \_ GETITEMW** (Unicode) y **CBEM \_ GETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="db274-130">**CBEM\_GETITEMW** (Unicode) and **CBEM\_GETITEMA** (ANSI)</span></span><br/>                 |



 

 





