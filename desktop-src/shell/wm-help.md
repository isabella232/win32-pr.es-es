---
description: Indica que el usuario presionó la tecla F1.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: Mensaje de WM_HELP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985391"
---
# <a name="wm_help-message"></a><span data-ttu-id="bbdb3-103">Mensaje de ayuda de WM \_</span><span class="sxs-lookup"><span data-stu-id="bbdb3-103">WM\_HELP message</span></span>

<span data-ttu-id="bbdb3-104">Indica que el usuario presionó la tecla F1.</span><span class="sxs-lookup"><span data-stu-id="bbdb3-104">Indicates that the user pressed the F1 key.</span></span> <span data-ttu-id="bbdb3-105">Si un menú está activo cuando se presiona F1, **la \_ ayuda de WM** se envía a la ventana asociada al menú; de lo contrario, la **\_ ayuda de WM** se envía a la ventana que tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="bbdb3-105">If a menu is active when F1 is pressed, **WM\_HELP** is sent to the window associated with the menu; otherwise, **WM\_HELP** is sent to the window that has the keyboard focus.</span></span> <span data-ttu-id="bbdb3-106">Si ninguna ventana tiene el foco de teclado, la **\_ ayuda de WM** se envía a la ventana activa actualmente.</span><span class="sxs-lookup"><span data-stu-id="bbdb3-106">If no window has the keyboard focus, **WM\_HELP** is sent to the currently active window.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbdb3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bbdb3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbdb3-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbdb3-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbdb3-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bbdb3-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bbdb3-110">*lphi*</span><span class="sxs-lookup"><span data-stu-id="bbdb3-110">*lphi*</span></span> 
</dt> <dd>

<span data-ttu-id="bbdb3-111">La dirección de una estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contiene información sobre el elemento de menú, el control, el cuadro de diálogo o la ventana para la que se solicita ayuda.</span><span class="sxs-lookup"><span data-stu-id="bbdb3-111">The address of a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains information about the menu item, control, dialog box, or window for which Help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbdb3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbdb3-112">Return value</span></span>

<span data-ttu-id="bbdb3-113">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="bbdb3-113">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbdb3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbdb3-114">Remarks</span></span>

<span data-ttu-id="bbdb3-115">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pasa **la \_ ayuda de WM** a la ventana primaria de una ventana secundaria o al propietario de una ventana de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="bbdb3-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes **WM\_HELP** to the parent window of a child window or to the owner of a top-level window.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbdb3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbdb3-116">Requirements</span></span>



| <span data-ttu-id="bbdb3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbdb3-117">Requirement</span></span> | <span data-ttu-id="bbdb3-118">Value</span><span class="sxs-lookup"><span data-stu-id="bbdb3-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bbdb3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbdb3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bbdb3-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bbdb3-120">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bbdb3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbdb3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bbdb3-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bbdb3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bbdb3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbdb3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbdb3-124"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbdb3-124"><dt>Winuser.h</dt></span></span> </dl> |



 

 
