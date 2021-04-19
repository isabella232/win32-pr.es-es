---
title: CDM_SETDEFEXT mensaje (Commdlg.h)
description: Establece la extensión de nombre de archivo predeterminada para un cuadro de diálogo Abrir o Guardar como de estilo explorador.
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- CDM_SETDEFEXT diálogo de mensaje
topic_type:
- apiref
api_name:
- CDM_SETDEFEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bd5706e0bccf0b61c0737ef54d6e227e5593bc9
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590862"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="77876-104">Mensaje \_ SETDEFEXT de CDM</span><span class="sxs-lookup"><span data-stu-id="77876-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="77876-105">\[A partir de Windows Vista, **los** cuadros **de** diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo de elemento común](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="77876-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="77876-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]</span><span class="sxs-lookup"><span data-stu-id="77876-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="77876-107">Establece la extensión de nombre de  archivo predeterminada para un cuadro de diálogo Abrir o **Guardar como** de estilo explorador.</span><span class="sxs-lookup"><span data-stu-id="77876-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="77876-108">El cuadro de diálogo se debe haber creado con la **marca OFN \_ EXPLORER;** de lo contrario, se produce un error en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="77876-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="77876-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77876-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77876-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77876-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77876-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="77876-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77876-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77876-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77876-113">Puntero a la nueva extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="77876-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="77876-114">No debe incluir el punto (.).</span><span class="sxs-lookup"><span data-stu-id="77876-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77876-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77876-115">Return value</span></span>

<span data-ttu-id="77876-116">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="77876-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77876-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77876-117">Remarks</span></span>

<span data-ttu-id="77876-118">La macro correspondiente es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="77876-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="77876-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77876-119">Requirements</span></span>



| <span data-ttu-id="77876-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="77876-120">Requirement</span></span> | <span data-ttu-id="77876-121">Value</span><span class="sxs-lookup"><span data-stu-id="77876-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77876-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77876-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77876-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="77876-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="77876-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77876-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77876-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="77876-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="77876-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77876-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="77876-127"><dt>Commdlg.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="77876-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77876-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="77876-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="77876-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="77876-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="77876-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="77876-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="77876-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="77876-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="77876-132">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="77876-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="77876-133">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="77876-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="77876-134">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="77876-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

