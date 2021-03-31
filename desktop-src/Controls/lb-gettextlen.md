---
title: Mensaje de LB_GETTEXTLEN (Winuser. h)
description: Obtiene la longitud de una cadena en un cuadro de lista.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- LB_GETTEXTLEN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150195"
---
# <a name="lb_gettextlen-message"></a><span data-ttu-id="a1fac-104">\_Mensaje lb GETTEXTLEN</span><span class="sxs-lookup"><span data-stu-id="a1fac-104">LB\_GETTEXTLEN message</span></span>

<span data-ttu-id="a1fac-105">Obtiene la longitud de una cadena en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="a1fac-105">Gets the length of a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1fac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1fac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1fac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1fac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fac-108">Índice de base cero de la cadena.</span><span class="sxs-lookup"><span data-stu-id="a1fac-108">The zero-based index of the string.</span></span>

<span data-ttu-id="a1fac-109">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a1fac-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="a1fac-110">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="a1fac-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="a1fac-111">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="a1fac-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="a1fac-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1fac-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fac-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a1fac-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1fac-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1fac-114">Return value</span></span>

<span data-ttu-id="a1fac-115">El valor devuelto es la longitud de la cadena, en **TCHAR** s, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="a1fac-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="a1fac-116">En determinadas condiciones, este valor puede ser realmente mayor que la longitud del texto.</span><span class="sxs-lookup"><span data-stu-id="a1fac-116">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="a1fac-117">Para obtener más información, vea la sección Comentarios que se muestra más adelante.</span><span class="sxs-lookup"><span data-stu-id="a1fac-117">For more information, see the following Remarks section.</span></span>

<span data-ttu-id="a1fac-118">Si el parámetro *wParam* no especifica un índice válido, el valor devuelto es lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="a1fac-118">If the *wParam* parameter does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1fac-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1fac-119">Remarks</span></span>

<span data-ttu-id="a1fac-120">En determinadas condiciones, el valor devuelto es mayor que la longitud real del texto.</span><span class="sxs-lookup"><span data-stu-id="a1fac-120">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="a1fac-121">Esto sucede con ciertas mezclas de ANSI y Unicode, y se debe a que el sistema operativo permite la existencia de caracteres de juegos de caracteres de doble byte (DBCS) en el texto.</span><span class="sxs-lookup"><span data-stu-id="a1fac-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="a1fac-122">Sin embargo, el valor devuelto siempre será al menos tan grande como la longitud real del texto; por tanto, se puede usar siempre para guiar la asignación de búfer.</span><span class="sxs-lookup"><span data-stu-id="a1fac-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="a1fac-123">Este comportamiento puede producirse cuando una aplicación usa funciones ANSI y cuadros de diálogo comunes, que usan Unicode.</span><span class="sxs-lookup"><span data-stu-id="a1fac-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="a1fac-124">Para obtener la longitud exacta del texto, use los mensajes [**de \_ WM gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)o [**CB \_ GETLBTEXT**](cb-getlbtext.md) , o la función [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="a1fac-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="a1fac-125">Si el cuadro de lista tiene un estilo dibujado por el propietario, pero no el estilo [**lb \_ HASSTRINGS**](list-box-styles.md) , el valor devuelto siempre es el tamaño, en bytes, de un valor **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="a1fac-125">If the list box has an owner-drawn style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the return value is always the size, in bytes, of a **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1fac-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1fac-126">Requirements</span></span>



| <span data-ttu-id="a1fac-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1fac-127">Requirement</span></span> | <span data-ttu-id="a1fac-128">Value</span><span class="sxs-lookup"><span data-stu-id="a1fac-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1fac-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1fac-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a1fac-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a1fac-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a1fac-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1fac-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a1fac-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1fac-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a1fac-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1fac-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1fac-134"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1fac-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1fac-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1fac-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1fac-136">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a1fac-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a1fac-137">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="a1fac-137">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="a1fac-138">**\_apgettext GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="a1fac-138">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="a1fac-139">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="a1fac-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a1fac-140">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="a1fac-140">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="a1fac-141">**GETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a1fac-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

