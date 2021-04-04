---
title: Mensaje SETRGBSTRING (commdlg. h)
description: El procedimiento de enlace de un cuadro de diálogo de color, CCHookProc, puede enviar el mensaje registrado de SETRGBSTRING al cuadro de diálogo para establecer la selección de color actual.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Cuadros de diálogo de mensaje de SETRGBSTRING
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803091"
---
# <a name="setrgbstring-message"></a><span data-ttu-id="4bece-104">Mensaje SETRGBSTRING</span><span class="sxs-lookup"><span data-stu-id="4bece-104">SETRGBSTRING message</span></span>

<span data-ttu-id="4bece-105">El procedimiento de enlace de un cuadro de diálogo de **color** , [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), puede enviar el mensaje registrado de **SETRGBSTRING** al cuadro de diálogo para establecer la selección de color actual.</span><span class="sxs-lookup"><span data-stu-id="4bece-105">The hook procedure of a **Color** dialog box, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), can send the **SETRGBSTRING** registered message to the dialog box to set the current color selection.</span></span>


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a><span data-ttu-id="4bece-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bece-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bece-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4bece-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4bece-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4bece-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4bece-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4bece-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4bece-110">Valor RGB del color que se va a seleccionar en el cuadro de diálogo de **color** .</span><span class="sxs-lookup"><span data-stu-id="4bece-110">The RGB value of the color to select in the **Color** dialog box.</span></span> <span data-ttu-id="4bece-111">Puede usar la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) para especificar las intensidades rojo, verde y azul de un valor de color RGB.</span><span class="sxs-lookup"><span data-stu-id="4bece-111">You can use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro to specify the red, green, and blue intensities of an RGB color value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bece-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bece-112">Return value</span></span>

<span data-ttu-id="4bece-113">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="4bece-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bece-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bece-114">Remarks</span></span>

<span data-ttu-id="4bece-115">Si *lParam* coincide con uno de los colores básicos o con uno de los 16 colores personalizados, el procedimiento de cuadro de diálogo selecciona ese color.</span><span class="sxs-lookup"><span data-stu-id="4bece-115">If *lParam* matches one of the basic colors or one of the 16 custom colors, the dialog box procedure selects that color.</span></span> <span data-ttu-id="4bece-116">El procedimiento de cuadro de diálogo también actualiza todos los controles de la extensión de color personalizada del cuadro de diálogo **color** , si está abierto.</span><span class="sxs-lookup"><span data-stu-id="4bece-116">The dialog box procedure also updates all the controls in the custom color extension of the **Color** dialog box, if it is open.</span></span>

<span data-ttu-id="4bece-117">Si *lParam* no coincide con un color básico o personalizado, el procedimiento del cuadro de diálogo no cambia la selección de color actual, pero actualiza los controles de color personalizados, si están visibles.</span><span class="sxs-lookup"><span data-stu-id="4bece-117">If *lParam* does not match a basic or custom color, the dialog box procedure does not change the current color selection, but it does update the custom color controls, if they are visible.</span></span>

## <a name="examples"></a><span data-ttu-id="4bece-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4bece-118">Examples</span></span>

<span data-ttu-id="4bece-119">En el código de ejemplo siguiente se obtiene el identificador de mensaje **SETRGBSTRING** y, a continuación, se establece la selección de color en azul.</span><span class="sxs-lookup"><span data-stu-id="4bece-119">The following sample code gets the **SETRGBSTRING** message identifier and then sets the color selection to blue.</span></span>


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a><span data-ttu-id="4bece-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bece-120">Requirements</span></span>



| <span data-ttu-id="4bece-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bece-121">Requirement</span></span> | <span data-ttu-id="4bece-122">Value</span><span class="sxs-lookup"><span data-stu-id="4bece-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bece-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bece-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4bece-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4bece-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4bece-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bece-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4bece-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4bece-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4bece-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bece-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bece-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4bece-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4bece-129">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="4bece-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4bece-130">**SETRGBSTRINGW** (Unicode) y **SETRGBSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4bece-130">**SETRGBSTRINGW** (Unicode) and **SETRGBSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="4bece-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bece-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="4bece-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4bece-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4bece-133">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="4bece-133">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="4bece-134">**RGB**</span><span class="sxs-lookup"><span data-stu-id="4bece-134">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[<span data-ttu-id="4bece-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="4bece-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

<span data-ttu-id="4bece-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="4bece-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4bece-137">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="4bece-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

