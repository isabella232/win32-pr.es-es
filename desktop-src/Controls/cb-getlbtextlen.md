---
title: Mensaje de CB_GETLBTEXTLEN (Winuser. h)
description: Obtiene la longitud, en caracteres, de una cadena en la lista de un cuadro combinado.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- CB_GETLBTEXTLEN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996377"
---
# <a name="cb_getlbtextlen-message"></a><span data-ttu-id="b68f6-104">\_Mensaje GETLBTEXTLEN CB</span><span class="sxs-lookup"><span data-stu-id="b68f6-104">CB\_GETLBTEXTLEN message</span></span>

<span data-ttu-id="b68f6-105">Obtiene la longitud, en caracteres, de una cadena en la lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="b68f6-105">Gets the length, in characters, of a string in the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b68f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b68f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b68f6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b68f6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b68f6-108">Índice de base cero de la cadena.</span><span class="sxs-lookup"><span data-stu-id="b68f6-108">The zero-based index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="b68f6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b68f6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b68f6-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b68f6-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b68f6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b68f6-111">Return value</span></span>

<span data-ttu-id="b68f6-112">El valor devuelto es la longitud de la cadena, en **TCHAR** s, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="b68f6-112">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="b68f6-113">Si una cadena ANSI es el número de bytes, y si es una cadena Unicode, es el número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b68f6-113">If an ANSI string this is the number of bytes, and if it is a Unicode string this is the number of characters.</span></span> <span data-ttu-id="b68f6-114">En determinadas condiciones, este valor puede ser realmente mayor que la longitud del texto.</span><span class="sxs-lookup"><span data-stu-id="b68f6-114">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="b68f6-115">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b68f6-115">For more information, see the Remarks section.</span></span>

<span data-ttu-id="b68f6-116">Si el parámetro *wParam* no especifica un índice válido, el valor devuelto es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="b68f6-116">If the *wParam* parameter does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="b68f6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b68f6-117">Remarks</span></span>

<span data-ttu-id="b68f6-118">En determinadas condiciones, el valor devuelto es mayor que la longitud real del texto.</span><span class="sxs-lookup"><span data-stu-id="b68f6-118">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="b68f6-119">Esto sucede con ciertas mezclas de ANSI y Unicode, y se debe a que el sistema operativo permite la existencia de caracteres de juegos de caracteres de doble byte (DBCS) en el texto.</span><span class="sxs-lookup"><span data-stu-id="b68f6-119">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="b68f6-120">Sin embargo, el valor devuelto siempre será al menos tan grande como la longitud real del texto; por lo tanto, siempre puede usarlo para guiar la asignación de búfer.</span><span class="sxs-lookup"><span data-stu-id="b68f6-120">The return value, however, will always be at least as large as the actual length of the text; so you can always use it to guide buffer allocation.</span></span> <span data-ttu-id="b68f6-121">Este comportamiento puede producirse cuando una aplicación usa funciones ANSI y cuadros de diálogo comunes, que usan Unicode.</span><span class="sxs-lookup"><span data-stu-id="b68f6-121">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="b68f6-122">Para obtener la longitud exacta del texto, use los mensajes [**de \_ WM gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)o [**CB \_ GETLBTEXT**](cb-getlbtext.md) , o la función [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="b68f6-122">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b68f6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b68f6-123">Requirements</span></span>



| <span data-ttu-id="b68f6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b68f6-124">Requirement</span></span> | <span data-ttu-id="b68f6-125">Value</span><span class="sxs-lookup"><span data-stu-id="b68f6-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b68f6-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b68f6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b68f6-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b68f6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b68f6-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b68f6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b68f6-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b68f6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b68f6-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b68f6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b68f6-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b68f6-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b68f6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b68f6-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="b68f6-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b68f6-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b68f6-134">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="b68f6-134">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="b68f6-135">**\_apgettext GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="b68f6-135">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="b68f6-136">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="b68f6-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b68f6-137">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="b68f6-137">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="b68f6-138">**GETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="b68f6-138">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

