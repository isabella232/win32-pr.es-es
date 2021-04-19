---
title: CDN_TYPECHANGE de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como de estilo explorador cuando el usuario selecciona un nuevo tipo de archivo en el cuadro combinado tipos de archivo.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- CDN_TYPECHANGE cuadros de diálogo de código de notificación
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
ms.openlocfilehash: 180a16c32fb6e83ea0b17e38b42ce8c729f7685a
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590812"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="4824c-104">Código de notificación TYPECHANGE de CDN \_</span><span class="sxs-lookup"><span data-stu-id="4824c-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="4824c-105">\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo Elemento común](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="4824c-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="4824c-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]</span><span class="sxs-lookup"><span data-stu-id="4824c-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="4824c-107">Enviado por un cuadro de **diálogo** Abrir o Guardar **como** de estilo explorador cuando el usuario selecciona un nuevo tipo de archivo en el cuadro combinado tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="4824c-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="4824c-108">El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="4824c-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="4824c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4824c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4824c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4824c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4824c-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4824c-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4824c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4824c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4824c-113">Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="4824c-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="4824c-114">La [**estructura OFNOTIFY contiene**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de **notificación \_ TYPECHANGE de la red CDN.**</span><span class="sxs-lookup"><span data-stu-id="4824c-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="4824c-115">La [**estructura OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) también contiene un puntero a una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) cuyo **miembro nFilterIndex** indica el índice basado en uno del filtro de tipo de archivo recién seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4824c-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4824c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4824c-116">Return value</span></span>

<span data-ttu-id="4824c-117">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="4824c-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4824c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4824c-118">Remarks</span></span>

<span data-ttu-id="4824c-119">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="4824c-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4824c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4824c-120">Requirements</span></span>



| <span data-ttu-id="4824c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4824c-121">Requirement</span></span> | <span data-ttu-id="4824c-122">Value</span><span class="sxs-lookup"><span data-stu-id="4824c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4824c-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4824c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4824c-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4824c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4824c-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4824c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4824c-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4824c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4824c-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4824c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4824c-128"><dt>Commdlg.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4824c-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4824c-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4824c-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="4824c-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4824c-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4824c-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="4824c-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="4824c-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="4824c-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="4824c-133">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="4824c-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="4824c-134">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="4824c-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="4824c-135">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="4824c-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="4824c-136">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="4824c-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4824c-137">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="4824c-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

