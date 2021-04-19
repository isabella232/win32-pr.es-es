---
title: CDN_FOLDERCHANGE de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como de estilo explorador cuando se abre una nueva carpeta.
ms.assetid: 864ab80d-cd99-4dd6-8aff-49beed246e53
keywords:
- CDN_FOLDERCHANGE de diálogo del código de notificación
topic_type:
- apiref
api_name:
- CDN_FOLDERCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39075bddbd191f60a9f9bcbad745e213fe9a978
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590872"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="841bf-104">Código de notificación FOLDERCHANGE de CDN \_</span><span class="sxs-lookup"><span data-stu-id="841bf-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="841bf-105">\[A partir de Windows Vista, **los** cuadros **de** diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo de elemento común](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="841bf-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="841bf-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]</span><span class="sxs-lookup"><span data-stu-id="841bf-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="841bf-107">Enviado por un cuadro de **diálogo** Abrir o Guardar **como** de estilo explorador cuando se abre una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="841bf-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="841bf-108">El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="841bf-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="841bf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="841bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="841bf-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="841bf-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="841bf-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="841bf-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="841bf-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="841bf-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="841bf-113">Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="841bf-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="841bf-114">La **estructura OFNOTIFY contiene** una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cuyo miembro de código indica el mensaje de notificación **\_ FOLDERCHANGE de la red CDN.** </span><span class="sxs-lookup"><span data-stu-id="841bf-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="841bf-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="841bf-115">Return value</span></span>

<span data-ttu-id="841bf-116">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="841bf-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="841bf-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="841bf-117">Remarks</span></span>

<span data-ttu-id="841bf-118">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="841bf-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="841bf-119">Para obtener la ruta de acceso de la carpeta recién abierta, el procedimiento de enlace puede enviar el mensaje [**\_ GETFOLDERPATH**](cdm-getfolderpath.md) de CDM al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="841bf-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="841bf-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="841bf-120">Requirements</span></span>



| <span data-ttu-id="841bf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="841bf-121">Requirement</span></span> | <span data-ttu-id="841bf-122">Value</span><span class="sxs-lookup"><span data-stu-id="841bf-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="841bf-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="841bf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="841bf-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="841bf-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="841bf-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="841bf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="841bf-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="841bf-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="841bf-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="841bf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="841bf-128"><dt>Commdlg.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="841bf-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="841bf-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="841bf-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="841bf-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="841bf-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="841bf-131">**GETFOLDERPATH de CDM \_**</span><span class="sxs-lookup"><span data-stu-id="841bf-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="841bf-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="841bf-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="841bf-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="841bf-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="841bf-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="841bf-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="841bf-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="841bf-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="841bf-136">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="841bf-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="841bf-137">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="841bf-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

