---
title: Mensaje SHAREVISTRING (Commdlg.h)
description: Un cuadro de diálogo Abrir o Guardar como envía el mensaje registrado de SHAREVISTRING al procedimiento de enlace, OFNHookProc, si se produce una infracción de uso compartido para el archivo seleccionado cuando el usuario hace clic en el botón Aceptar.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Cuadros de diálogo del mensaje SHAREVISTRING
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
ms.openlocfilehash: 043bed9edd08269e4e030482cbd44debea3a3695
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548770"
---
# <a name="sharevistring-message"></a><span data-ttu-id="3e641-104">Mensaje DE SHAREVISTRING</span><span class="sxs-lookup"><span data-stu-id="3e641-104">SHAREVISTRING message</span></span>

<span data-ttu-id="3e641-105">\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="3e641-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="3e641-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]</span><span class="sxs-lookup"><span data-stu-id="3e641-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="3e641-107">Un **cuadro** de **diálogo** Abrir o Guardar como envía el mensaje registrado de **SHAREVISTRING** al procedimiento de enlace, [*OFNHookProc,*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)si se produce una infracción de uso compartido para el archivo seleccionado cuando el usuario hace clic en el botón Aceptar. </span><span class="sxs-lookup"><span data-stu-id="3e641-107">An **Open** or **Save As** dialog box sends the **SHAREVISTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), if a sharing violation occurs for the selected file when the user clicks the **OK** button.</span></span>


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a><span data-ttu-id="3e641-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e641-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e641-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e641-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e641-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3e641-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e641-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e641-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e641-112">Puntero a una [**estructura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)</span><span class="sxs-lookup"><span data-stu-id="3e641-112">A pointer to a [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="3e641-113">El **miembro lpstrFile** de esta estructura contiene el nombre de archivo que produjo la infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="3e641-113">The **lpstrFile** member of this structure contains the file name that caused the sharing violation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e641-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e641-114">Return value</span></span>

<span data-ttu-id="3e641-115">El procedimiento de enlace debe devolver uno de los siguientes valores para indicar cómo el cuadro de diálogo debe controlar la infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="3e641-115">The hook procedure must return one of the following values to indicate how the dialog box should handle the sharing violation.</span></span>



| <span data-ttu-id="3e641-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e641-116">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="3e641-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e641-117">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e641-118"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3e641-118"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="3e641-119">Aceptación del nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="3e641-119">Accept the file name</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="3e641-120"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3e641-120"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="3e641-121">Rechace el nombre de archivo, pero no advierte al usuario.</span><span class="sxs-lookup"><span data-stu-id="3e641-121">Reject the file name but do not warn the user.</span></span> <span data-ttu-id="3e641-122">La aplicación es responsable de mostrar un mensaje de advertencia.</span><span class="sxs-lookup"><span data-stu-id="3e641-122">The application is responsible for displaying a warning message.</span></span><br/> |
| <dl> <span data-ttu-id="3e641-123"><dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e641-123"><dt>**OFN\_SHAREWARN**</dt> <dt>0</dt></span></span> </dl>        | <span data-ttu-id="3e641-124">Rechace el nombre de archivo y muestra un mensaje de advertencia (el mismo resultado que si no hubiera ningún procedimiento de enlace).</span><span class="sxs-lookup"><span data-stu-id="3e641-124">Reject the file name and displays a warning message (the same result as if there were no hook procedure).</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="3e641-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3e641-125">Remarks</span></span>

<span data-ttu-id="3e641-126">El procedimiento de enlace debe especificar la **constante SHAREVISTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3e641-126">The hook procedure must specify the **SHAREVISTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="3e641-127">El cuadro de diálogo envía el mensaje registrado **de SHAREVISTRING** solo si no especificó la marca **OFN \_ SHAREAWARE** en el miembro **Flags** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al crear el diálogo.</span><span class="sxs-lookup"><span data-stu-id="3e641-127">The dialog box sends the **SHAREVISTRING** registered message only if you did not specify the **OFN\_SHAREAWARE** flag in the **Flags** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure when you created the dialog.</span></span>

<span data-ttu-id="3e641-128">Si el procedimiento de enlace devuelve un valor indefinido, el cuadro de diálogo responde como si se hubiera devuelto **OFN \_ SHAREWARN.**</span><span class="sxs-lookup"><span data-stu-id="3e641-128">If the hook procedure returns an undefined value, the dialog box responds as if **OFN\_SHAREWARN** was returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e641-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e641-129">Requirements</span></span>



| <span data-ttu-id="3e641-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e641-130">Requirement</span></span> | <span data-ttu-id="3e641-131">Value</span><span class="sxs-lookup"><span data-stu-id="3e641-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e641-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e641-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3e641-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3e641-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3e641-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e641-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3e641-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e641-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3e641-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e641-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e641-137"><dt>Commdlg.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e641-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3e641-138">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="3e641-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3e641-139">**SHAREVISTRINGW** (Unicode) y **SHAREVISTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3e641-139">**SHAREVISTRINGW** (Unicode) and **SHAREVISTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="3e641-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3e641-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e641-141">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="3e641-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3e641-142">**CDN \_ SHAREVIOLATION**</span><span class="sxs-lookup"><span data-stu-id="3e641-142">**CDN\_SHAREVIOLATION**</span></span>](cdn-shareviolation.md)
</dt> <dt>

[<span data-ttu-id="3e641-143">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="3e641-143">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="3e641-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="3e641-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="3e641-145">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="3e641-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3e641-146">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="3e641-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

