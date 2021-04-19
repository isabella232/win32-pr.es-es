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
ms.openlocfilehash: 5c03fae474f6622e1ccec0c5b52b0dfb473ba438
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590852"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="27b71-104">Código de notificación HELP de CDN \_</span><span class="sxs-lookup"><span data-stu-id="27b71-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="27b71-105">\[A partir de Windows Vista, **los** cuadros **de** diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo de elemento común](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="27b71-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="27b71-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]</span><span class="sxs-lookup"><span data-stu-id="27b71-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="27b71-107">Enviado por un cuadro de **diálogo** Abrir o Guardar **como** de estilo explorador cuando el usuario hace clic en el **botón** Ayuda.</span><span class="sxs-lookup"><span data-stu-id="27b71-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="27b71-108">El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="27b71-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="27b71-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27b71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27b71-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27b71-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27b71-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="27b71-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27b71-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27b71-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27b71-113">Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="27b71-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="27b71-114">La **estructura OFNOTIFY contiene** una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de **notificación HELP \_ de cdn.**</span><span class="sxs-lookup"><span data-stu-id="27b71-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27b71-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27b71-115">Return value</span></span>

<span data-ttu-id="27b71-116">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="27b71-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="27b71-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27b71-117">Remarks</span></span>

<span data-ttu-id="27b71-118">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="27b71-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="27b71-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27b71-119">Requirements</span></span>



| <span data-ttu-id="27b71-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="27b71-120">Requirement</span></span> | <span data-ttu-id="27b71-121">Value</span><span class="sxs-lookup"><span data-stu-id="27b71-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27b71-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27b71-122">Minimum supported client</span></span><br/> | <span data-ttu-id="27b71-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="27b71-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="27b71-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27b71-124">Minimum supported server</span></span><br/> | <span data-ttu-id="27b71-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27b71-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="27b71-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27b71-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="27b71-127"><dt>Commdlg.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="27b71-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27b71-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="27b71-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="27b71-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="27b71-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="27b71-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="27b71-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="27b71-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="27b71-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="27b71-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="27b71-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="27b71-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="27b71-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="27b71-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="27b71-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="27b71-135">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="27b71-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="27b71-136">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="27b71-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

