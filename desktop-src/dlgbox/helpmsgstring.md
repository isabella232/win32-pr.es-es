---
title: Mensaje HELPMSGSTRING (commdlg. h)
description: Un cuadro de diálogo común envía el mensaje registrado HELPMSGSTRING al procedimiento de ventana de la ventana propietaria cuando el usuario hace clic en el botón ayuda.
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Cuadros de diálogo de mensaje de HELPMSGSTRING
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3f7a883f50b06c8d142cb83bedf0bfa2920191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151063"
---
# <a name="helpmsgstring-message"></a><span data-ttu-id="b7687-104">Mensaje HELPMSGSTRING</span><span class="sxs-lookup"><span data-stu-id="b7687-104">HELPMSGSTRING message</span></span>

<span data-ttu-id="b7687-105">Un cuadro de diálogo común envía el mensaje registrado **HELPMSGSTRING** al procedimiento de ventana de la ventana propietaria cuando el usuario hace clic en el botón **ayuda** .</span><span class="sxs-lookup"><span data-stu-id="b7687-105">A common dialog box sends the **HELPMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Help** button.</span></span>


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a><span data-ttu-id="b7687-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7687-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7687-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7687-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7687-108">Identificador del cuadro de diálogo común.</span><span class="sxs-lookup"><span data-stu-id="b7687-108">A handle to the common dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b7687-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7687-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7687-110">Puntero a la estructura de inicialización del cuadro de diálogo común.</span><span class="sxs-lookup"><span data-stu-id="b7687-110">A pointer to the initialization structure for the common dialog box.</span></span> <span data-ttu-id="b7687-111">Esta estructura puede ser una estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) o [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .</span><span class="sxs-lookup"><span data-stu-id="b7687-111">This structure can be a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) or [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7687-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7687-112">Return value</span></span>

<span data-ttu-id="b7687-113">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="b7687-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7687-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7687-114">Remarks</span></span>

<span data-ttu-id="b7687-115">Debe especificar la constante **HELPMSGSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b7687-115">You must specify the **HELPMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="b7687-116">Al crear el cuadro de diálogo, use el miembro **hwndOwner** de la estructura de inicialización para identificar la ventana que recibirá mensajes **HELPMSGSTRING** .</span><span class="sxs-lookup"><span data-stu-id="b7687-116">When you create the dialog box, use the **hwndOwner** member of the initialization structure to identify the window to receive **HELPMSGSTRING** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7687-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7687-117">Requirements</span></span>



| <span data-ttu-id="b7687-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7687-118">Requirement</span></span> | <span data-ttu-id="b7687-119">Value</span><span class="sxs-lookup"><span data-stu-id="b7687-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7687-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7687-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b7687-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b7687-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b7687-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7687-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b7687-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b7687-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b7687-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7687-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7687-125"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7687-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b7687-126">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="b7687-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b7687-127">**HELPMSGSTRINGW** (Unicode) y **HELPMSGSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b7687-127">**HELPMSGSTRINGW** (Unicode) and **HELPMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="b7687-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7687-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b7687-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b7687-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b7687-130">**ayuda de CDN \_**</span><span class="sxs-lookup"><span data-stu-id="b7687-130">**CDN\_HELP**</span></span>](cdn-help.md)
</dt> <dt>

[<span data-ttu-id="b7687-131">**LAS CHOOSECOLOR.**</span><span class="sxs-lookup"><span data-stu-id="b7687-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="b7687-132">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="b7687-132">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="b7687-133">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="b7687-133">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="b7687-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="b7687-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="b7687-135">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="b7687-135">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[<span data-ttu-id="b7687-136">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="b7687-136">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="b7687-137">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="b7687-137">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="b7687-138">**Vista**</span><span class="sxs-lookup"><span data-stu-id="b7687-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b7687-139">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="b7687-139">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

