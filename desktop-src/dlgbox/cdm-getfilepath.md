---
title: Mensaje de CDM_GETFILEPATH (commdlg. h)
description: Recupera la ruta de acceso y el nombre de archivo del archivo seleccionado en un cuadro de diálogo abrir o guardar como de estilo del explorador.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- CDM_GETFILEPATH cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b7cc278d1d5a2305b3d2a311ce9c82886f9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996868"
---
# <a name="cdm_getfilepath-message"></a><span data-ttu-id="6e851-104">\_Mensaje GETFILEPATH CDM</span><span class="sxs-lookup"><span data-stu-id="6e851-104">CDM\_GETFILEPATH message</span></span>

<span data-ttu-id="6e851-105">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6e851-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="6e851-106">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="6e851-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="6e851-107">Recupera la ruta de acceso y el nombre de archivo del archivo seleccionado en un cuadro de diálogo **abrir** o **Guardar como** de estilo del explorador.</span><span class="sxs-lookup"><span data-stu-id="6e851-107">Retrieves the path and file name of the selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="6e851-108">El cuadro de diálogo se debe haber creado con la marca **OFN \_ Explorer** ; de lo contrario, se produce un error en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6e851-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a><span data-ttu-id="6e851-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e851-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e851-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e851-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e851-111">Tamaño, en caracteres, del búfer *lParam* .</span><span class="sxs-lookup"><span data-stu-id="6e851-111">The size, in characters, of the *lParam* buffer.</span></span> <span data-ttu-id="6e851-112">En la versión ANSI, es el número de bytes; para la versión Unicode, es el número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6e851-112">For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="6e851-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e851-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e851-114">Puntero al búfer que recibe el nombre de archivo y la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="6e851-114">A pointer to the buffer that receives the file name and path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e851-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e851-115">Return value</span></span>

<span data-ttu-id="6e851-116">Si el mensaje se realiza correctamente, el valor devuelto es el tamaño, en caracteres, del nombre de archivo y la cadena de ruta de acceso, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="6e851-116">If the message succeeds, the return value is the size, in characters, of the file name and path string, including the terminating NULL character.</span></span> <span data-ttu-id="6e851-117">Es el número de bytes o caracteres copiados en el búfer o el tamaño de búfer necesario si el búfer es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="6e851-117">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="6e851-118">Si se produce un error, el valor devuelto es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="6e851-118">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e851-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e851-119">Remarks</span></span>

<span data-ttu-id="6e851-120">La macro correspondiente es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="6e851-120">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="6e851-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e851-121">Requirements</span></span>



| <span data-ttu-id="6e851-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e851-122">Requirement</span></span> | <span data-ttu-id="6e851-123">Value</span><span class="sxs-lookup"><span data-stu-id="6e851-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e851-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e851-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6e851-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6e851-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6e851-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e851-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6e851-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e851-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e851-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e851-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e851-129"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e851-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e851-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e851-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e851-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6e851-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6e851-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="6e851-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="6e851-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="6e851-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="6e851-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="6e851-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="6e851-135">**Vista**</span><span class="sxs-lookup"><span data-stu-id="6e851-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6e851-136">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="6e851-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

