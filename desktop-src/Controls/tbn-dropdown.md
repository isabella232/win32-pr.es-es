---
title: Código de notificación de TBN_DROPDOWN (commctrl. h)
description: Se envía por un control de barra de herramientas cuando el usuario hace clic en un botón desplegable. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- TBN_DROPDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996207"
---
# <a name="tbn_dropdown-notification-code"></a><span data-ttu-id="03268-105">\_Código de notificación de desplegable TBN</span><span class="sxs-lookup"><span data-stu-id="03268-105">TBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="03268-106">Se envía por un control de barra de herramientas cuando el usuario hace clic en un botón desplegable.</span><span class="sxs-lookup"><span data-stu-id="03268-106">Sent by a toolbar control when the user clicks a dropdown button.</span></span> <span data-ttu-id="03268-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="03268-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="03268-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03268-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03268-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03268-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03268-110">Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="03268-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="03268-111">En este código de notificación, solo son válidos los miembros **HDR** y **iItem** de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="03268-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03268-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03268-112">Return value</span></span>

<span data-ttu-id="03268-113">Devuelve uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="03268-113">Returns one of the following values:</span></span>



| <span data-ttu-id="03268-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="03268-114">Return code</span></span>                                                                                          | <span data-ttu-id="03268-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="03268-115">Description</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="03268-116"><dt>**\_valor predeterminado de TBDDRET**</dt></span><span class="sxs-lookup"><span data-stu-id="03268-116"><dt>**TBDDRET\_DEFAULT**</dt></span></span> </dl>      | <span data-ttu-id="03268-117">Se controló la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="03268-117">The drop-down was handled.</span></span><br/>                                             |
| <dl> <span data-ttu-id="03268-118"><dt>**TBDDRET \_ NOdefault**</dt></span><span class="sxs-lookup"><span data-stu-id="03268-118"><dt>**TBDDRET\_NODEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="03268-119">No se controló la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="03268-119">The drop-down was not handled.</span></span><br/>                                         |
| <dl> <span data-ttu-id="03268-120"><dt>**TBDDRET \_ TREATPRESSED**</dt></span><span class="sxs-lookup"><span data-stu-id="03268-120"><dt>**TBDDRET\_TREATPRESSED**</dt></span></span> </dl> | <span data-ttu-id="03268-121">La lista desplegable se ha controlado, pero se trata el botón como un botón normal.</span><span class="sxs-lookup"><span data-stu-id="03268-121">The drop-down was handled, but treat the button like a regular button.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="03268-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03268-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="03268-123">Los botones desplegables pueden ser sin formato (estilo [**\_ desplegable BTNS**](toolbar-control-and-button-styles.md) ), mostrar una flecha junto a la imagen del botón (estilo [**BTNS \_ WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) ) o mostrar una flecha que esté separada de la imagen (estilo [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="03268-123">Dropdown buttons can be plain ([**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style), display an arrow next to the button image ([**BTNS\_WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) style), or display an arrow that is separated from the image ([**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style).</span></span> <span data-ttu-id="03268-124">Si se usa una flecha separada, \_ la lista desplegable TBN se envía solo si el usuario hace clic en la parte de la flecha del botón.</span><span class="sxs-lookup"><span data-stu-id="03268-124">If a separated arrow is used, TBN\_DROPDOWN is sent only if the user clicks the arrow portion of the button.</span></span> <span data-ttu-id="03268-125">Si el usuario hace clic en la parte principal del botón, se envía un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) con el identificador del botón, al igual que con un botón estándar.</span><span class="sxs-lookup"><span data-stu-id="03268-125">If the user clicks the main part of the button, a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with button's ID is sent, just as with a standard button.</span></span> <span data-ttu-id="03268-126">En el caso de los otros dos estilos del botón desplegable, \_ se envía la lista desplegable TBN cuando el usuario hace clic en cualquier parte del botón.</span><span class="sxs-lookup"><span data-stu-id="03268-126">For the other two styles of dropdown button, TBN\_DROPDOWN is sent when the user clicks any part of the button.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="03268-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03268-127">Requirements</span></span>



| <span data-ttu-id="03268-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="03268-128">Requirement</span></span> | <span data-ttu-id="03268-129">Value</span><span class="sxs-lookup"><span data-stu-id="03268-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03268-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03268-130">Minimum supported client</span></span><br/> | <span data-ttu-id="03268-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="03268-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03268-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03268-132">Minimum supported server</span></span><br/> | <span data-ttu-id="03268-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="03268-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03268-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03268-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="03268-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="03268-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

