---
title: CDM_HIDECONTROL mensaje (Commdlg.h)
description: Oculta el control especificado en un cuadro de diálogo Abrir o Guardar como de estilo explorador.
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- CDM_HIDECONTROL cuadro de diálogo de mensaje
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
ms.openlocfilehash: 21f1a5a7a1830ceeb2c3671b0dfb538ad89e0a58
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548660"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="82f58-104">Mensaje \_ HIDECONTROL de CDM</span><span class="sxs-lookup"><span data-stu-id="82f58-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="82f58-105">\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="82f58-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="82f58-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]</span><span class="sxs-lookup"><span data-stu-id="82f58-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="82f58-107">Oculta el control especificado en un  cuadro de diálogo Abrir o Guardar **como** de estilo explorador.</span><span class="sxs-lookup"><span data-stu-id="82f58-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="82f58-108">El cuadro de diálogo debe haber sido creado con la **marca OFN \_ EXPLORER;** de lo contrario, se produce un error en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="82f58-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="82f58-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82f58-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82f58-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82f58-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82f58-111">Identificador del control que se va a ocultar.</span><span class="sxs-lookup"><span data-stu-id="82f58-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="82f58-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82f58-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82f58-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="82f58-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82f58-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82f58-114">Return value</span></span>

<span data-ttu-id="82f58-115">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="82f58-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82f58-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82f58-116">Remarks</span></span>

<span data-ttu-id="82f58-117">La macro correspondiente es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="82f58-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="82f58-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82f58-118">Requirements</span></span>



| <span data-ttu-id="82f58-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="82f58-119">Requirement</span></span> | <span data-ttu-id="82f58-120">Value</span><span class="sxs-lookup"><span data-stu-id="82f58-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82f58-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82f58-121">Minimum supported client</span></span><br/> | <span data-ttu-id="82f58-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="82f58-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="82f58-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82f58-123">Minimum supported server</span></span><br/> | <span data-ttu-id="82f58-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="82f58-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="82f58-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82f58-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="82f58-126"><dt>Commdlg.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="82f58-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82f58-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="82f58-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="82f58-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="82f58-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="82f58-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="82f58-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="82f58-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="82f58-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="82f58-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="82f58-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="82f58-132">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="82f58-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="82f58-133">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="82f58-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

