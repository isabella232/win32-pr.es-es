---
title: Código de notificación de LVN_INCREMENTALSEARCH (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que se ha iniciado una búsqueda incremental. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658420"
---
# <a name="lvn_incrementalsearch-notification-code"></a><span data-ttu-id="8c8e1-105">LVN \_ código de notificación INCREMENTALSEARCH</span><span class="sxs-lookup"><span data-stu-id="8c8e1-105">LVN\_INCREMENTALSEARCH notification code</span></span>

<span data-ttu-id="8c8e1-106">Notifica a la ventana primaria de un control de vista de lista que se ha iniciado una búsqueda incremental.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-106">Notifies a list-view control's parent window that an incremental search has started.</span></span> <span data-ttu-id="8c8e1-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8c8e1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8c8e1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c8e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c8e1-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c8e1-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c8e1-110">Puntero a una estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) que describe el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-110">Pointer to a [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that describes the notification code.</span></span> <span data-ttu-id="8c8e1-111">El autor de la llamada es responsable de la asignación de esta estructura, incluidas las estructuras [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) y [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenidas.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) and [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structures.</span></span> <span data-ttu-id="8c8e1-112">Establezca los miembros de la estructura **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="8c8e1-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="8c8e1-113">El miembro de **código** debe establecerse en LVN \_ INCREMENTALSEARCH.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-113">The **code** member must be set to LVN\_INCREMENTALSEARCH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c8e1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c8e1-114">Return value</span></span>

<span data-ttu-id="8c8e1-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c8e1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c8e1-116">Remarks</span></span>

<span data-ttu-id="8c8e1-117">El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .</span><span class="sxs-lookup"><span data-stu-id="8c8e1-117">The notification receiver casts *lParam* to retrieve the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span> <span data-ttu-id="8c8e1-118">El parámetro *wParam* contiene el identificador del control que envía este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-118">The *wParam* parameter contains the ID of the control that sends this notification code.</span></span>

<span data-ttu-id="8c8e1-119">Este código de notificación proporciona a una aplicación (o al receptor de notificaciones) la oportunidad de personalizar una búsqueda incremental.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-119">This notification code gives an application (or the notification receiver) the opportunity to customize an incremental search.</span></span> <span data-ttu-id="8c8e1-120">Por ejemplo, si los elementos de búsqueda son numéricos, la aplicación puede realizar una búsqueda numérica en lugar de una búsqueda de cadena.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-120">For example, if the search items are numeric, the application can perform a numerical search instead of a string search.</span></span>

<span data-ttu-id="8c8e1-121">La aplicación establece el miembro **lParam** de la estructura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) incluida en la estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) en el resultado de la búsqueda, o en otro valor definido por la aplicación para que no se realice la búsqueda e indique al control cómo proceder.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-121">The application sets the **lParam** member of the [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure contained in [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure  to the result of the search, or to another application defined value to fail the search and indicate to the control how to proceed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c8e1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c8e1-122">Requirements</span></span>



| <span data-ttu-id="8c8e1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c8e1-123">Requirement</span></span> | <span data-ttu-id="8c8e1-124">Value</span><span class="sxs-lookup"><span data-stu-id="8c8e1-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8e1-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c8e1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8c8e1-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8c8e1-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8c8e1-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c8e1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8c8e1-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c8e1-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c8e1-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c8e1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c8e1-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c8e1-130"><dt>Commctrl.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c8e1-131">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8c8e1-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8c8e1-132">**LVN \_ INCREMENTALSEARCHW** (Unicode) y **LVN \_ INCREMENTALSEARCHA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8c8e1-132">**LVN\_INCREMENTALSEARCHW** (Unicode) and **LVN\_INCREMENTALSEARCHA** (ANSI)</span></span><br/> |



 

 





