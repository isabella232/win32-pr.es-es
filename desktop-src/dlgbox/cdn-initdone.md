---
title: Código de notificación de CDN_INITDONE (commdlg. h)
description: Enviado por un cuadro de diálogo abrir o guardar como del explorador cuando el sistema ha terminado de organizar los controles en el cuadro de diálogo. El sistema mueve los controles estándar para dejar espacio a los controles del cuadro de diálogo secundario.
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- CDN_INITDONE cuadros de diálogo código de notificación
topic_type:
- apiref
api_name:
- CDN_INITDONE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6d51f1c34a0a399775e1786356aae4fc6526fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422308"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="32268-105">\_Código de notificación INITDONE de CDN</span><span class="sxs-lookup"><span data-stu-id="32268-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="32268-106">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32268-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="32268-107">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="32268-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="32268-108">Enviado por un cuadro de diálogo **abrir** o **Guardar como** del explorador cuando el sistema ha terminado de organizar los controles en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="32268-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="32268-109">El sistema mueve los controles estándar para dejar espacio a los controles del cuadro de diálogo secundario.</span><span class="sxs-lookup"><span data-stu-id="32268-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="32268-110">El procedimiento de enlace de [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje de [**\_ notificación de WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="32268-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="32268-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32268-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32268-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32268-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32268-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="32268-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="32268-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32268-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32268-115">Puntero a una estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="32268-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="32268-116">La estructura **imnotify** contiene una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cuyo miembro de **código** indica el mensaje de notificación INITDONE de la **red CDN \_** .</span><span class="sxs-lookup"><span data-stu-id="32268-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32268-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32268-117">Return value</span></span>

<span data-ttu-id="32268-118">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="32268-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="32268-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32268-119">Remarks</span></span>

<span data-ttu-id="32268-120">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el valor del **\_ Explorador OFN** .</span><span class="sxs-lookup"><span data-stu-id="32268-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="32268-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32268-121">Requirements</span></span>



| <span data-ttu-id="32268-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="32268-122">Requirement</span></span> | <span data-ttu-id="32268-123">Value</span><span class="sxs-lookup"><span data-stu-id="32268-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32268-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32268-124">Minimum supported client</span></span><br/> | <span data-ttu-id="32268-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="32268-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="32268-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32268-126">Minimum supported server</span></span><br/> | <span data-ttu-id="32268-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32268-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32268-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32268-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="32268-129"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32268-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32268-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="32268-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="32268-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="32268-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="32268-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="32268-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="32268-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="32268-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="32268-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="32268-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="32268-135">**No NOTIFICAr**</span><span class="sxs-lookup"><span data-stu-id="32268-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="32268-136">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="32268-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="32268-137">**Vista**</span><span class="sxs-lookup"><span data-stu-id="32268-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="32268-138">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="32268-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

