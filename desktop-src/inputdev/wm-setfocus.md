---
title: Mensaje de WM_SETFOCUS (Winuser. h)
description: Se envía a una ventana una vez que ha obtenido el foco de teclado.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- Entrada de mouse y teclado de mensaje de WM_SETFOCUS
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b304d7f7739ce551c1efc6a1d33a934c48dc8b4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492652"
---
# <a name="wm_setfocus-message"></a><span data-ttu-id="2341e-104">Mensaje de SETFOCUS de WM \_</span><span class="sxs-lookup"><span data-stu-id="2341e-104">WM\_SETFOCUS message</span></span>

<span data-ttu-id="2341e-105">Se envía a una ventana una vez que ha obtenido el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="2341e-105">Sent to a window after it has gained the keyboard focus.</span></span>


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a><span data-ttu-id="2341e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2341e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2341e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2341e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2341e-108">Identificador de la ventana que ha perdido el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="2341e-108">A handle to the window that has lost the keyboard focus.</span></span> <span data-ttu-id="2341e-109">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2341e-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2341e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2341e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2341e-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2341e-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2341e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2341e-112">Return value</span></span>

<span data-ttu-id="2341e-113">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="2341e-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="2341e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2341e-114">Remarks</span></span>

<span data-ttu-id="2341e-115">Para mostrar un símbolo de intercalación, una aplicación debe llamar a las funciones de símbolo de intercalación apropiadas cuando recibe el mensaje de **\_ SETFOCUS de WM** .</span><span class="sxs-lookup"><span data-stu-id="2341e-115">To display a caret, an application should call the appropriate caret functions when it receives the **WM\_SETFOCUS** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2341e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2341e-116">Requirements</span></span>



| <span data-ttu-id="2341e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2341e-117">Requirement</span></span> | <span data-ttu-id="2341e-118">Value</span><span class="sxs-lookup"><span data-stu-id="2341e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2341e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2341e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2341e-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2341e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2341e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2341e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2341e-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2341e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2341e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2341e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2341e-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2341e-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2341e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2341e-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="2341e-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2341e-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2341e-127">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="2341e-127">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="2341e-128">**KILLFOCUS de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2341e-128">**WM\_KILLFOCUS**</span></span>](wm-killfocus.md)
</dt> <dt>

<span data-ttu-id="2341e-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="2341e-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2341e-130">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="2341e-130">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

