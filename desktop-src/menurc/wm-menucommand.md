---
title: Mensaje de WM_MENUCOMMAND (Winuser. h)
description: Se envía cuando el usuario realiza una selección en un menú.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422623"
---
# <a name="wm_menucommand-message"></a><span data-ttu-id="d2634-104">\_Mensaje MENUCOMMAND de WM</span><span class="sxs-lookup"><span data-stu-id="d2634-104">WM\_MENUCOMMAND message</span></span>

<span data-ttu-id="d2634-105">Se envía cuando el usuario realiza una selección en un menú.</span><span class="sxs-lookup"><span data-stu-id="d2634-105">Sent when the user makes a selection from a menu.</span></span>


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a><span data-ttu-id="d2634-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2634-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2634-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2634-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2634-108">Índice de base cero del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d2634-108">The zero-based index of the item selected.</span></span>

</dd> <dt>

<span data-ttu-id="d2634-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2634-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2634-110">Identificador del menú para el elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d2634-110">A handle to the menu for the item selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2634-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2634-111">Remarks</span></span>

<span data-ttu-id="d2634-112">El **mensaje \_ MENUCOMMAND de WM** le proporciona un identificador para el menú, de modo que pueda tener acceso a los datos de menú en la estructura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) y también le proporcionará el índice del elemento seleccionado, que es normalmente lo que necesitan las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d2634-112">The **WM\_MENUCOMMAND** message gives you a handle to the menu so you can access the menu data in the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure and also gives you the index of the selected item, which is typically what applications need.</span></span> <span data-ttu-id="d2634-113">En cambio, el mensaje de [**\_ comando de WM**](wm-command.md) le proporciona el identificador del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="d2634-113">In contrast, the [**WM\_COMMAND**](wm-command.md) message gives you the menu item identifier.</span></span>

<span data-ttu-id="d2634-114">El **mensaje \_ MENUCOMMAND de WM** solo se envía para los menús que se definen con la marca **mns \_ NOTIFYBYPOS** establecida en el miembro **dwStyle** de la estructura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) .</span><span class="sxs-lookup"><span data-stu-id="d2634-114">The **WM\_MENUCOMMAND** message is sent only for menus that are defined with the **MNS\_NOTIFYBYPOS** flag set in the **dwStyle** member of the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2634-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2634-115">Requirements</span></span>



| <span data-ttu-id="d2634-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2634-116">Requirement</span></span> | <span data-ttu-id="d2634-117">Value</span><span class="sxs-lookup"><span data-stu-id="d2634-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2634-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2634-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2634-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d2634-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d2634-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2634-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2634-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2634-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d2634-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2634-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2634-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2634-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2634-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2634-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2634-125">Información general sobre menús</span><span class="sxs-lookup"><span data-stu-id="d2634-125">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





