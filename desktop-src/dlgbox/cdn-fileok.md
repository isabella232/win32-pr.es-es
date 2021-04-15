---
title: Código de notificación de CDN_FILEOK (commdlg. h)
description: Enviado por un cuadro de diálogo abrir o guardar como del explorador cuando el usuario especifica un nombre de archivo y hace clic en el botón Aceptar.
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- CDN_FILEOK cuadros de diálogo código de notificación
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aef63d531b603c94369936374bc10531639254
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676909"
---
# <a name="cdn_fileok-notification-code"></a><span data-ttu-id="d5bc5-104">\_Código de notificación FILEOK de CDN</span><span class="sxs-lookup"><span data-stu-id="d5bc5-104">CDN\_FILEOK notification code</span></span>

<span data-ttu-id="d5bc5-105">Enviado por un cuadro de diálogo **abrir** o **Guardar como** del explorador cuando el usuario especifica un nombre de archivo y hace clic en el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="d5bc5-105">Sent by an Explorer-style **Open** or **Save As** dialog box when the user specifies a file name and clicks the **OK** button.</span></span>

<span data-ttu-id="d5bc5-106">El procedimiento de enlace de [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje de [**\_ notificación de WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d5bc5-106">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="d5bc5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5bc5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5bc5-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5bc5-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5bc5-109">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d5bc5-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d5bc5-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5bc5-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5bc5-111">Puntero a una estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="d5bc5-111">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="d5bc5-112">La estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contiene una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cuyo miembro de **código** indica el mensaje de notificación FILEOK de la **red CDN \_** .</span><span class="sxs-lookup"><span data-stu-id="d5bc5-112">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FILEOK** notification message.</span></span>

<span data-ttu-id="d5bc5-113">La estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) también contiene un puntero a una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) cuyo miembro **lpstrFile** especifica la dirección del nombre de archivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d5bc5-113">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **lpstrFile** member specifies the address of the selected file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5bc5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5bc5-114">Return value</span></span>

<span data-ttu-id="d5bc5-115">Si el procedimiento de enlace devuelve cero, el cuadro de diálogo acepta el nombre de archivo especificado y se cierra.</span><span class="sxs-lookup"><span data-stu-id="d5bc5-115">If the hook procedure returns zero, the dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="d5bc5-116">Para rechazar el nombre de archivo especificado y forzar que el cuadro de diálogo permanezca abierto, devuelve un valor distinto de cero del procedimiento de enlace y llama a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer un valor **\_ MSGRESULT de DWL** distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d5bc5-116">To reject the specified file name and force the dialog box to remain open, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set a nonzero **DWL\_MSGRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5bc5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5bc5-117">Remarks</span></span>

<span data-ttu-id="d5bc5-118">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el valor del **\_ Explorador OFN** .</span><span class="sxs-lookup"><span data-stu-id="d5bc5-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5bc5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5bc5-119">Requirements</span></span>



| <span data-ttu-id="d5bc5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5bc5-120">Requirement</span></span> | <span data-ttu-id="d5bc5-121">Value</span><span class="sxs-lookup"><span data-stu-id="d5bc5-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5bc5-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5bc5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d5bc5-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d5bc5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d5bc5-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5bc5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d5bc5-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5bc5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d5bc5-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5bc5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5bc5-127"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5bc5-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5bc5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5bc5-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5bc5-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d5bc5-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d5bc5-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="d5bc5-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="d5bc5-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="d5bc5-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="d5bc5-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="d5bc5-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="d5bc5-133">**No NOTIFICAr**</span><span class="sxs-lookup"><span data-stu-id="d5bc5-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="d5bc5-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="d5bc5-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="d5bc5-135">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="d5bc5-135">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="d5bc5-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d5bc5-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d5bc5-137">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="d5bc5-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="d5bc5-138">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="d5bc5-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d5bc5-139">**\_notificaciones de WM**</span><span class="sxs-lookup"><span data-stu-id="d5bc5-139">**WM\_NOTIFY**</span></span>](../controls/wm-notify.md)
</dt> </dl>

 

