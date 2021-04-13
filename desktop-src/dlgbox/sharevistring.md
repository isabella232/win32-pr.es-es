---
title: Mensaje SHAREVISTRING (commdlg. h)
description: Un cuadro de diálogo abrir o guardar como envía el mensaje registrado SHAREVISTRING al procedimiento de enlace, OFNHookProc, si se produce una infracción de uso compartido para el archivo seleccionado cuando el usuario hace clic en el botón Aceptar.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Cuadros de diálogo de mensaje de SHAREVISTRING
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23c17280ad1156e35f7e0f503816c07645cf4f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491872"
---
# <a name="sharevistring-message"></a><span data-ttu-id="a3802-104">Mensaje SHAREVISTRING</span><span class="sxs-lookup"><span data-stu-id="a3802-104">SHAREVISTRING message</span></span>

<span data-ttu-id="a3802-105">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3802-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="a3802-106">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="a3802-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="a3802-107">Un cuadro de diálogo **abrir** o **Guardar como** envía el mensaje registrado **SHAREVISTRING** al procedimiento de enlace, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), si se produce una infracción de uso compartido para el archivo seleccionado cuando el usuario hace clic en el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="a3802-107">An **Open** or **Save As** dialog box sends the **SHAREVISTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), if a sharing violation occurs for the selected file when the user clicks the **OK** button.</span></span>


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a><span data-ttu-id="a3802-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3802-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3802-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3802-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3802-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a3802-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a3802-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3802-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3802-112">Puntero a una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="a3802-112">A pointer to a [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="a3802-113">El miembro **lpstrFile** de esta estructura contiene el nombre de archivo que causó la infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="a3802-113">The **lpstrFile** member of this structure contains the file name that caused the sharing violation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3802-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3802-114">Return value</span></span>

<span data-ttu-id="a3802-115">El procedimiento de enlace debe devolver uno de los valores siguientes para indicar cómo el cuadro de diálogo debe controlar la infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="a3802-115">The hook procedure must return one of the following values to indicate how the dialog box should handle the sharing violation.</span></span>



| <span data-ttu-id="a3802-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3802-116">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="a3802-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3802-117">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3802-118"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a3802-118"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="a3802-119">Aceptar el nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="a3802-119">Accept the file name</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="a3802-120"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a3802-120"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="a3802-121">Rechace el nombre de archivo, pero no advierta al usuario.</span><span class="sxs-lookup"><span data-stu-id="a3802-121">Reject the file name but do not warn the user.</span></span> <span data-ttu-id="a3802-122">La aplicación es responsable de mostrar un mensaje de advertencia.</span><span class="sxs-lookup"><span data-stu-id="a3802-122">The application is responsible for displaying a warning message.</span></span><br/> |
| <dl> <span data-ttu-id="a3802-123"><dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a3802-123"><dt>**OFN\_SHAREWARN**</dt> <dt>0</dt></span></span> </dl>        | <span data-ttu-id="a3802-124">Rechace el nombre de archivo y muestre un mensaje de advertencia (el mismo resultado que si no hubiera ningún procedimiento de enlace).</span><span class="sxs-lookup"><span data-stu-id="a3802-124">Reject the file name and displays a warning message (the same result as if there were no hook procedure).</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="a3802-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3802-125">Remarks</span></span>

<span data-ttu-id="a3802-126">El procedimiento de enlace debe especificar la constante **SHAREVISTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a3802-126">The hook procedure must specify the **SHAREVISTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="a3802-127">El cuadro de diálogo solo envía el mensaje registrado de **SHAREVISTRING** si no especificó la marca **\_ SHAREAWARE de OFN** en el miembro **Flags** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al crear el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a3802-127">The dialog box sends the **SHAREVISTRING** registered message only if you did not specify the **OFN\_SHAREAWARE** flag in the **Flags** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure when you created the dialog.</span></span>

<span data-ttu-id="a3802-128">Si el procedimiento de enlace devuelve un valor no definido, el cuadro de diálogo responde como si se devolviera **OFN \_ SHAREWARN** .</span><span class="sxs-lookup"><span data-stu-id="a3802-128">If the hook procedure returns an undefined value, the dialog box responds as if **OFN\_SHAREWARN** was returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3802-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3802-129">Requirements</span></span>



| <span data-ttu-id="a3802-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3802-130">Requirement</span></span> | <span data-ttu-id="a3802-131">Value</span><span class="sxs-lookup"><span data-stu-id="a3802-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3802-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3802-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a3802-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a3802-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a3802-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3802-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a3802-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3802-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a3802-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3802-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3802-137"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3802-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a3802-138">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="a3802-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a3802-139">**SHAREVISTRINGW** (Unicode) y **SHAREVISTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a3802-139">**SHAREVISTRINGW** (Unicode) and **SHAREVISTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="a3802-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3802-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3802-141">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a3802-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a3802-142">**SHAREVIOLATION de CDN \_**</span><span class="sxs-lookup"><span data-stu-id="a3802-142">**CDN\_SHAREVIOLATION**</span></span>](cdn-shareviolation.md)
</dt> <dt>

[<span data-ttu-id="a3802-143">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="a3802-143">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="a3802-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="a3802-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="a3802-145">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a3802-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a3802-146">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="a3802-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

