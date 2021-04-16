---
title: Mensaje de CDM_HIDECONTROL (commdlg. h)
description: Oculta el control especificado en un cuadro de diálogo abrir o guardar como de estilo del explorador.
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- CDM_HIDECONTROL cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- CDM_HIDECONTROL
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff632b7d1e3c24c84f73498846db9e6bfa68fd74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666011"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="ef2fd-104">\_Mensaje HIDECONTROL CDM</span><span class="sxs-lookup"><span data-stu-id="ef2fd-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="ef2fd-105">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ef2fd-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="ef2fd-106">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="ef2fd-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="ef2fd-107">Oculta el control especificado en un cuadro de diálogo **abrir** o **Guardar como** de estilo del explorador.</span><span class="sxs-lookup"><span data-stu-id="ef2fd-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="ef2fd-108">El cuadro de diálogo se debe haber creado con la marca **OFN \_ Explorer** ; de lo contrario, se produce un error en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef2fd-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="ef2fd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef2fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef2fd-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef2fd-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef2fd-111">Identificador del control que se va a ocultar.</span><span class="sxs-lookup"><span data-stu-id="ef2fd-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="ef2fd-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef2fd-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef2fd-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ef2fd-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef2fd-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef2fd-114">Return value</span></span>

<span data-ttu-id="ef2fd-115">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="ef2fd-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef2fd-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef2fd-116">Remarks</span></span>

<span data-ttu-id="ef2fd-117">La macro correspondiente es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ef2fd-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="ef2fd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef2fd-118">Requirements</span></span>



| <span data-ttu-id="ef2fd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef2fd-119">Requirement</span></span> | <span data-ttu-id="ef2fd-120">Value</span><span class="sxs-lookup"><span data-stu-id="ef2fd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2fd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef2fd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ef2fd-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ef2fd-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ef2fd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef2fd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ef2fd-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef2fd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ef2fd-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef2fd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef2fd-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef2fd-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef2fd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef2fd-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef2fd-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ef2fd-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ef2fd-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="ef2fd-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="ef2fd-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="ef2fd-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="ef2fd-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="ef2fd-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="ef2fd-132">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ef2fd-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ef2fd-133">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="ef2fd-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

