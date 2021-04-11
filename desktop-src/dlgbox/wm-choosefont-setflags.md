---
title: Mensaje de WM_CHOOSEFONT_SETFLAGS (commdlg. h)
description: Una aplicación envía el mensaje de WM \_ CHOOSEFONT \_ SETFLAGS a un cuadro de diálogo fuente para establecer las opciones de presentación del cuadro de diálogo.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- WM_CHOOSEFONT_SETFLAGS cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7abf436311f8a3868b1471c2a10a7ee2e4a3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150686"
---
# <a name="wm_choosefont_setflags-message"></a><span data-ttu-id="76e90-104">Mensaje de WM \_ CHOOSEFONT \_ SETFLAGS</span><span class="sxs-lookup"><span data-stu-id="76e90-104">WM\_CHOOSEFONT\_SETFLAGS message</span></span>

<span data-ttu-id="76e90-105">Una aplicación envía el mensaje de **WM \_ CHOOSEFONT \_ SETFLAGS** a un cuadro de diálogo **fuente** para establecer las opciones de presentación del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="76e90-105">An application sends the **WM\_CHOOSEFONT\_SETFLAGS** message to a **Font** dialog box to set the display options for the dialog box.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a><span data-ttu-id="76e90-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76e90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76e90-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76e90-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76e90-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="76e90-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="76e90-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76e90-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76e90-110">Puntero a una estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) que contiene nuevos valores en el miembro **Flags** .</span><span class="sxs-lookup"><span data-stu-id="76e90-110">A pointer to a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure that contains new settings in the **Flags** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76e90-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76e90-111">Return value</span></span>

<span data-ttu-id="76e90-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="76e90-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76e90-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76e90-113">Remarks</span></span>

<span data-ttu-id="76e90-114">La función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crea un cuadro de diálogo de **fuente** y utiliza una estructura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar los valores iniciales del miembro **Flags** .</span><span class="sxs-lookup"><span data-stu-id="76e90-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box and uses a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify the initial values for the **Flags** member.</span></span> <span data-ttu-id="76e90-115">Use el mensaje **WM \_ CHOOSEFONT \_ SETFLAGS** para especificar valores diferentes para el miembro **Flags** mientras el cuadro de diálogo **fuente** está abierto.</span><span class="sxs-lookup"><span data-stu-id="76e90-115">Use the **WM\_CHOOSEFONT\_SETFLAGS** message to specify different values for the **Flags** member while the **Font** dialog box is open.</span></span>

<span data-ttu-id="76e90-116">Normalmente, debe enviar el mensaje de **WM \_ CHOOSEFONT \_ SETFLAGS** desde un procedimiento de enlace de [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .</span><span class="sxs-lookup"><span data-stu-id="76e90-116">Typically, you should send the **WM\_CHOOSEFONT\_SETFLAGS** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="76e90-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76e90-117">Requirements</span></span>



| <span data-ttu-id="76e90-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="76e90-118">Requirement</span></span> | <span data-ttu-id="76e90-119">Value</span><span class="sxs-lookup"><span data-stu-id="76e90-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76e90-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76e90-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76e90-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="76e90-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="76e90-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76e90-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76e90-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="76e90-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="76e90-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76e90-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="76e90-125"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76e90-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76e90-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="76e90-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="76e90-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="76e90-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="76e90-128">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="76e90-128">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="76e90-129">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="76e90-129">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="76e90-130">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="76e90-130">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

<span data-ttu-id="76e90-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="76e90-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="76e90-132">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="76e90-132">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

