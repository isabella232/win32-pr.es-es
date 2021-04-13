---
title: Mensaje de WM_UNINITMENUPOPUP (Winuser. h)
description: Se envía cuando se destruye un menú desplegable o un submenú.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535542"
---
# <a name="wm_uninitmenupopup-message"></a><span data-ttu-id="a3224-104">Mensaje de UNINITMENUPOPUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="a3224-104">WM\_UNINITMENUPOPUP message</span></span>

<span data-ttu-id="a3224-105">Se envía cuando se destruye un menú desplegable o un submenú.</span><span class="sxs-lookup"><span data-stu-id="a3224-105">Sent when a drop-down menu or submenu has been destroyed.</span></span>


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a><span data-ttu-id="a3224-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3224-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3224-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3224-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3224-108">Identificador del menú.</span><span class="sxs-lookup"><span data-stu-id="a3224-108">A handle to the menu</span></span>

</dd> <dt>

<span data-ttu-id="a3224-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3224-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3224-110">La palabra de orden superior identifica el menú que se ha destruido.</span><span class="sxs-lookup"><span data-stu-id="a3224-110">The high-order word identifies the menu that was destroyed.</span></span> <span data-ttu-id="a3224-111">Actualmente, este parámetro solo puede ser **MF \_ SYSMENU** (el menú ventana).</span><span class="sxs-lookup"><span data-stu-id="a3224-111">Currently, this parameter can only be **MF\_SYSMENU** (the window menu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3224-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3224-112">Remarks</span></span>

<span data-ttu-id="a3224-113">Si una aplicación recibe un mensaje de [**\_ INITMENUPOPUP de WM**](wm-initmenupopup.md) , recibirá un mensaje de **\_ UNINITMENUPOPUP de WM** .</span><span class="sxs-lookup"><span data-stu-id="a3224-113">If an application receives a [**WM\_INITMENUPOPUP**](wm-initmenupopup.md) message, it will receive a **WM\_UNINITMENUPOPUP** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3224-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3224-114">Requirements</span></span>



| <span data-ttu-id="a3224-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3224-115">Requirement</span></span> | <span data-ttu-id="a3224-116">Value</span><span class="sxs-lookup"><span data-stu-id="a3224-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3224-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3224-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a3224-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a3224-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a3224-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3224-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a3224-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3224-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a3224-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3224-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3224-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3224-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3224-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3224-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3224-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a3224-124">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="a3224-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a3224-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a3224-126">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a3224-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a3224-127">Menús</span><span class="sxs-lookup"><span data-stu-id="a3224-127">Menus</span></span>](menus.md)
</dt> </dl>

 

