---
title: Mensaje de WM_MENURBUTTONUP (Winuser. h)
description: Se envía cuando el usuario suelta el botón secundario del mouse mientras el cursor está en un elemento de menú.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359868"
---
# <a name="wm_menurbuttonup-message"></a><span data-ttu-id="7afc3-104">Mensaje de MENURBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="7afc3-104">WM\_MENURBUTTONUP message</span></span>

<span data-ttu-id="7afc3-105">Se envía cuando el usuario suelta el botón secundario del mouse mientras el cursor está en un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="7afc3-105">Sent when the user releases the right mouse button while the cursor is on a menu item.</span></span>


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a><span data-ttu-id="7afc3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7afc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7afc3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7afc3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7afc3-108">Índice de base cero del elemento de menú en el que se liberó el botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="7afc3-108">The zero-based index of the menu item on which the right mouse button was released.</span></span>

</dd> <dt>

<span data-ttu-id="7afc3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7afc3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7afc3-110">Identificador del menú que contiene el elemento.</span><span class="sxs-lookup"><span data-stu-id="7afc3-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7afc3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7afc3-111">Remarks</span></span>

<span data-ttu-id="7afc3-112">El mensaje de **\_ MENURBUTTONUP de WM** permite a las aplicaciones proporcionar un menú contextual también conocido como menú contextual para el elemento de menú especificado en este mensaje.</span><span class="sxs-lookup"><span data-stu-id="7afc3-112">The **WM\_MENURBUTTONUP** message allows applications to provide a context-sensitive menu also known as a shortcut menu for the menu item specified in this message.</span></span> <span data-ttu-id="7afc3-113">Para mostrar un menú contextual de un elemento de menú, llame a la función [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) con el **\_ RECURSE de TPM**.</span><span class="sxs-lookup"><span data-stu-id="7afc3-113">To display a context-sensitive menu for a menu item, call the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function with **TPM\_RECURSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7afc3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7afc3-114">Requirements</span></span>



| <span data-ttu-id="7afc3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7afc3-115">Requirement</span></span> | <span data-ttu-id="7afc3-116">Value</span><span class="sxs-lookup"><span data-stu-id="7afc3-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7afc3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7afc3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7afc3-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7afc3-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7afc3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7afc3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7afc3-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7afc3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7afc3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7afc3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7afc3-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7afc3-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7afc3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7afc3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7afc3-124">Información general sobre menús</span><span class="sxs-lookup"><span data-stu-id="7afc3-124">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





