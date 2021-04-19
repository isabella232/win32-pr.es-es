---
title: CDN_INITDONE de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como de estilo explorador cuando el sistema ha terminado de organizar los controles en el cuadro de diálogo. El sistema mueve los controles estándar para hacer espacio para los controles del cuadro de diálogo secundario.
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
ms.openlocfilehash: 5b07c25183eced86c3a430621091bed74c53f90d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590802"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="936b5-105">Código de notificación \_ INITDONE de CDN</span><span class="sxs-lookup"><span data-stu-id="936b5-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="936b5-106">\[A partir de Windows Vista, **los** cuadros **de** diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo de elemento común](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="936b5-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="936b5-107">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]</span><span class="sxs-lookup"><span data-stu-id="936b5-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="936b5-108">Enviado por un cuadro de **diálogo** Abrir o Guardar **como** de estilo explorador cuando el sistema ha terminado de organizar los controles en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="936b5-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="936b5-109">El sistema mueve los controles estándar para hacer espacio para los controles del cuadro de diálogo secundario.</span><span class="sxs-lookup"><span data-stu-id="936b5-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="936b5-110">El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="936b5-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="936b5-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="936b5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936b5-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="936b5-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="936b5-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="936b5-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="936b5-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="936b5-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="936b5-115">Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="936b5-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="936b5-116">La **estructura OFNOTIFY contiene** una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de **notificación \_ INITDONE de CDN.**</span><span class="sxs-lookup"><span data-stu-id="936b5-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="936b5-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="936b5-117">Return value</span></span>

<span data-ttu-id="936b5-118">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="936b5-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="936b5-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="936b5-119">Remarks</span></span>

<span data-ttu-id="936b5-120">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="936b5-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="936b5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="936b5-121">Requirements</span></span>



| <span data-ttu-id="936b5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="936b5-122">Requirement</span></span> | <span data-ttu-id="936b5-123">Value</span><span class="sxs-lookup"><span data-stu-id="936b5-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="936b5-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="936b5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="936b5-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="936b5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="936b5-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="936b5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="936b5-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="936b5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="936b5-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="936b5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="936b5-129"><dt>Commdlg.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="936b5-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="936b5-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="936b5-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="936b5-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="936b5-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="936b5-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="936b5-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="936b5-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="936b5-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="936b5-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="936b5-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="936b5-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="936b5-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="936b5-136">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="936b5-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="936b5-137">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="936b5-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="936b5-138">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="936b5-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

