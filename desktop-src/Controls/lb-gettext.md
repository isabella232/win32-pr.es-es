---
title: Mensaje de LB_GETTEXT (Winuser. h)
description: Obtiene una cadena de un cuadro de lista.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- LB_GETTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492149"
---
# <a name="lb_gettext-message"></a><span data-ttu-id="970a4-104">Mensaje de LB \_ GETTEXT</span><span class="sxs-lookup"><span data-stu-id="970a4-104">LB\_GETTEXT message</span></span>

<span data-ttu-id="970a4-105">Obtiene una cadena de un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="970a4-105">Gets a string from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="970a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="970a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="970a4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="970a4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="970a4-108">Índice de base cero de la cadena que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="970a4-108">The zero-based index of the string to retrieve.</span></span>

<span data-ttu-id="970a4-109">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="970a4-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="970a4-110">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="970a4-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="970a4-111">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="970a4-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="970a4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="970a4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="970a4-113">Puntero al búfer que recibirá la cadena; es de tipo **LPTSTR** que se convierte posteriormente en **lParam**.</span><span class="sxs-lookup"><span data-stu-id="970a4-113">A pointer to the buffer that will receive the string; it is type **LPTSTR** which is subsequently cast to an **LPARAM**.</span></span> <span data-ttu-id="970a4-114">El búfer debe tener espacio suficiente para la cadena y un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="970a4-114">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="970a4-115">Se puede enviar un mensaje de [**lb \_ GETTEXTLEN**](lb-gettextlen.md) antes del mensaje de la extensión de **equilibro de lb \_** para recuperar la longitud, en **TCHAR** s, de la cadena.</span><span class="sxs-lookup"><span data-stu-id="970a4-115">An [**LB\_GETTEXTLEN**](lb-gettextlen.md) message can be sent before the **LB\_GETTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="970a4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="970a4-116">Return value</span></span>

<span data-ttu-id="970a4-117">El valor devuelto es la longitud de la cadena, en **TCHAR** s, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="970a4-117">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="970a4-118">Si *wParam* no especifica un índice válido, el valor devuelto es lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="970a4-118">If *wParam* does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="970a4-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="970a4-119">Remarks</span></span>

<span data-ttu-id="970a4-120">Si el cuadro de lista tiene un estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , el búfer al que apunta el parámetro *lParam* recibe el valor asociado al elemento (los datos del elemento).</span><span class="sxs-lookup"><span data-stu-id="970a4-120">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the buffer pointed to by the *lParam* parameter receives the value associated with the item (the item data).</span></span>

## <a name="requirements"></a><span data-ttu-id="970a4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="970a4-121">Requirements</span></span>



| <span data-ttu-id="970a4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="970a4-122">Requirement</span></span> | <span data-ttu-id="970a4-123">Value</span><span class="sxs-lookup"><span data-stu-id="970a4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="970a4-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="970a4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="970a4-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="970a4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="970a4-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="970a4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="970a4-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="970a4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="970a4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="970a4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="970a4-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="970a4-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="970a4-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="970a4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="970a4-131">**LB \_ GETTEXTLEN**</span><span class="sxs-lookup"><span data-stu-id="970a4-131">**LB\_GETTEXTLEN**</span></span>](lb-gettextlen.md)
</dt> </dl>

 

 





