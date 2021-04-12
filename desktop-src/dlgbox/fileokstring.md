---
title: Mensaje FILEOKSTRING (commdlg. h)
description: Un cuadro de diálogo abrir o guardar como envía el mensaje registrado FILEOKSTRING al procedimiento de enlace, OFNHookProc, cuando el usuario especifica un nombre de archivo y hace clic en el botón Aceptar.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Cuadros de diálogo de mensaje de FILEOKSTRING
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61208ddebc63f1186c2947416e451231f0bea24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492874"
---
# <a name="fileokstring-message"></a><span data-ttu-id="ffb69-104">Mensaje FILEOKSTRING</span><span class="sxs-lookup"><span data-stu-id="ffb69-104">FILEOKSTRING message</span></span>

<span data-ttu-id="ffb69-105">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ffb69-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="ffb69-106">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="ffb69-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="ffb69-107">Un cuadro de diálogo **abrir** o **Guardar como** envía el mensaje registrado **FILEOKSTRING** al procedimiento de enlace, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), cuando el usuario especifica un nombre de archivo y hace clic en el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="ffb69-107">An **Open** or **Save As** dialog box sends the **FILEOKSTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), when the user specifies a file name and clicks the **OK** button.</span></span> <span data-ttu-id="ffb69-108">El procedimiento de enlace puede aceptar el nombre de archivo y permitir que el cuadro de diálogo se cierre, o bien rechazar el nombre de archivo y forzar que el cuadro de diálogo permanezca abierto.</span><span class="sxs-lookup"><span data-stu-id="ffb69-108">The hook procedure can accept the file name and allow the dialog box to close, or reject the file name and force the dialog box to remain open.</span></span>


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a><span data-ttu-id="ffb69-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffb69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffb69-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ffb69-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffb69-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ffb69-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ffb69-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ffb69-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffb69-113">Puntero a una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="ffb69-113">A pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="ffb69-114">El miembro **lpstrFile** de esta estructura contiene la unidad, la ruta de acceso y el nombre de archivo especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ffb69-114">The **lpstrFile** member of this structure contains the drive, path, and file name specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffb69-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffb69-115">Return value</span></span>

<span data-ttu-id="ffb69-116">Si el procedimiento de enlace devuelve cero, el cuadro de diálogo **abrir** o **Guardar como** acepta el nombre de archivo especificado y se cierra.</span><span class="sxs-lookup"><span data-stu-id="ffb69-116">If the hook procedure returns zero, the **Open** or **Save As** dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="ffb69-117">Si el procedimiento de enlace devuelve un valor distinto de cero, el cuadro de diálogo **abrir** o **Guardar como** rechaza el nombre de archivo especificado y permanece abierto.</span><span class="sxs-lookup"><span data-stu-id="ffb69-117">If the hook procedure returns a nonzero value, the **Open** or **Save As** dialog box rejects the specified file name and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffb69-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffb69-118">Remarks</span></span>

<span data-ttu-id="ffb69-119">El procedimiento de enlace debe especificar la constante **FILEOKSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ffb69-119">The hook procedure must specify the **FILEOKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffb69-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffb69-120">Requirements</span></span>



| <span data-ttu-id="ffb69-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffb69-121">Requirement</span></span> | <span data-ttu-id="ffb69-122">Value</span><span class="sxs-lookup"><span data-stu-id="ffb69-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb69-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffb69-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ffb69-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ffb69-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ffb69-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffb69-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ffb69-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ffb69-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ffb69-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffb69-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffb69-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffb69-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ffb69-129">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ffb69-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ffb69-130">**FILEOKSTRINGW** (Unicode) y **FILEOKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ffb69-130">**FILEOKSTRINGW** (Unicode) and **FILEOKSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="ffb69-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffb69-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="ffb69-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ffb69-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ffb69-133">**FILEOK de CDN \_**</span><span class="sxs-lookup"><span data-stu-id="ffb69-133">**CDN\_FILEOK**</span></span>](cdn-fileok.md)
</dt> <dt>

[<span data-ttu-id="ffb69-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="ffb69-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="ffb69-135">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="ffb69-135">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="ffb69-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ffb69-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ffb69-137">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="ffb69-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

