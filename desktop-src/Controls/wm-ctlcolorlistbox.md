---
title: Mensaje de WM_CTLCOLORLISTBOX (Winuser. h)
description: Se envía a la ventana primaria de un cuadro de lista antes de que el sistema dibuje el cuadro de lista. Al responder a este mensaje, la ventana primaria puede establecer los colores de texto y de fondo del cuadro de lista utilizando el identificador de contexto de dispositivo de pantalla especificado.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- WM_CTLCOLORLISTBOX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949af76bd05aa9ad3a3e720c89be33cfe76ed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150227"
---
# <a name="wm_ctlcolorlistbox-message"></a><span data-ttu-id="575dc-105">Mensaje de CTLCOLORLISTBOX de WM \_</span><span class="sxs-lookup"><span data-stu-id="575dc-105">WM\_CTLCOLORLISTBOX message</span></span>

<span data-ttu-id="575dc-106">Se envía a la ventana primaria de un cuadro de lista antes de que el sistema dibuje el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="575dc-106">Sent to the parent window of a list box before the system draws the list box.</span></span> <span data-ttu-id="575dc-107">Al responder a este mensaje, la ventana primaria puede establecer los colores de texto y de fondo del cuadro de lista utilizando el identificador de contexto de dispositivo de pantalla especificado.</span><span class="sxs-lookup"><span data-stu-id="575dc-107">By responding to this message, the parent window can set the text and background colors of the list box by using the specified display device context handle.</span></span>


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="575dc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="575dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="575dc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="575dc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="575dc-110">Identificador del contexto de dispositivo para el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="575dc-110">Handle to the device context for the list box.</span></span>

</dd> <dt>

<span data-ttu-id="575dc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="575dc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="575dc-112">Identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="575dc-112">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="575dc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="575dc-113">Return value</span></span>

<span data-ttu-id="575dc-114">Si una aplicación procesa este mensaje, debe devolver un identificador a un pincel.</span><span class="sxs-lookup"><span data-stu-id="575dc-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="575dc-115">El sistema utiliza el pincel para pintar el fondo del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="575dc-115">The system uses the brush to paint the background of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="575dc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="575dc-116">Remarks</span></span>

<span data-ttu-id="575dc-117">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="575dc-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the list box.</span></span>

<span data-ttu-id="575dc-118">El mensaje de **\_ CTLCOLORLISTBOX de WM** nunca se envía entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="575dc-118">The **WM\_CTLCOLORLISTBOX** message is never sent between threads.</span></span> <span data-ttu-id="575dc-119">Solo se envía dentro de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="575dc-119">It is sent only within one thread.</span></span>

<span data-ttu-id="575dc-120">Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado a **int \_ ptr** y devolver el valor directamente.</span><span class="sxs-lookup"><span data-stu-id="575dc-120">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="575dc-121">Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="575dc-121">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="575dc-122">Se omite el valor de **DWL \_ MSGRESULT** establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="575dc-122">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="575dc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="575dc-123">Requirements</span></span>



| <span data-ttu-id="575dc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="575dc-124">Requirement</span></span> | <span data-ttu-id="575dc-125">Value</span><span class="sxs-lookup"><span data-stu-id="575dc-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="575dc-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="575dc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="575dc-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="575dc-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="575dc-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="575dc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="575dc-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="575dc-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="575dc-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="575dc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="575dc-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="575dc-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="575dc-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="575dc-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="575dc-133">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="575dc-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="575dc-134">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="575dc-134">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="575dc-135">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="575dc-135">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="575dc-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="575dc-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

