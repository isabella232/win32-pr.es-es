---
title: Mensaje de SB_GETTEXTLENGTH (commctrl. h)
description: Recupera la longitud, en caracteres, del texto de la parte especificada de una ventana de estado.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- SB_GETTEXTLENGTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996812"
---
# <a name="sb_gettextlength-message"></a><span data-ttu-id="ad93c-104">\_Mensaje GETTEXTLENGTH de SB</span><span class="sxs-lookup"><span data-stu-id="ad93c-104">SB\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="ad93c-105">Recupera la longitud, en caracteres, del texto de la parte especificada de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="ad93c-105">Retrieves the length, in characters, of the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad93c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad93c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad93c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad93c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad93c-108">Índice de base cero del elemento del que se va a recuperar el texto.</span><span class="sxs-lookup"><span data-stu-id="ad93c-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="ad93c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad93c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ad93c-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ad93c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad93c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad93c-111">Return value</span></span>

<span data-ttu-id="ad93c-112">Devuelve un valor de 32 bits que consta de valores de 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ad93c-112">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="ad93c-113">La palabra baja especifica la longitud, en caracteres, del texto.</span><span class="sxs-lookup"><span data-stu-id="ad93c-113">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="ad93c-114">La palabra alta especifica el tipo de operación que se usa para dibujar el texto.</span><span class="sxs-lookup"><span data-stu-id="ad93c-114">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="ad93c-115">El tipo puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="ad93c-115">The type can be one of the following values:</span></span>



| <span data-ttu-id="ad93c-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ad93c-116">Return code</span></span>                                                                                    | <span data-ttu-id="ad93c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad93c-117">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad93c-118"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="ad93c-118"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="ad93c-119">El texto se dibuja con un borde para que aparezca inferior al plano de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ad93c-119">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>          |
| <dl> <span data-ttu-id="ad93c-120"><dt>**SBT \_ NOborders**</dt></span><span class="sxs-lookup"><span data-stu-id="ad93c-120"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="ad93c-121">El texto se dibuja sin bordes.</span><span class="sxs-lookup"><span data-stu-id="ad93c-121">The text is drawn without borders.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="ad93c-122"><dt>**SBT \_ OWNERDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="ad93c-122"><dt>**SBT\_OWNERDRAW**</dt></span></span> </dl>  | <span data-ttu-id="ad93c-123">El texto se dibuja mediante la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="ad93c-123">The text is drawn by the parent window.</span></span><br/>                                                |
| <dl> <span data-ttu-id="ad93c-124"><dt>**SBT \_ emergente**</dt></span><span class="sxs-lookup"><span data-stu-id="ad93c-124"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="ad93c-125">El texto se dibuja con un borde para que aparezca más arriba que el plano de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ad93c-125">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/>         |
| <dl> <span data-ttu-id="ad93c-126"><dt>**SBT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="ad93c-126"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="ad93c-127">El texto se mostrará en la dirección opuesta al texto de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="ad93c-127">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ad93c-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad93c-128">Remarks</span></span>

<span data-ttu-id="ad93c-129">Texto normal de la pantalla de Windows de izquierda a derecha (LTR).</span><span class="sxs-lookup"><span data-stu-id="ad93c-129">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="ad93c-130">Las ventanas se pueden *reflejar* para mostrar idiomas como el hebreo o el árabe que se leen de derecha a izquierda (RTL).</span><span class="sxs-lookup"><span data-stu-id="ad93c-130">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="ad93c-131">Si \_ se establece SBT RTLREADING, el texto de la ventana de estado especificada se leerá en la dirección opuesta a la del texto de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="ad93c-131">If SBT\_RTLREADING is set, the specified status window text will read in the opposite direction from the text in the parent window.</span></span>

<span data-ttu-id="ad93c-132">Este mensaje devuelve una longitud máxima de cadena de 65.535 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ad93c-132">This message returns a maximum string length of 65,535 characters.</span></span> <span data-ttu-id="ad93c-133">Si la cadena de texto real es más larga que esa, el mensaje [**\_ GETTEXT de SB**](sb-gettext.md) lo trunca.</span><span class="sxs-lookup"><span data-stu-id="ad93c-133">If the actual text string is longer than that, the [**SB\_GETTEXT**](sb-gettext.md) message truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad93c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad93c-134">Requirements</span></span>



| <span data-ttu-id="ad93c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad93c-135">Requirement</span></span> | <span data-ttu-id="ad93c-136">Value</span><span class="sxs-lookup"><span data-stu-id="ad93c-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad93c-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad93c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ad93c-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ad93c-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad93c-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad93c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ad93c-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad93c-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad93c-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad93c-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad93c-142"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad93c-142"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ad93c-143">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ad93c-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ad93c-144">**SB \_ GETTEXTLENGTHW** (Unicode) y **SB \_ GETTEXTLENGTHA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ad93c-144">**SB\_GETTEXTLENGTHW** (Unicode) and **SB\_GETTEXTLENGTHA** (ANSI)</span></span><br/>         |



 

 





