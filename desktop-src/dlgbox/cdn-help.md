---
title: CDN_HELP de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como de estilo explorador cuando el usuario hace clic en el botón Ayuda.
ms.assetid: 18ee86b2-3446-4de4-a47a-2e44e677f4f7
keywords:
- CDN_HELP de diálogo del código de notificación
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
ms.openlocfilehash: 0abd3519bdc877eca24304b1104a12d51b2dfe4f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550070"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="85b3a-104">Código de notificación DE AYUDA de CDN \_</span><span class="sxs-lookup"><span data-stu-id="85b3a-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="85b3a-105">\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="85b3a-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="85b3a-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]</span><span class="sxs-lookup"><span data-stu-id="85b3a-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="85b3a-107">Enviado por un cuadro de **diálogo** Abrir o Guardar **como** de estilo explorador cuando el usuario hace clic en el **botón Ayuda.**</span><span class="sxs-lookup"><span data-stu-id="85b3a-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="85b3a-108">El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="85b3a-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="85b3a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85b3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85b3a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85b3a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85b3a-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="85b3a-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85b3a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85b3a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85b3a-113">Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="85b3a-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="85b3a-114">La **estructura OFNOTIFY contiene** una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de **notificación DE AYUDA \_ de CDN.**</span><span class="sxs-lookup"><span data-stu-id="85b3a-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85b3a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85b3a-115">Return value</span></span>

<span data-ttu-id="85b3a-116">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="85b3a-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="85b3a-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85b3a-117">Remarks</span></span>

<span data-ttu-id="85b3a-118">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="85b3a-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="85b3a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85b3a-119">Requirements</span></span>



| <span data-ttu-id="85b3a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="85b3a-120">Requirement</span></span> | <span data-ttu-id="85b3a-121">Value</span><span class="sxs-lookup"><span data-stu-id="85b3a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85b3a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85b3a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="85b3a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="85b3a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="85b3a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85b3a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="85b3a-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="85b3a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="85b3a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85b3a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="85b3a-127"><dt>Commdlg.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="85b3a-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85b3a-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="85b3a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="85b3a-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="85b3a-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="85b3a-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="85b3a-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="85b3a-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="85b3a-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="85b3a-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="85b3a-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="85b3a-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="85b3a-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="85b3a-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="85b3a-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="85b3a-135">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="85b3a-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="85b3a-136">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="85b3a-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

