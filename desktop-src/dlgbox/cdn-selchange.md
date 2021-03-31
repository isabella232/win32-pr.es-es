---
title: Código de notificación de CDN_SELCHANGE (commdlg. h)
description: Enviado por un cuadro de diálogo para abrir o guardar como del explorador cuando la selección cambia en el cuadro de lista que muestra el contenido de la carpeta o el directorio abiertos actualmente.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- CDN_SELCHANGE cuadros de diálogo código de notificación
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2f0f5a7860c7d729340a84bd80bc4e5713c733
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490570"
---
# <a name="cdn_selchange-notification-code"></a><span data-ttu-id="98e66-104">\_Código de notificación SELCHANGE de CDN</span><span class="sxs-lookup"><span data-stu-id="98e66-104">CDN\_SELCHANGE notification code</span></span>

<span data-ttu-id="98e66-105">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="98e66-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="98e66-106">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="98e66-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="98e66-107">Enviado por un cuadro de diálogo para **abrir** o **Guardar como** del explorador cuando la selección cambia en el cuadro de lista que muestra el contenido de la carpeta o el directorio abiertos actualmente.</span><span class="sxs-lookup"><span data-stu-id="98e66-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the selection changes in the list box that displays the contents of the currently opened folder or directory.</span></span>

<span data-ttu-id="98e66-108">El procedimiento de enlace de [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje de [**\_ notificación de WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="98e66-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a><span data-ttu-id="98e66-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98e66-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e66-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98e66-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98e66-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="98e66-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98e66-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98e66-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98e66-113">Puntero a una estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="98e66-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="98e66-114">La estructura **imnotify** contiene una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cuyo miembro de **código** indica el mensaje de notificación SELCHANGE de la **red CDN \_** .</span><span class="sxs-lookup"><span data-stu-id="98e66-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SELCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e66-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98e66-115">Return value</span></span>

<span data-ttu-id="98e66-116">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="98e66-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e66-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98e66-117">Remarks</span></span>

<span data-ttu-id="98e66-118">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el valor del **\_ Explorador OFN** .</span><span class="sxs-lookup"><span data-stu-id="98e66-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="98e66-119">Para obtener el nombre del archivo o carpeta recién seleccionado, el procedimiento de enlace puede enviar el mensaje [**CDM \_ GETFILEPATH**](cdm-getfilepath.md) o [**CDM \_ GETSPEC**](cdm-getspec.md) al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="98e66-119">To get the name of the newly selected file or folder, the hook procedure can send the [**CDM\_GETFILEPATH**](cdm-getfilepath.md) or [**CDM\_GETSPEC**](cdm-getspec.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e66-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98e66-120">Requirements</span></span>



| <span data-ttu-id="98e66-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="98e66-121">Requirement</span></span> | <span data-ttu-id="98e66-122">Value</span><span class="sxs-lookup"><span data-stu-id="98e66-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e66-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98e66-123">Minimum supported client</span></span><br/> | <span data-ttu-id="98e66-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98e66-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="98e66-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98e66-125">Minimum supported server</span></span><br/> | <span data-ttu-id="98e66-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98e66-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="98e66-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98e66-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="98e66-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98e66-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e66-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="98e66-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="98e66-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="98e66-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="98e66-131">**CDM \_ GETFILEPATH**</span><span class="sxs-lookup"><span data-stu-id="98e66-131">**CDM\_GETFILEPATH**</span></span>](cdm-getfilepath.md)
</dt> <dt>

[<span data-ttu-id="98e66-132">**CDM \_ GETSPEC**</span><span class="sxs-lookup"><span data-stu-id="98e66-132">**CDM\_GETSPEC**</span></span>](cdm-getspec.md)
</dt> <dt>

[<span data-ttu-id="98e66-133">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="98e66-133">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="98e66-134">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="98e66-134">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="98e66-135">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="98e66-135">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="98e66-136">**No NOTIFICAr**</span><span class="sxs-lookup"><span data-stu-id="98e66-136">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="98e66-137">**Vista**</span><span class="sxs-lookup"><span data-stu-id="98e66-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="98e66-138">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="98e66-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

