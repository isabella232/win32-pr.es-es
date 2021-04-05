---
title: Mensaje de WM_CHOOSEFONT_SETLOGFONT (commdlg. h)
description: Una aplicación envía el \_ mensaje de CHOOSEFONT \_ SETLOGFONT de WM a un cuadro de diálogo de fuente para establecer la información de fuente lógica actual.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- WM_CHOOSEFONT_SETLOGFONT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803086"
---
# <a name="wm_choosefont_setlogfont-message"></a><span data-ttu-id="c7e54-104">\_Mensaje SETLOGFONT de CHOOSEFONT de WM \_</span><span class="sxs-lookup"><span data-stu-id="c7e54-104">WM\_CHOOSEFONT\_SETLOGFONT message</span></span>

<span data-ttu-id="c7e54-105">Una aplicación envía el mensaje de **\_ CHOOSEFONT \_ SETLOGFONT de WM** a un cuadro de diálogo de **fuente** para establecer la información de fuente lógica actual.</span><span class="sxs-lookup"><span data-stu-id="c7e54-105">An application sends the **WM\_CHOOSEFONT\_SETLOGFONT** message to a **Font** dialog box to set the current logical font information.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a><span data-ttu-id="c7e54-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7e54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7e54-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7e54-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7e54-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c7e54-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7e54-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7e54-110">Puntero a una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contiene información sobre la fuente lógica actual.</span><span class="sxs-lookup"><span data-stu-id="c7e54-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the current logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7e54-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7e54-111">Return value</span></span>

<span data-ttu-id="c7e54-112">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c7e54-112">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7e54-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7e54-113">Remarks</span></span>

<span data-ttu-id="c7e54-114">Cuando llame a la función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para crear un cuadro de diálogo de **fuente** , puede usar el miembro **lpLogFont** de la estructura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contenga valores iniciales para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7e54-114">When you call the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to create a **Font** dialog box, you can use the **lpLogFont** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure containing initial values for the dialog box.</span></span> <span data-ttu-id="c7e54-115">Use el **mensaje \_ CHOOSEFONT de \_ SETLOGFONT de WM** para especificar una estructura **LOGFONT** con valores diferentes mientras el cuadro de diálogo **fuente** está abierto.</span><span class="sxs-lookup"><span data-stu-id="c7e54-115">Use the **WM\_CHOOSEFONT\_SETLOGFONT** message to specify a **LOGFONT** structure with different values while the **Font** dialog box is open.</span></span>

<span data-ttu-id="c7e54-116">Normalmente, se enviará el mensaje de **\_ CHOOSEFONT \_ SETLOGFONT de WM** desde un procedimiento de enlace [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .</span><span class="sxs-lookup"><span data-stu-id="c7e54-116">Typically, you would send the **WM\_CHOOSEFONT\_SETLOGFONT** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span> <span data-ttu-id="c7e54-117">El procedimiento de enlace también puede enviar los mensajes [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) y [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) .</span><span class="sxs-lookup"><span data-stu-id="c7e54-117">The hook procedure can also send the [**WM\_CHOOSEFONT\_GETLOGFONT**](wm-choosefont-getlogfont.md) and [**WM\_CHOOSEFONT\_SETFLAGS**](wm-choosefont-setflags.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e54-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7e54-118">Requirements</span></span>



| <span data-ttu-id="c7e54-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7e54-119">Requirement</span></span> | <span data-ttu-id="c7e54-120">Value</span><span class="sxs-lookup"><span data-stu-id="c7e54-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e54-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7e54-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e54-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c7e54-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c7e54-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7e54-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e54-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c7e54-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7e54-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7e54-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7e54-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7e54-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7e54-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7e54-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7e54-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c7e54-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c7e54-129">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="c7e54-129">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="c7e54-130">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="c7e54-130">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="c7e54-131">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="c7e54-131">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="c7e54-132">**\_GETLOGFONT CHOOSEFONT \_ WM**</span><span class="sxs-lookup"><span data-stu-id="c7e54-132">**WM\_CHOOSEFONT\_GETLOGFONT**</span></span>](wm-choosefont-getlogfont.md)
</dt> <dt>

[<span data-ttu-id="c7e54-133">**WM \_ CHOOSEFONT \_ SETFLAGS**</span><span class="sxs-lookup"><span data-stu-id="c7e54-133">**WM\_CHOOSEFONT\_SETFLAGS**</span></span>](wm-choosefont-setflags.md)
</dt> <dt>

<span data-ttu-id="c7e54-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c7e54-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7e54-135">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="c7e54-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="c7e54-136">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="c7e54-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c7e54-137">**NDPTECGDI**</span><span class="sxs-lookup"><span data-stu-id="c7e54-137">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

