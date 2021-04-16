---
title: Código de notificación de TVN_GETDISPINFO (commctrl. h)
description: Solicita que la ventana primaria de un control de vista de árbol proporcione la información necesaria para mostrar u ordenar un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534215"
---
# <a name="tvn_getdispinfo-notification-code"></a><span data-ttu-id="1729a-105">Código de notificación de GETDISPINFO de TVN \_</span><span class="sxs-lookup"><span data-stu-id="1729a-105">TVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="1729a-106">Solicita que la ventana primaria de un control de vista de árbol proporcione la información necesaria para mostrar u ordenar un elemento.</span><span class="sxs-lookup"><span data-stu-id="1729a-106">Requests that a tree-view control's parent window provide information needed to display or sort an item.</span></span> <span data-ttu-id="1729a-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1729a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="1729a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1729a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1729a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1729a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1729a-110">Puntero a una estructura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="1729a-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="1729a-111">El miembro del **elemento** es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cuyos miembros **Mask**, **hItem**, **State** e **lParam** especifican el tipo de información necesaria.</span><span class="sxs-lookup"><span data-stu-id="1729a-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **mask**, **hItem**, **state**, and **lParam** members specify the type of information required.</span></span> <span data-ttu-id="1729a-112">Debe rellenar los miembros de la estructura con la información adecuada.</span><span class="sxs-lookup"><span data-stu-id="1729a-112">You must fill the members of the structure with the appropriate information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1729a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1729a-113">Return value</span></span>

<span data-ttu-id="1729a-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1729a-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="1729a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1729a-115">Remarks</span></span>

<span data-ttu-id="1729a-116">Este código de notificación se envía en las siguientes circunstancias:</span><span class="sxs-lookup"><span data-stu-id="1729a-116">This notification code is sent under the following circumstances:</span></span>

-   <span data-ttu-id="1729a-117">Si el miembro **miembros pszText** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el \_ valor LPSTR TEXTCALLBACK, el control envía este código de notificación para recuperar el texto del elemento.</span><span class="sxs-lookup"><span data-stu-id="1729a-117">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification code to retrieve the item's text.</span></span> <span data-ttu-id="1729a-118">En este caso, el miembro de **máscara** de *lParam* tendrá establecido el \_ indicador de texto TVIF.</span><span class="sxs-lookup"><span data-stu-id="1729a-118">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>
-   <span data-ttu-id="1729a-119">Si el miembro **iImage** o **iSelectedImage** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el \_ valor I IMAGECALLBACK, el control envía este código de notificación para recuperar el índice de los iconos de un elemento en la lista de imágenes del control.</span><span class="sxs-lookup"><span data-stu-id="1729a-119">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification code to retrieve the index of an item's icons in the control's image list.</span></span> <span data-ttu-id="1729a-120">En este caso, si el elemento está seleccionado, el miembro de **máscara** de *lParam* tendrá la \_ marca TVIF SELECTEDIMAGE establecida.</span><span class="sxs-lookup"><span data-stu-id="1729a-120">In this case, if the item is selected, the **mask** member of *lParam* will have the TVIF\_SELECTEDIMAGE flag set.</span></span> <span data-ttu-id="1729a-121">Si el elemento no está seleccionado, el miembro de **máscara** de *lParam* tendrá establecido el \_ indicador de imagen TVIF.</span><span class="sxs-lookup"><span data-stu-id="1729a-121">If the item is not selected, the **mask** member of *lParam* will have the TVIF\_IMAGE flag set.</span></span>
-   <span data-ttu-id="1729a-122">Si el miembro **cChildren** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el \_ valor I CHILDRENCALLBACK, el control envía este código de notificación para recuperar un valor que indica si el elemento tiene elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="1729a-122">If the **cChildren** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_CHILDRENCALLBACK value, the control sends this notification code to retrieve a value that indicates whether the item has child items.</span></span> <span data-ttu-id="1729a-123">En este caso, el miembro de **máscara** de *lParam* tendrá establecido el \_ marcador de TVIF Children.</span><span class="sxs-lookup"><span data-stu-id="1729a-123">In this case, the **mask** member of *lParam* will have the TVIF\_CHILDREN flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="1729a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1729a-124">Requirements</span></span>



| <span data-ttu-id="1729a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1729a-125">Requirement</span></span> | <span data-ttu-id="1729a-126">Value</span><span class="sxs-lookup"><span data-stu-id="1729a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1729a-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1729a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1729a-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1729a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1729a-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1729a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1729a-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1729a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1729a-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1729a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1729a-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1729a-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1729a-133">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1729a-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1729a-134">**TVN \_ GETDISPINFOW** (Unicode) y **TVN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1729a-134">**TVN\_GETDISPINFOW** (Unicode) and **TVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="1729a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1729a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1729a-136">TVN \_ SETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="1729a-136">TVN\_SETDISPINFO</span></span>](tvn-setdispinfo.md)
</dt> </dl>

 

 





