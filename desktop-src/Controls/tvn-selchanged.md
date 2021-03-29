---
title: Código de notificación de TVN_SELCHANGED (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que la selección ha cambiado de un elemento a otro. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a564ec039e179d03dda9edc19d6de3412cd5361a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905581"
---
# <a name="tvn_selchanged-notification-code"></a><span data-ttu-id="3b8af-105">Código de notificación de SELCHANGED de TVN \_</span><span class="sxs-lookup"><span data-stu-id="3b8af-105">TVN\_SELCHANGED notification code</span></span>

<span data-ttu-id="3b8af-106">Notifica a la ventana primaria de un control de vista de árbol que la selección ha cambiado de un elemento a otro.</span><span class="sxs-lookup"><span data-stu-id="3b8af-106">Notifies a tree-view control's parent window that the selection has changed from one item to another.</span></span> <span data-ttu-id="3b8af-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3b8af-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="3b8af-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b8af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b8af-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b8af-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b8af-110">Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="3b8af-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="3b8af-111">Los miembros **itemOld** y **itemNew** de la estructura **NMTREEVIEW** son estructuras [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contienen información sobre el elemento seleccionado anteriormente y el elemento recién seleccionado.</span><span class="sxs-lookup"><span data-stu-id="3b8af-111">The **itemOld** and **itemNew** members of the **NMTREEVIEW** structure are [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structures that contain information about the previously selected item and the newly selected item.</span></span> <span data-ttu-id="3b8af-112">Solo los miembros **Mask**, **hItem**, **State** e **lParam** de estas estructuras son válidos.</span><span class="sxs-lookup"><span data-stu-id="3b8af-112">Only the **mask**, **hItem**, **state**, and **lParam** members of these structures are valid.</span></span> <span data-ttu-id="3b8af-113">Los miembros de **stateMask** de las estructuras **TVITEM** especificados por **itemOld** y **itemNew** no están definidos en la entrada.</span><span class="sxs-lookup"><span data-stu-id="3b8af-113">The **stateMask** members of the **TVITEM** structures specified by **itemOld** and **itemNew** are undefined on input.</span></span> <span data-ttu-id="3b8af-114">El miembro de **acción** de la estructura **NMTREEVIEW** indica el tipo de acción que provocó el cambio de la selección.</span><span class="sxs-lookup"><span data-stu-id="3b8af-114">The **action** member of the **NMTREEVIEW** structure indicates the type of action that caused the selection to change.</span></span> <span data-ttu-id="3b8af-115">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="3b8af-115">It can be one of the following values:</span></span>



| <span data-ttu-id="3b8af-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b8af-116">Requirement</span></span> | <span data-ttu-id="3b8af-117">Value</span><span class="sxs-lookup"><span data-stu-id="3b8af-117">Value</span></span> |
|-----------------|-------------------|
| <span data-ttu-id="3b8af-118">TVC \_ BYKEYBOARD</span><span class="sxs-lookup"><span data-stu-id="3b8af-118">TVC\_BYKEYBOARD</span></span> | <span data-ttu-id="3b8af-119">Mediante una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="3b8af-119">By a keystroke.</span></span>   |
| <span data-ttu-id="3b8af-120">TVC \_ BYMOUSE</span><span class="sxs-lookup"><span data-stu-id="3b8af-120">TVC\_BYMOUSE</span></span>    | <span data-ttu-id="3b8af-121">Con un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="3b8af-121">By a mouse click.</span></span> |
| <span data-ttu-id="3b8af-122">TVC \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="3b8af-122">TVC\_UNKNOWN</span></span>    | <span data-ttu-id="3b8af-123">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="3b8af-123">Unknown.</span></span>          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b8af-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b8af-124">Return value</span></span>

<span data-ttu-id="3b8af-125">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="3b8af-125">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b8af-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b8af-126">Requirements</span></span>



| <span data-ttu-id="3b8af-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b8af-127">Requirement</span></span> | <span data-ttu-id="3b8af-128">Value</span><span class="sxs-lookup"><span data-stu-id="3b8af-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8af-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b8af-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3b8af-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3b8af-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b8af-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b8af-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3b8af-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b8af-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b8af-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b8af-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b8af-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b8af-134"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3b8af-135">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="3b8af-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3b8af-136">**TVN \_ SELCHANGEDW** (Unicode) y **TVN \_ SELCHANGEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3b8af-136">**TVN\_SELCHANGEDW** (Unicode) and **TVN\_SELCHANGEDA** (ANSI)</span></span><br/>             |



 

 





