---
title: Mensaje de CDM_SETCONTROLTEXT (commdlg. h)
description: Establece el texto para el control especificado en un cuadro de diálogo abrir o guardar como de estilo del explorador.
ms.assetid: ff0e50b7-a14d-40d1-8576-f93a612f3aa3
keywords:
- CDM_SETCONTROLTEXT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- CDM_SETCONTROLTEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87490ba20b5785da4fb9660d97b1b9232d047671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421885"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="b4a43-104">\_Mensaje SETCONTROLTEXT CDM</span><span class="sxs-lookup"><span data-stu-id="b4a43-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="b4a43-105">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b4a43-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="b4a43-106">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="b4a43-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="b4a43-107">Establece el texto para el control especificado en un cuadro de diálogo **abrir** o **Guardar como** de estilo del explorador.</span><span class="sxs-lookup"><span data-stu-id="b4a43-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="b4a43-108">El cuadro de diálogo se debe haber creado con la marca **OFN \_ Explorer** ; de lo contrario, se produce un error en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b4a43-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="b4a43-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4a43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4a43-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4a43-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4a43-111">Identificador del control en cuyo texto se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="b4a43-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="b4a43-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4a43-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4a43-113">Nuevo texto del control.</span><span class="sxs-lookup"><span data-stu-id="b4a43-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4a43-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4a43-114">Return value</span></span>

<span data-ttu-id="b4a43-115">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b4a43-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4a43-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4a43-116">Remarks</span></span>

<span data-ttu-id="b4a43-117">La macro correspondiente es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="b4a43-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="b4a43-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4a43-118">Requirements</span></span>



| <span data-ttu-id="b4a43-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a43-119">Requirement</span></span> | <span data-ttu-id="b4a43-120">Value</span><span class="sxs-lookup"><span data-stu-id="b4a43-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a43-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4a43-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b4a43-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b4a43-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b4a43-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4a43-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b4a43-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4a43-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b4a43-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4a43-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4a43-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4a43-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a43-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4a43-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b4a43-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b4a43-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b4a43-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="b4a43-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="b4a43-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="b4a43-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="b4a43-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="b4a43-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="b4a43-132">**Vista**</span><span class="sxs-lookup"><span data-stu-id="b4a43-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b4a43-133">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="b4a43-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

