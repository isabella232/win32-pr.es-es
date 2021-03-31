---
title: Mensaje de CB_GETEDITSEL (Winuser. h)
description: Obtiene las posiciones de caracteres inicial y final de la selección actual en el control de edición de un cuadro combinado.
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- CB_GETEDITSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319ce4a3c7a5a61903d4fc3bf04eed223e749787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079369"
---
# <a name="cb_geteditsel-message"></a><span data-ttu-id="312f9-104">\_Mensaje GETEDITSEL CB</span><span class="sxs-lookup"><span data-stu-id="312f9-104">CB\_GETEDITSEL message</span></span>

<span data-ttu-id="312f9-105">Obtiene las posiciones de caracteres inicial y final de la selección actual en el control de edición de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="312f9-105">Gets the starting and ending character positions of the current selection in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="312f9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="312f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="312f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="312f9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="312f9-108">Un puntero a un valor **DWORD** que recibe la posición inicial de la selección.</span><span class="sxs-lookup"><span data-stu-id="312f9-108">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="312f9-109">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="312f9-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="312f9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="312f9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="312f9-111">Un puntero a un valor **DWORD** que recibe la posición final de la selección.</span><span class="sxs-lookup"><span data-stu-id="312f9-111">A pointer to a **DWORD** value that receives the ending position of the selection.</span></span> <span data-ttu-id="312f9-112">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="312f9-112">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="312f9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="312f9-113">Return value</span></span>

<span data-ttu-id="312f9-114">El valor devuelto es un valor **DWORD** basado en cero con la posición inicial de la selección en [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y con la posición final del primer carácter después del último carácter seleccionado en el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="312f9-114">The return value is a zero-based **DWORD** value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and with the ending position of the first character after the last selected character in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="312f9-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="312f9-115">Examples</span></span>

<span data-ttu-id="312f9-116">En el ejemplo de código siguiente se muestran dos maneras de recuperar el intervalo de selección actual.</span><span class="sxs-lookup"><span data-stu-id="312f9-116">The following code example shows two ways of retrieving the current selection range.</span></span>


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



## <a name="requirements"></a><span data-ttu-id="312f9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="312f9-117">Requirements</span></span>



| <span data-ttu-id="312f9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="312f9-118">Requirement</span></span> | <span data-ttu-id="312f9-119">Value</span><span class="sxs-lookup"><span data-stu-id="312f9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="312f9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="312f9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="312f9-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="312f9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="312f9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="312f9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="312f9-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="312f9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="312f9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="312f9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="312f9-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="312f9-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="312f9-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="312f9-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="312f9-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="312f9-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="312f9-128">**CB \_ SETEDITSEL**</span><span class="sxs-lookup"><span data-stu-id="312f9-128">**CB\_SETEDITSEL**</span></span>](cb-seteditsel.md)
</dt> <dt>

<span data-ttu-id="312f9-129">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="312f9-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="312f9-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="312f9-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="312f9-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="312f9-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

