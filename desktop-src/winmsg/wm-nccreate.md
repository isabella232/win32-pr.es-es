---
description: Se envía antes del mensaje de creación de WM \_ cuando se crea una ventana por primera vez.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: Mensaje de WM_NCCREATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716043"
---
# <a name="wm_nccreate-message"></a><span data-ttu-id="8d5ff-103">Mensaje de NCCREATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="8d5ff-103">WM\_NCCREATE message</span></span>

<span data-ttu-id="8d5ff-104">Se envía antes del mensaje de [**\_ creación de WM**](wm-create.md) cuando se crea una ventana por primera vez.</span><span class="sxs-lookup"><span data-stu-id="8d5ff-104">Sent prior to the [**WM\_CREATE**](wm-create.md) message when a window is first created.</span></span>

<span data-ttu-id="8d5ff-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8d5ff-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a><span data-ttu-id="8d5ff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d5ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d5ff-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d5ff-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d5ff-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8d5ff-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8d5ff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d5ff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d5ff-110">Puntero a la estructura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) que contiene información sobre la ventana que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="8d5ff-110">A pointer to the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span> <span data-ttu-id="8d5ff-111">Los miembros de **CREATESTRUCT** son idénticos a los parámetros de la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="8d5ff-111">The members of **CREATESTRUCT** are identical to the parameters of the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d5ff-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d5ff-112">Return value</span></span>

<span data-ttu-id="8d5ff-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="8d5ff-113">Type: **LRESULT**</span></span>

<span data-ttu-id="8d5ff-114">Si una aplicación procesa este mensaje, debe devolver **true** para continuar con la creación de la ventana.</span><span class="sxs-lookup"><span data-stu-id="8d5ff-114">If an application processes this message, it should return **TRUE** to continue creation of the window.</span></span> <span data-ttu-id="8d5ff-115">Si la aplicación devuelve **false**, la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) devolverá un identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="8d5ff-115">If the application returns **FALSE**, the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function will return a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d5ff-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d5ff-116">Requirements</span></span>



| <span data-ttu-id="8d5ff-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d5ff-117">Requirement</span></span> | <span data-ttu-id="8d5ff-118">Value</span><span class="sxs-lookup"><span data-stu-id="8d5ff-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5ff-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d5ff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d5ff-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8d5ff-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8d5ff-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d5ff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d5ff-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8d5ff-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8d5ff-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d5ff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d5ff-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d5ff-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d5ff-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d5ff-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="8d5ff-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8d5ff-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8d5ff-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="8d5ff-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="8d5ff-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="8d5ff-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="8d5ff-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="8d5ff-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="8d5ff-130">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="8d5ff-130">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="8d5ff-131">**creación de WM \_**</span><span class="sxs-lookup"><span data-stu-id="8d5ff-131">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

<span data-ttu-id="8d5ff-132">**Vista**</span><span class="sxs-lookup"><span data-stu-id="8d5ff-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8d5ff-133">Windows</span><span class="sxs-lookup"><span data-stu-id="8d5ff-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
