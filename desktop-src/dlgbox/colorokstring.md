---
title: Mensaje COLOROKSTRING (commdlg. h)
description: Un cuadro de diálogo de color envía el mensaje registrado COLOROKSTRING al procedimiento de enlace, CCHookProc, cuando el usuario selecciona un color y hace clic en el botón Aceptar.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Cuadros de diálogo de mensaje de COLOROKSTRING
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150275"
---
# <a name="colorokstring-message"></a><span data-ttu-id="f4b34-104">Mensaje COLOROKSTRING</span><span class="sxs-lookup"><span data-stu-id="f4b34-104">COLOROKSTRING message</span></span>

<span data-ttu-id="f4b34-105">Un cuadro de diálogo de **color** envía el mensaje registrado **COLOROKSTRING** al procedimiento de enlace, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), cuando el usuario selecciona un color y hace clic en el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="f4b34-105">A **Color** dialog box sends the **COLOROKSTRING** registered message to your hook procedure, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), when the user selects a color and clicks the **OK** button.</span></span> <span data-ttu-id="f4b34-106">El procedimiento de enlace puede aceptar el color y permitir que el cuadro de diálogo se cierre, o bien rechazar el color y forzar que el cuadro de diálogo permanezca abierto.</span><span class="sxs-lookup"><span data-stu-id="f4b34-106">The hook procedure can accept the color and allow the dialog box to close, or reject the color and force the dialog box to remain open.</span></span>


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a><span data-ttu-id="f4b34-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4b34-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4b34-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4b34-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4b34-109">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f4b34-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4b34-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4b34-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4b34-111">Puntero a una estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) .</span><span class="sxs-lookup"><span data-stu-id="f4b34-111">A pointer to a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure.</span></span> <span data-ttu-id="f4b34-112">El miembro **rgbResult** de esta estructura contiene el valor de color RGB del color seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f4b34-112">The **rgbResult** member of this structure contains the RGB color value of the selected color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4b34-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4b34-113">Return value</span></span>

<span data-ttu-id="f4b34-114">Si el procedimiento de enlace devuelve cero, el cuadro de diálogo **color** acepta el color seleccionado y se cierra.</span><span class="sxs-lookup"><span data-stu-id="f4b34-114">If the hook procedure returns zero, the **Color** dialog box accepts the selected color and closes.</span></span>

<span data-ttu-id="f4b34-115">Si el procedimiento de enlace devuelve un valor distinto de cero, el cuadro de diálogo de **color** rechaza el color seleccionado y permanece abierto.</span><span class="sxs-lookup"><span data-stu-id="f4b34-115">If the hook procedure returns a nonzero value, the **Color** dialog box rejects the selected color and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4b34-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4b34-116">Remarks</span></span>

<span data-ttu-id="f4b34-117">El procedimiento de enlace debe especificar la constante **COLOROKSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f4b34-117">The hook procedure must specify the **COLOROKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier of the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4b34-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4b34-118">Requirements</span></span>



| <span data-ttu-id="f4b34-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4b34-119">Requirement</span></span> | <span data-ttu-id="f4b34-120">Value</span><span class="sxs-lookup"><span data-stu-id="f4b34-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4b34-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4b34-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f4b34-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f4b34-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f4b34-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4b34-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f4b34-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f4b34-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f4b34-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4b34-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4b34-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4b34-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f4b34-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f4b34-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f4b34-128">**COLOROKSTRINGW** (Unicode) y **COLOROKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f4b34-128">**COLOROKSTRINGW** (Unicode) and **COLOROKSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="f4b34-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4b34-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4b34-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f4b34-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f4b34-131">**LAS CHOOSECOLOR.**</span><span class="sxs-lookup"><span data-stu-id="f4b34-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="f4b34-132">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="f4b34-132">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="f4b34-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f4b34-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f4b34-134">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="f4b34-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

