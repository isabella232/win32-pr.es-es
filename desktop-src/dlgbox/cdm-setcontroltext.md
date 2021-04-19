---
title: CDM_SETCONTROLTEXT mensaje (Commdlg.h)
description: Establece el texto del control especificado en un cuadro de diálogo Abrir o Guardar como de estilo explorador.
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
ms.openlocfilehash: 74d75bb3d3ac486bbb43545df80c67383a7655b8
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590892"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="e41a6-104">Mensaje \_ SETCONTROLTEXT de CDM</span><span class="sxs-lookup"><span data-stu-id="e41a6-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="e41a6-105">\[A partir de Windows Vista, **los** cuadros **de** diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo de elemento común](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="e41a6-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="e41a6-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]</span><span class="sxs-lookup"><span data-stu-id="e41a6-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="e41a6-107">Establece el texto del control especificado en  un cuadro de diálogo Abrir o **Guardar como** de estilo explorador.</span><span class="sxs-lookup"><span data-stu-id="e41a6-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="e41a6-108">El cuadro de diálogo se debe haber creado con la **marca OFN \_ EXPLORER;** de lo contrario, se produce un error en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e41a6-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="e41a6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e41a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e41a6-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e41a6-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e41a6-111">Identificador del control en el que se va a establecer el texto.</span><span class="sxs-lookup"><span data-stu-id="e41a6-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="e41a6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e41a6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e41a6-113">Nuevo texto para el control.</span><span class="sxs-lookup"><span data-stu-id="e41a6-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e41a6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e41a6-114">Return value</span></span>

<span data-ttu-id="e41a6-115">Este mensaje no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e41a6-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e41a6-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e41a6-116">Remarks</span></span>

<span data-ttu-id="e41a6-117">La macro correspondiente es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="e41a6-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="e41a6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e41a6-118">Requirements</span></span>



| <span data-ttu-id="e41a6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e41a6-119">Requirement</span></span> | <span data-ttu-id="e41a6-120">Value</span><span class="sxs-lookup"><span data-stu-id="e41a6-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e41a6-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e41a6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e41a6-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e41a6-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e41a6-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e41a6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e41a6-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e41a6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e41a6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e41a6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e41a6-126"><dt>Commdlg.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e41a6-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e41a6-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e41a6-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e41a6-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e41a6-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e41a6-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="e41a6-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="e41a6-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="e41a6-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="e41a6-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="e41a6-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="e41a6-132">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="e41a6-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e41a6-133">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="e41a6-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

