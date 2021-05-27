---
title: CDM_GETFOLDERIDLIST mensaje (Commdlg.h)
description: Recupera la dirección de la lista de identificadores de elemento correspondiente a la carpeta que un cuadro de diálogo Abrir o Guardar como del estilo explorador tiene abierto actualmente.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST cuadro de diálogo de mensaje
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3ffff4f80dc21ed685e589ed4780b43592c2d2
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549710"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="04071-104">Mensaje \_ GETFOLDERIDLIST de CDM</span><span class="sxs-lookup"><span data-stu-id="04071-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="04071-105">\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="04071-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="04071-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]</span><span class="sxs-lookup"><span data-stu-id="04071-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="04071-107">Recupera la dirección de la lista de identificadores de  elemento correspondiente a la carpeta que un cuadro de diálogo Abrir o Guardar **como** del estilo explorador tiene abierto actualmente.</span><span class="sxs-lookup"><span data-stu-id="04071-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="04071-108">El cuadro de diálogo debe haber sido creado con la **marca OFN \_ EXPLORER;** de lo contrario, se produce un error en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="04071-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="04071-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04071-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04071-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04071-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04071-111">Tamaño, en bytes, del búfer *lParam.*</span><span class="sxs-lookup"><span data-stu-id="04071-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="04071-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04071-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04071-113">Puntero al búfer que recibe la lista de identificadores de elemento.</span><span class="sxs-lookup"><span data-stu-id="04071-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04071-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04071-114">Return value</span></span>

<span data-ttu-id="04071-115">Si el mensaje se realiza correctamente, el valor devuelto es el tamaño, en bytes, de la lista de identificadores de elemento.</span><span class="sxs-lookup"><span data-stu-id="04071-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="04071-116">Este es el número de bytes copiados en el búfer o el tamaño de búfer necesario si el búfer es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="04071-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="04071-117">Si se produce un error, el valor devuelto es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="04071-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="04071-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04071-118">Remarks</span></span>

<span data-ttu-id="04071-119">La macro correspondiente es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="04071-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="04071-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04071-120">Requirements</span></span>



| <span data-ttu-id="04071-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="04071-121">Requirement</span></span> | <span data-ttu-id="04071-122">Value</span><span class="sxs-lookup"><span data-stu-id="04071-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04071-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04071-123">Minimum supported client</span></span><br/> | <span data-ttu-id="04071-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="04071-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="04071-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04071-125">Minimum supported server</span></span><br/> | <span data-ttu-id="04071-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04071-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="04071-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04071-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="04071-128"><dt>Commdlg.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="04071-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04071-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="04071-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="04071-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="04071-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="04071-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="04071-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="04071-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="04071-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="04071-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="04071-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="04071-134">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="04071-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="04071-135">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="04071-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

