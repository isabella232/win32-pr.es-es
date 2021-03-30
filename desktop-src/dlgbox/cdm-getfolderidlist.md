---
title: Mensaje de CDM_GETFOLDERIDLIST (commdlg. h)
description: Recupera la dirección de la lista de identificadores de elemento correspondiente a la carpeta que tiene abierto un cuadro de diálogo de estilo de explorador abrir o guardar como.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST cuadros de diálogo de mensaje
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
ms.openlocfilehash: 0b4ac82a628d6fcace6863abb30e5703af02a948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803554"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="6bfcd-104">\_Mensaje GETFOLDERIDLIST CDM</span><span class="sxs-lookup"><span data-stu-id="6bfcd-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="6bfcd-105">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6bfcd-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="6bfcd-106">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="6bfcd-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="6bfcd-107">Recupera la dirección de la lista de identificadores de elemento correspondiente a la carpeta que tiene abierto un cuadro de diálogo de estilo de explorador **abrir** o **Guardar como** .</span><span class="sxs-lookup"><span data-stu-id="6bfcd-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="6bfcd-108">El cuadro de diálogo se debe haber creado con la marca **OFN \_ Explorer** ; de lo contrario, se produce un error en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6bfcd-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="6bfcd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6bfcd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bfcd-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6bfcd-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bfcd-111">Tamaño, en bytes, del búfer *lParam* .</span><span class="sxs-lookup"><span data-stu-id="6bfcd-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6bfcd-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6bfcd-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bfcd-113">Puntero al búfer que recibe la lista de identificadores de elemento.</span><span class="sxs-lookup"><span data-stu-id="6bfcd-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bfcd-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bfcd-114">Return value</span></span>

<span data-ttu-id="6bfcd-115">Si el mensaje se realiza correctamente, el valor devuelto es el tamaño, en bytes, de la lista de identificadores de elemento.</span><span class="sxs-lookup"><span data-stu-id="6bfcd-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="6bfcd-116">Es el número de bytes copiados en el búfer o el tamaño de búfer necesario si el búfer es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="6bfcd-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="6bfcd-117">Si se produce un error, el valor devuelto es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="6bfcd-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bfcd-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6bfcd-118">Remarks</span></span>

<span data-ttu-id="6bfcd-119">La macro correspondiente es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="6bfcd-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="6bfcd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bfcd-120">Requirements</span></span>



| <span data-ttu-id="6bfcd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bfcd-121">Requirement</span></span> | <span data-ttu-id="6bfcd-122">Value</span><span class="sxs-lookup"><span data-stu-id="6bfcd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bfcd-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bfcd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6bfcd-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6bfcd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6bfcd-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bfcd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6bfcd-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6bfcd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6bfcd-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bfcd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bfcd-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bfcd-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bfcd-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bfcd-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="6bfcd-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6bfcd-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6bfcd-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="6bfcd-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="6bfcd-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="6bfcd-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="6bfcd-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="6bfcd-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="6bfcd-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="6bfcd-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6bfcd-135">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="6bfcd-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

