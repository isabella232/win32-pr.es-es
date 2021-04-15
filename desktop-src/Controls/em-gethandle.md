---
title: Mensaje de EM_GETHANDLE (Winuser. h)
description: Obtiene un identificador de la memoria asignada actualmente para el texto de un control de edición multilínea.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- EM_GETHANDLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a466394b48d2d726621e50a7e2c5df2f747f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534684"
---
# <a name="em_gethandle-message"></a><span data-ttu-id="327f3-104">\_Mensaje de GETHANDLE em</span><span class="sxs-lookup"><span data-stu-id="327f3-104">EM\_GETHANDLE message</span></span>

<span data-ttu-id="327f3-105">Obtiene un identificador de la memoria asignada actualmente para el texto de un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="327f3-105">Gets a handle of the memory currently allocated for a multiline edit control's text.</span></span>

## <a name="parameters"></a><span data-ttu-id="327f3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="327f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="327f3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="327f3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="327f3-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="327f3-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="327f3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="327f3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="327f3-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="327f3-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="327f3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="327f3-111">Return value</span></span>

<span data-ttu-id="327f3-112">El valor devuelto es un identificador de memoria que identifica el búfer que contiene el contenido del control de edición.</span><span class="sxs-lookup"><span data-stu-id="327f3-112">The return value is a memory handle identifying the buffer that holds the content of the edit control.</span></span> <span data-ttu-id="327f3-113">Si se produce un error, como el envío del mensaje a un control de edición de una sola línea, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="327f3-113">If an error occurs, such as sending the message to a single-line edit control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="327f3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="327f3-114">Remarks</span></span>

<span data-ttu-id="327f3-115">Si la función se ejecuta correctamente, la aplicación puede tener acceso al contenido del control de edición convirtiendo el valor devuelto en [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) y pasándolo a [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock).</span><span class="sxs-lookup"><span data-stu-id="327f3-115">If the function succeeds, the application can access the contents of the edit control by casting the return value to [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) and passing it to [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock).</span></span> <span data-ttu-id="327f3-116">**LocalLock** devuelve un puntero a un búfer que es una matriz terminada en NULL de **Char** s o **WCHAR** s, dependiendo de si una función ANSI o Unicode creó el control.</span><span class="sxs-lookup"><span data-stu-id="327f3-116">**LocalLock** returns a pointer to a buffer that is a null-terminated array of **CHAR** s or **WCHAR** s, depending on whether an ANSI or Unicode function created the control.</span></span> <span data-ttu-id="327f3-117">Por ejemplo, si se usó [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , el búfer es una matriz de **Char** s, pero si se usó **CreateWindowExW** , el búfer es una matriz de **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="327f3-117">For example, if [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) was used the buffer is an array of **CHAR** s, but if **CreateWindowExW** was used the buffer is an array of **WCHAR** s.</span></span> <span data-ttu-id="327f3-118">Es posible que la aplicación no cambie el contenido del búfer.</span><span class="sxs-lookup"><span data-stu-id="327f3-118">The application may not change the contents of the buffer.</span></span> <span data-ttu-id="327f3-119">Para desbloquear el búfer, la aplicación llama a [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) antes de permitir que el control de edición reciba mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="327f3-119">To unlock the buffer, the application calls [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) before allowing the edit control to receive new messages.</span></span>

> [!Note]  
> <span data-ttu-id="327f3-120">En el caso de Comctl32.dll versión 6, el búfer siempre contiene una matriz de **WCHAR** s, independientemente de si una función ANSI o Unicode creó el control de edición.</span><span class="sxs-lookup"><span data-stu-id="327f3-120">For Comctl32.dll version 6, the buffer always contains an array of **WCHAR** s, regardless of whether an ANSI or Unicode function created the edit control.</span></span> <span data-ttu-id="327f3-121">Para obtener más información sobre las versiones de DLL, vea [versiones de control comunes](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="327f3-121">For more information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

 

<span data-ttu-id="327f3-122">Si la aplicación no puede cumplir las restricciones impuestas por la función **\_ GETHANDLE**, utilice las funciones [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) y [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) para copiar el contenido del control de edición en un búfer proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="327f3-122">If your application cannot abide by the restrictions imposed by **EM\_GETHANDLE**, use the [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) and [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) functions to copy the contents of the edit control into an application-provided buffer.</span></span>

<span data-ttu-id="327f3-123">**Edición enriquecida:** No se admite el mensaje de **\_ GETHANDLE em** .</span><span class="sxs-lookup"><span data-stu-id="327f3-123">**Rich Edit:** The **EM\_GETHANDLE** message is not supported.</span></span> <span data-ttu-id="327f3-124">Los controles Rich Edit no almacenan texto como una matriz de caracteres simple.</span><span class="sxs-lookup"><span data-stu-id="327f3-124">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="327f3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="327f3-125">Requirements</span></span>



| <span data-ttu-id="327f3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="327f3-126">Requirement</span></span> | <span data-ttu-id="327f3-127">Value</span><span class="sxs-lookup"><span data-stu-id="327f3-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="327f3-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="327f3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="327f3-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="327f3-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="327f3-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="327f3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="327f3-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="327f3-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="327f3-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="327f3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="327f3-133"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="327f3-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="327f3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="327f3-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="327f3-135">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="327f3-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="327f3-136">**\_SETHANDLE em**</span><span class="sxs-lookup"><span data-stu-id="327f3-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

<span data-ttu-id="327f3-137">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="327f3-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="327f3-138">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="327f3-138">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="327f3-139">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="327f3-139">**GetWindowTextLength**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="327f3-140">**LocalLock**</span><span class="sxs-lookup"><span data-stu-id="327f3-140">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[<span data-ttu-id="327f3-141">**LocalUnlock**</span><span class="sxs-lookup"><span data-stu-id="327f3-141">**LocalUnlock**</span></span>](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

