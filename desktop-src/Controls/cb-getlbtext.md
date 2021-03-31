---
title: Mensaje de CB_GETLBTEXT (Winuser. h)
description: Obtiene una cadena de la lista de un cuadro combinado.
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- CB_GETLBTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079365"
---
# <a name="cb_getlbtext-message"></a><span data-ttu-id="9e339-104">\_Mensaje GETLBTEXT CB</span><span class="sxs-lookup"><span data-stu-id="9e339-104">CB\_GETLBTEXT message</span></span>

<span data-ttu-id="9e339-105">Obtiene una cadena de la lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="9e339-105">Gets a string from the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e339-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e339-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e339-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e339-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e339-108">Índice de base cero de la cadena que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="9e339-108">The zero-based index of the string to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9e339-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e339-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e339-110">Puntero al búfer que recibe la cadena.</span><span class="sxs-lookup"><span data-stu-id="9e339-110">A pointer to the buffer that receives the string.</span></span> <span data-ttu-id="9e339-111">El búfer debe tener espacio suficiente para la cadena y un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="9e339-111">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="9e339-112">Puede enviar un mensaje [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) antes del mensaje **CB \_ GETLBTEXT** para recuperar la longitud de la cadena en **TCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="9e339-112">You can send a [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) message prior to the **CB\_GETLBTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span> <span data-ttu-id="9e339-113">Si es una cadena ANSI, es el número de bytes, pero si es una cadena Unicode, es el número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9e339-113">If it is an ANSI string this is the number of bytes, but if it is a Unicode string this is the number of characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e339-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e339-114">Return value</span></span>

<span data-ttu-id="9e339-115">El valor devuelto es la longitud de la cadena, en **TCHAR** s, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="9e339-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="9e339-116">Si *wParam* no especifica un índice válido, el valor devuelto es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="9e339-116">If *wParam* does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e339-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e339-117">Remarks</span></span>

<span data-ttu-id="9e339-118">**Advertencia de seguridad:** El uso incorrecto de este mensaje puede poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="9e339-118">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="9e339-119">Este mensaje no proporciona una manera de conocer el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="9e339-119">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="9e339-120">Si usa este mensaje, llame primero a [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) para obtener el número de caracteres necesarios y, a continuación, llame al mensaje para recuperar la cadena.</span><span class="sxs-lookup"><span data-stu-id="9e339-120">If you use this message, first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="9e339-121">Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="9e339-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="9e339-122">Si crea el cuadro combinado con un estilo dibujado por el propietario, pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el búfer al que apunta *lParam* recibirá los datos asociados al elemento.</span><span class="sxs-lookup"><span data-stu-id="9e339-122">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the buffer pointed to by *lParam* receives the data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e339-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e339-123">Requirements</span></span>



| <span data-ttu-id="9e339-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e339-124">Requirement</span></span> | <span data-ttu-id="9e339-125">Value</span><span class="sxs-lookup"><span data-stu-id="9e339-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e339-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e339-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9e339-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e339-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9e339-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e339-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9e339-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e339-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9e339-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e339-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e339-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e339-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e339-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e339-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e339-133">**CB \_ GETLBTEXTLEN**</span><span class="sxs-lookup"><span data-stu-id="9e339-133">**CB\_GETLBTEXTLEN**</span></span>](cb-getlbtextlen.md)
</dt> </dl>

 

 





