---
title: CDN_INITDONE de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como de estilo explorador cuando el sistema ha terminado de organizar los controles del cuadro de diálogo. El sistema mueve los controles estándar para hacer espacio para los controles del cuadro de diálogo secundario.
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- CDN_INITDONE de diálogo de código de notificación
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
ms.openlocfilehash: 6594c161d57a5d0772679477ee9bce2cda28ba12
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549840"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="6c042-105">Código de notificación \_ INITDONE de CDN</span><span class="sxs-lookup"><span data-stu-id="6c042-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="6c042-106">\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="6c042-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="6c042-107">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]</span><span class="sxs-lookup"><span data-stu-id="6c042-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="6c042-108">Enviado por un cuadro de **diálogo** Abrir o Guardar **como** de estilo explorador cuando el sistema ha terminado de organizar los controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6c042-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="6c042-109">El sistema mueve los controles estándar para hacer espacio para los controles del cuadro de diálogo secundario.</span><span class="sxs-lookup"><span data-stu-id="6c042-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="6c042-110">El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="6c042-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="6c042-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c042-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c042-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c042-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c042-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6c042-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6c042-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c042-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c042-115">Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="6c042-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="6c042-116">La **estructura OFNOTIFY contiene** una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de **notificación \_ INITDONE de CDN.**</span><span class="sxs-lookup"><span data-stu-id="6c042-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c042-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c042-117">Return value</span></span>

<span data-ttu-id="6c042-118">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="6c042-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c042-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c042-119">Remarks</span></span>

<span data-ttu-id="6c042-120">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="6c042-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c042-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c042-121">Requirements</span></span>



| <span data-ttu-id="6c042-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c042-122">Requirement</span></span> | <span data-ttu-id="6c042-123">Value</span><span class="sxs-lookup"><span data-stu-id="6c042-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c042-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c042-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c042-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6c042-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6c042-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c042-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c042-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c042-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c042-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c042-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c042-129"><dt>Commdlg.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c042-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c042-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6c042-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c042-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6c042-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6c042-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="6c042-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="6c042-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="6c042-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="6c042-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="6c042-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="6c042-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="6c042-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="6c042-136">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="6c042-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="6c042-137">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="6c042-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6c042-138">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="6c042-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

