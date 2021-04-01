---
title: Código de notificación de CDN_HELP (commdlg. h)
description: Enviado por un cuadro de diálogo abrir o guardar como del explorador cuando el usuario hace clic en el botón ayuda.
ms.assetid: 18ee86b2-3446-4de4-a47a-2e44e677f4f7
keywords:
- CDN_HELP cuadros de diálogo código de notificación
topic_type:
- apiref
api_name:
- CDN_HELP
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c73b690b1ac522a985ae121413804c4385e0f2cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150831"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="f21f4-104">Código de notificación de ayuda de CDN \_</span><span class="sxs-lookup"><span data-stu-id="f21f4-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="f21f4-105">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f21f4-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="f21f4-106">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="f21f4-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="f21f4-107">Enviado por un cuadro de diálogo **abrir** o **Guardar como** del explorador cuando el usuario hace clic en el botón **ayuda** .</span><span class="sxs-lookup"><span data-stu-id="f21f4-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="f21f4-108">El procedimiento de enlace de [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje de [**\_ notificación de WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f21f4-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="f21f4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f21f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f21f4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f21f4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f21f4-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f21f4-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f21f4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f21f4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f21f4-113">Puntero a una estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="f21f4-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="f21f4-114">La estructura **imnotify** contiene una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cuyo miembro de **código** indica el mensaje de notificación de la **\_ ayuda de CDN** .</span><span class="sxs-lookup"><span data-stu-id="f21f4-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f21f4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f21f4-115">Return value</span></span>

<span data-ttu-id="f21f4-116">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f21f4-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f21f4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f21f4-117">Remarks</span></span>

<span data-ttu-id="f21f4-118">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el valor del **\_ Explorador OFN** .</span><span class="sxs-lookup"><span data-stu-id="f21f4-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f21f4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f21f4-119">Requirements</span></span>



| <span data-ttu-id="f21f4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f21f4-120">Requirement</span></span> | <span data-ttu-id="f21f4-121">Value</span><span class="sxs-lookup"><span data-stu-id="f21f4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21f4-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f21f4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f21f4-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f21f4-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f21f4-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f21f4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f21f4-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f21f4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f21f4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f21f4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f21f4-127"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f21f4-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f21f4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f21f4-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="f21f4-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f21f4-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f21f4-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="f21f4-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="f21f4-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="f21f4-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="f21f4-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="f21f4-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="f21f4-133">**No NOTIFICAr**</span><span class="sxs-lookup"><span data-stu-id="f21f4-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="f21f4-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="f21f4-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="f21f4-135">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f21f4-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f21f4-136">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="f21f4-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

