---
title: Código de notificación de CDN_FOLDERCHANGE (commdlg. h)
description: Enviado por un cuadro de diálogo abrir o guardar como del explorador cuando se abre una nueva carpeta.
ms.assetid: 864ab80d-cd99-4dd6-8aff-49beed246e53
keywords:
- CDN_FOLDERCHANGE cuadros de diálogo código de notificación
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
ms.openlocfilehash: 4c93bd37afa44e7fc5ca81d928974f56bf80d1b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150374"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="1ca44-104">\_Código de notificación FOLDERCHANGE de CDN</span><span class="sxs-lookup"><span data-stu-id="1ca44-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="1ca44-105">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1ca44-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="1ca44-106">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="1ca44-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="1ca44-107">Enviado por un cuadro de diálogo **abrir** o **Guardar como** del explorador cuando se abre una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="1ca44-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="1ca44-108">El procedimiento de enlace de [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje de [**\_ notificación de WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ca44-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="1ca44-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ca44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ca44-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ca44-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ca44-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1ca44-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ca44-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ca44-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ca44-113">Puntero a una estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="1ca44-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="1ca44-114">La estructura **imnotify** contiene una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cuyo miembro de **código** indica el mensaje de notificación FOLDERCHANGE de la **red CDN \_** .</span><span class="sxs-lookup"><span data-stu-id="1ca44-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ca44-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ca44-115">Return value</span></span>

<span data-ttu-id="1ca44-116">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1ca44-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ca44-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ca44-117">Remarks</span></span>

<span data-ttu-id="1ca44-118">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el valor del **\_ Explorador OFN** .</span><span class="sxs-lookup"><span data-stu-id="1ca44-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="1ca44-119">Para obtener la ruta de acceso de la carpeta recién abierta, el procedimiento de enlace puede enviar el mensaje de la [**\_ GETFOLDERPATH de CDM**](cdm-getfolderpath.md) al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1ca44-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ca44-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ca44-120">Requirements</span></span>



| <span data-ttu-id="1ca44-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ca44-121">Requirement</span></span> | <span data-ttu-id="1ca44-122">Value</span><span class="sxs-lookup"><span data-stu-id="1ca44-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca44-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ca44-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1ca44-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1ca44-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1ca44-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ca44-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1ca44-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ca44-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ca44-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ca44-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ca44-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ca44-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ca44-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ca44-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="1ca44-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1ca44-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1ca44-131">**GETFOLDERPATH de CDM \_**</span><span class="sxs-lookup"><span data-stu-id="1ca44-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="1ca44-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="1ca44-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="1ca44-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="1ca44-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="1ca44-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="1ca44-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="1ca44-135">**No NOTIFICAr**</span><span class="sxs-lookup"><span data-stu-id="1ca44-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="1ca44-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="1ca44-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1ca44-137">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="1ca44-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

