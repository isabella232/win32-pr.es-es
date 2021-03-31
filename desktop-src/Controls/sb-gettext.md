---
title: Mensaje de SB_GETTEXT (commctrl. h)
description: Recupera el texto de la parte especificada de una ventana de estado.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- SB_GETTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079609"
---
# <a name="sb_gettext-message"></a><span data-ttu-id="ada5e-104">\_Mensaje GETTEXT de SB</span><span class="sxs-lookup"><span data-stu-id="ada5e-104">SB\_GETTEXT message</span></span>

<span data-ttu-id="ada5e-105">Recupera el texto de la parte especificada de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="ada5e-105">Retrieves the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="ada5e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ada5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ada5e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ada5e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ada5e-108">Índice de base cero del elemento del que se va a recuperar el texto.</span><span class="sxs-lookup"><span data-stu-id="ada5e-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="ada5e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ada5e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ada5e-110">Puntero al búfer que recibe el texto como una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="ada5e-110">Pointer to the buffer that receives the text as a null-terminated string.</span></span> <span data-ttu-id="ada5e-111">Use el [**mensaje \_ GETTEXTLENGTH de SB**](sb-gettextlength.md) para determinar el tamaño requerido del búfer.</span><span class="sxs-lookup"><span data-stu-id="ada5e-111">Use the [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message to determine the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ada5e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ada5e-112">Return value</span></span>

<span data-ttu-id="ada5e-113">Devuelve un valor de 32 bits que consta de valores de 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ada5e-113">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="ada5e-114">La palabra baja especifica la longitud, en caracteres, del texto.</span><span class="sxs-lookup"><span data-stu-id="ada5e-114">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="ada5e-115">La palabra alta especifica el tipo de operación que se usa para dibujar el texto.</span><span class="sxs-lookup"><span data-stu-id="ada5e-115">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="ada5e-116">El tipo puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ada5e-116">The type can be one of the following values.</span></span>



| <span data-ttu-id="ada5e-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ada5e-117">Return code</span></span>                                                                                    | <span data-ttu-id="ada5e-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ada5e-118">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ada5e-119"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="ada5e-119"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="ada5e-120">El texto se dibuja con un borde para que aparezca inferior al plano de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ada5e-120">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>  |
| <dl> <span data-ttu-id="ada5e-121"><dt>**SBT \_ NOborders**</dt></span><span class="sxs-lookup"><span data-stu-id="ada5e-121"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="ada5e-122">El texto se dibuja sin bordes.</span><span class="sxs-lookup"><span data-stu-id="ada5e-122">The text is drawn without borders.</span></span><br/>                                             |
| <dl> <span data-ttu-id="ada5e-123"><dt>**SBT \_ emergente**</dt></span><span class="sxs-lookup"><span data-stu-id="ada5e-123"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="ada5e-124">El texto se dibuja con un borde para que aparezca más arriba que el plano de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ada5e-124">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/> |
| <dl> <span data-ttu-id="ada5e-125"><dt>**SBT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="ada5e-125"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="ada5e-126">El texto se muestra en la dirección opuesta del texto de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="ada5e-126">The text displays in the opposite direction of the text in the parent window.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="ada5e-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ada5e-127">Remarks</span></span>

<span data-ttu-id="ada5e-128">**Advertencia de seguridad:** El uso incorrecto de este mensaje puede poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="ada5e-128">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="ada5e-129">Este mensaje no proporciona una manera de conocer el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="ada5e-129">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="ada5e-130">Si usa este mensaje, llame primero a [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obtener el número de caracteres necesarios y, a continuación, llame al mensaje para recuperar la cadena.</span><span class="sxs-lookup"><span data-stu-id="ada5e-130">If you use this message, first call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="ada5e-131">Si espera antes de llamar a la **\_ GETTEXT de SB** , el texto podría cambiar, invalidando de este modo el valor devuelto de **SB \_ GETTEXTLENGTH**.</span><span class="sxs-lookup"><span data-stu-id="ada5e-131">If you wait before calling **SB\_GETTEXT** the text could change, thereby invalidating the return value of **SB\_GETTEXTLENGTH**.</span></span> <span data-ttu-id="ada5e-132">Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="ada5e-132">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="ada5e-133">Este mensaje devuelve un máximo de 65.535 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ada5e-133">This message returns a maximum of 65,535 characters.</span></span> <span data-ttu-id="ada5e-134">Si la cadena de texto es más larga, se trunca.</span><span class="sxs-lookup"><span data-stu-id="ada5e-134">If the text string is longer than that, it is truncated.</span></span>

<span data-ttu-id="ada5e-135">Si el texto tiene el \_ tipo de dibujo OWNERDRAW SBT, este mensaje devuelve el valor de 32 bits asociado al texto en lugar de la longitud y el tipo de operación.</span><span class="sxs-lookup"><span data-stu-id="ada5e-135">If the text has the SBT\_OWNERDRAW drawing type, this message returns the 32-bit value associated with the text instead of the length and operation type.</span></span>

<span data-ttu-id="ada5e-136">Texto normal de la pantalla de Windows de izquierda a derecha (LTR).</span><span class="sxs-lookup"><span data-stu-id="ada5e-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="ada5e-137">Las ventanas se pueden *reflejar* para mostrar idiomas como el hebreo o el árabe que se leen de derecha a izquierda (RTL).</span><span class="sxs-lookup"><span data-stu-id="ada5e-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="ada5e-138">Si \_ se establece SBT RTLREADING, la cadena *lParam* lee en la dirección opuesta del texto de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="ada5e-138">If SBT\_RTLREADING is set, the *lParam* string reads in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="ada5e-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ada5e-139">Requirements</span></span>



| <span data-ttu-id="ada5e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="ada5e-140">Requirement</span></span> | <span data-ttu-id="ada5e-141">Value</span><span class="sxs-lookup"><span data-stu-id="ada5e-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ada5e-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ada5e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ada5e-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ada5e-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ada5e-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ada5e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ada5e-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ada5e-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ada5e-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ada5e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ada5e-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ada5e-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ada5e-148">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ada5e-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ada5e-149">**SB \_ GETTEXTW** (Unicode) y **\_ gettext gettexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ada5e-149">**SB\_GETTEXTW** (Unicode) and **SB\_GETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="ada5e-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="ada5e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ada5e-151">**SETTEXT de SB \_**</span><span class="sxs-lookup"><span data-stu-id="ada5e-151">**SB\_SETTEXT**</span></span>](sb-settext.md)
</dt> </dl>

 

 





