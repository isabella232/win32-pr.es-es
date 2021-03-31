---
description: Se envía a un icono cuando el usuario solicita que la ventana se restaure a su tamaño y posición anteriores.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: Mensaje de WM_QUERYOPEN (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082669"
---
# <a name="wm_queryopen-message"></a><span data-ttu-id="0a19a-103">Mensaje de QUERYOPEN de WM \_</span><span class="sxs-lookup"><span data-stu-id="0a19a-103">WM\_QUERYOPEN message</span></span>

<span data-ttu-id="0a19a-104">Se envía a un icono cuando el usuario solicita que la ventana se restaure a su tamaño y posición anteriores.</span><span class="sxs-lookup"><span data-stu-id="0a19a-104">Sent to an icon when the user requests that the window be restored to its previous size and position.</span></span>

<span data-ttu-id="0a19a-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0a19a-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYOPEN                    0x0013
```



## <a name="parameters"></a><span data-ttu-id="0a19a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a19a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a19a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a19a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a19a-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0a19a-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0a19a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a19a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a19a-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0a19a-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a19a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a19a-111">Return value</span></span>

<span data-ttu-id="0a19a-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="0a19a-112">Type: **LRESULT**</span></span>

<span data-ttu-id="0a19a-113">Si se puede abrir el icono, una aplicación que procese este mensaje debe devolver **true**; de lo contrario, debería devolver **false** para evitar que se abra el icono.</span><span class="sxs-lookup"><span data-stu-id="0a19a-113">If the icon can be opened, an application that processes this message should return **TRUE**; otherwise, it should return **FALSE** to prevent the icon from being opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a19a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a19a-114">Remarks</span></span>

<span data-ttu-id="0a19a-115">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="0a19a-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE**.</span></span>

<span data-ttu-id="0a19a-116">Al procesar este mensaje, la aplicación no debe realizar ninguna acción que provoque un cambio de activación o foco (por ejemplo, crear un cuadro de diálogo).</span><span class="sxs-lookup"><span data-stu-id="0a19a-116">While processing this message, the application should not perform any action that would cause an activation or focus change (for example, creating a dialog box).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a19a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a19a-117">Requirements</span></span>



| <span data-ttu-id="0a19a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a19a-118">Requirement</span></span> | <span data-ttu-id="0a19a-119">Value</span><span class="sxs-lookup"><span data-stu-id="0a19a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a19a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a19a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0a19a-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0a19a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0a19a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a19a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0a19a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a19a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0a19a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a19a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a19a-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a19a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a19a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a19a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a19a-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0a19a-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0a19a-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="0a19a-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="0a19a-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0a19a-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0a19a-130">Windows</span><span class="sxs-lookup"><span data-stu-id="0a19a-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
