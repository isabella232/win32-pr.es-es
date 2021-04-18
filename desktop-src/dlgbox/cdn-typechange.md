---
title: Código de notificación de CDN_TYPECHANGE (commdlg. h)
description: Enviado por un cuadro de diálogo abrir o guardar como del explorador cuando el usuario selecciona un nuevo tipo de archivo en el cuadro combinado tipos de archivo.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- CDN_TYPECHANGE cuadros de diálogo código de notificación
topic_type:
- apiref
api_name:
- CDN_TYPECHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64226c1ac15cb6b55c6c2e2de7264d726e6f3a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490565"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="6678f-104">\_Código de notificación TYPECHANGE de CDN</span><span class="sxs-lookup"><span data-stu-id="6678f-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="6678f-105">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6678f-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="6678f-106">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="6678f-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="6678f-107">Enviado por un cuadro de diálogo **abrir** o **Guardar como** del explorador cuando el usuario selecciona un nuevo tipo de archivo en el cuadro combinado tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="6678f-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="6678f-108">El procedimiento de enlace de [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje de [**\_ notificación de WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6678f-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="6678f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6678f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6678f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6678f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6678f-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6678f-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6678f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6678f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6678f-113">Puntero a una estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="6678f-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="6678f-114">La estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contiene una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cuyo miembro de **código** indica el mensaje de notificación TYPECHANGE de la **red CDN \_** .</span><span class="sxs-lookup"><span data-stu-id="6678f-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="6678f-115">La estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) también contiene un puntero a una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) cuyo miembro **nFilterIndex** indica el índice de base uno del filtro de tipo de archivo recién seleccionado.</span><span class="sxs-lookup"><span data-stu-id="6678f-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6678f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6678f-116">Return value</span></span>

<span data-ttu-id="6678f-117">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="6678f-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6678f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6678f-118">Remarks</span></span>

<span data-ttu-id="6678f-119">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el valor del **\_ Explorador OFN** .</span><span class="sxs-lookup"><span data-stu-id="6678f-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6678f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6678f-120">Requirements</span></span>



| <span data-ttu-id="6678f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6678f-121">Requirement</span></span> | <span data-ttu-id="6678f-122">Value</span><span class="sxs-lookup"><span data-stu-id="6678f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6678f-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6678f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6678f-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6678f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6678f-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6678f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6678f-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6678f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6678f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6678f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6678f-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6678f-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6678f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6678f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="6678f-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6678f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6678f-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="6678f-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="6678f-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="6678f-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="6678f-133">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="6678f-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="6678f-134">**No NOTIFICAr**</span><span class="sxs-lookup"><span data-stu-id="6678f-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="6678f-135">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="6678f-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="6678f-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="6678f-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6678f-137">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="6678f-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

