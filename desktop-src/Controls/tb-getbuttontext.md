---
title: Mensaje de TB_GETBUTTONTEXT (commctrl. h)
description: Recupera el texto para mostrar de un botón de una barra de herramientas.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- TB_GETBUTTONTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac0b238574cc136f41959b57f3f0e1ec13e3ea1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150453"
---
# <a name="tb_getbuttontext-message"></a><span data-ttu-id="1f9df-104">\_Mensaje GETBUTTONTEXT TB</span><span class="sxs-lookup"><span data-stu-id="1f9df-104">TB\_GETBUTTONTEXT message</span></span>

<span data-ttu-id="1f9df-105">Recupera el texto para mostrar de un botón de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="1f9df-105">Retrieves the display text of a button on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f9df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f9df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f9df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f9df-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f9df-108">Identificador de comando del botón cuyo texto se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="1f9df-108">Command identifier of the button whose text is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="1f9df-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f9df-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f9df-110">Puntero a un búfer que recibe el texto del botón.</span><span class="sxs-lookup"><span data-stu-id="1f9df-110">Pointer to a buffer that receives the button text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f9df-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f9df-111">Return value</span></span>

<span data-ttu-id="1f9df-112">Devuelve la longitud, en caracteres, de la cadena a la que señala *lParam*.</span><span class="sxs-lookup"><span data-stu-id="1f9df-112">Returns the length, in characters, of the string pointed to by *lParam*.</span></span> <span data-ttu-id="1f9df-113">La longitud no incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="1f9df-113">The length does not include the terminating null character.</span></span> <span data-ttu-id="1f9df-114">Si no se realiza correctamente, el valor devuelto es-1.</span><span class="sxs-lookup"><span data-stu-id="1f9df-114">If unsuccessful, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f9df-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f9df-115">Remarks</span></span>

<span data-ttu-id="1f9df-116">**Advertencia de seguridad:** El uso incorrecto de este mensaje podría poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="1f9df-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="1f9df-117">Este mensaje no proporciona una manera de conocer el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="1f9df-117">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="1f9df-118">Si usa este mensaje, llame primero al mensaje que pasa **null** en *lParam*; esto devuelve el número de caracteres, excluidos los **valores NULL** necesarios.</span><span class="sxs-lookup"><span data-stu-id="1f9df-118">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="1f9df-119">A continuación, llame al mensaje una segunda vez para recuperar la cadena.</span><span class="sxs-lookup"><span data-stu-id="1f9df-119">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="1f9df-120">Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="1f9df-120">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="1f9df-121">La cadena devuelta corresponde al texto que se muestra actualmente en el botón.</span><span class="sxs-lookup"><span data-stu-id="1f9df-121">The returned string corresponds to the text that is currently displayed by the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f9df-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f9df-122">Requirements</span></span>



| <span data-ttu-id="1f9df-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f9df-123">Requirement</span></span> | <span data-ttu-id="1f9df-124">Value</span><span class="sxs-lookup"><span data-stu-id="1f9df-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9df-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f9df-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1f9df-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1f9df-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f9df-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f9df-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1f9df-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1f9df-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f9df-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f9df-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f9df-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f9df-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1f9df-131">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1f9df-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1f9df-132">**TB \_ GETBUTTONTEXTW** (Unicode) y **TB \_ GETBUTTONTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1f9df-132">**TB\_GETBUTTONTEXTW** (Unicode) and **TB\_GETBUTTONTEXTA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="1f9df-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f9df-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f9df-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1f9df-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1f9df-135">**TB \_ GETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="1f9df-135">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="1f9df-136">**GETSTRING de TB \_**</span><span class="sxs-lookup"><span data-stu-id="1f9df-136">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="1f9df-137">**TB \_ SETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="1f9df-137">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> </dl>

 

 





