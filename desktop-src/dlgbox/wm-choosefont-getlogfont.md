---
title: Mensaje de WM_CHOOSEFONT_GETLOGFONT (commdlg. h)
description: Una aplicación envía el \_ mensaje de CHOOSEFONT GETLOGFONT de WM \_ a un cuadro de diálogo de fuente para recuperar información sobre las selecciones de fuente actuales del usuario.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- WM_CHOOSEFONT_GETLOGFONT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696246d26c2b87e9b299844a9dc7e78d39ac632f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695975"
---
# <a name="wm_choosefont_getlogfont-message"></a><span data-ttu-id="0737e-104">\_Mensaje GETLOGFONT de CHOOSEFONT de WM \_</span><span class="sxs-lookup"><span data-stu-id="0737e-104">WM\_CHOOSEFONT\_GETLOGFONT message</span></span>

<span data-ttu-id="0737e-105">Una aplicación envía el mensaje de **\_ CHOOSEFONT \_ GETLOGFONT de WM** a un cuadro de diálogo de **fuente** para recuperar información sobre las selecciones de fuente actuales del usuario.</span><span class="sxs-lookup"><span data-stu-id="0737e-105">An application sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to a **Font** dialog box to retrieve information about the user's current font selections.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a><span data-ttu-id="0737e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0737e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0737e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0737e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0737e-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0737e-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0737e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0737e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0737e-110">Puntero a una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que recibe información sobre las selecciones de fuente actuales del usuario.</span><span class="sxs-lookup"><span data-stu-id="0737e-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the user's current font selections.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0737e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0737e-111">Return value</span></span>

<span data-ttu-id="0737e-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0737e-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0737e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0737e-113">Remarks</span></span>

<span data-ttu-id="0737e-114">La función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crea un cuadro de diálogo de **fuente** .</span><span class="sxs-lookup"><span data-stu-id="0737e-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box.</span></span> <span data-ttu-id="0737e-115">Cuando el usuario cierra el cuadro de diálogo **fuente** , la función **ChooseFont** devuelve información sobre las selecciones de fuente del usuario en la estructura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .</span><span class="sxs-lookup"><span data-stu-id="0737e-115">When the user closes the **Font** dialog box, the **ChooseFont** function returns information about the user's font selections in the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure.</span></span> <span data-ttu-id="0737e-116">El miembro **lpLogFont** de la estructura **CHOOSEFONT** es un puntero a una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="0737e-116">The **lpLogFont** member of the **CHOOSEFONT** structure is a pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

<span data-ttu-id="0737e-117">Use el mensaje de **\_ \_ GETLOGFONT de CHOOSEFONT de WM** para obtener información sobre las selecciones de fuente actuales del usuario mientras el cuadro de diálogo **fuente** está abierto.</span><span class="sxs-lookup"><span data-stu-id="0737e-117">Use the **WM\_CHOOSEFONT\_GETLOGFONT** message to get information about the user's current font selections while the **Font** dialog box is open.</span></span> <span data-ttu-id="0737e-118">Por ejemplo, si habilita el botón **aplicar** en el cuadro de diálogo **fuente** , envíe el mensaje para obtener la información de fuente que se va a aplicar a la selección de texto actual.</span><span class="sxs-lookup"><span data-stu-id="0737e-118">For example, if you enable the **Apply** button in the **Font** dialog box, send the message to get the font information to apply to the current text selection.</span></span>

<span data-ttu-id="0737e-119">Normalmente, se habilita un procedimiento de enlace [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) para procesar los mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) para el botón **aplicar** .</span><span class="sxs-lookup"><span data-stu-id="0737e-119">Typically, you enable a [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure to process [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages for the **Apply** button.</span></span> <span data-ttu-id="0737e-120">Cuando el usuario hace clic en el botón **aplicar** , el procedimiento de enlace envía el mensaje de **\_ CHOOSEFONT \_ GETLOGFONT de WM** al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0737e-120">When the user clicks the **Apply** button, the hook procedure sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="0737e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0737e-121">Requirements</span></span>



| <span data-ttu-id="0737e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0737e-122">Requirement</span></span> | <span data-ttu-id="0737e-123">Value</span><span class="sxs-lookup"><span data-stu-id="0737e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0737e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0737e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0737e-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0737e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0737e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0737e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0737e-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0737e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0737e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0737e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0737e-129"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0737e-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0737e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0737e-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="0737e-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0737e-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0737e-132">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="0737e-132">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="0737e-133">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="0737e-133">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="0737e-134">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="0737e-134">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="0737e-135">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="0737e-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> <dt>

<span data-ttu-id="0737e-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0737e-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0737e-137">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="0737e-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="0737e-138">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="0737e-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0737e-139">**NDPTECGDI**</span><span class="sxs-lookup"><span data-stu-id="0737e-139">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

