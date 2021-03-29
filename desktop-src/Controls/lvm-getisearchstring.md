---
title: Mensaje de LVM_GETISEARCHSTRING (commctrl. h)
description: Recupera la cadena de búsqueda incremental de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetISearchString de ListView.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- LVM_GETISEARCHSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492418"
---
# <a name="lvm_getisearchstring-message"></a><span data-ttu-id="f8244-105">\_Mensaje GETISEARCHSTRING LVM</span><span class="sxs-lookup"><span data-stu-id="f8244-105">LVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="f8244-106">Recupera la cadena de búsqueda incremental de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="f8244-106">Retrieves the incremental search string of a list-view control.</span></span> <span data-ttu-id="f8244-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetISearchString de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) .</span><span class="sxs-lookup"><span data-stu-id="f8244-107">You can send this message explicitly or by using the [**ListView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8244-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8244-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8244-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8244-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f8244-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f8244-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f8244-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8244-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8244-112">Puntero a un búfer que recibe la cadena de búsqueda incremental.</span><span class="sxs-lookup"><span data-stu-id="f8244-112">Pointer to a buffer that receives the incremental search string.</span></span> <span data-ttu-id="f8244-113">Para recuperar solo la longitud de la cadena, establezca *lParam* en **null**.</span><span class="sxs-lookup"><span data-stu-id="f8244-113">To just retrieve the length of the string, set *lParam* to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8244-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8244-114">Return value</span></span>

<span data-ttu-id="f8244-115">Devuelve el número de caracteres de la cadena de búsqueda incremental, sin incluir el carácter nulo de terminación, o bien cero si el control de vista de lista no está en modo de búsqueda incremental.</span><span class="sxs-lookup"><span data-stu-id="f8244-115">Returns the number of characters in the incremental search string, not including the terminating NULL character, or zero if the list-view control is not in incremental search mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8244-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8244-116">Remarks</span></span>

<span data-ttu-id="f8244-117">**Advertencia de seguridad:** El uso incorrecto de este mensaje podría poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="f8244-117">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="f8244-118">Este mensaje no proporciona una manera de conocer el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="f8244-118">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="f8244-119">Si usa este mensaje, llame primero al mensaje que pasa **null** en *lParam*; esto devuelve el número de caracteres, excluidos los **valores NULL** necesarios.</span><span class="sxs-lookup"><span data-stu-id="f8244-119">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="f8244-120">A continuación, llame al mensaje una segunda vez para recuperar la cadena.</span><span class="sxs-lookup"><span data-stu-id="f8244-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="f8244-121">Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="f8244-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="f8244-122">La *cadena de búsqueda incremental* es la secuencia de caracteres que el usuario escribe mientras la vista de lista tiene el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="f8244-122">The *incremental search string* is the character sequence that the user types while the list view has the input focus.</span></span> <span data-ttu-id="f8244-123">Cada vez que el usuario escribe un carácter, el sistema anexa el carácter a la cadena de búsqueda y, a continuación, busca un elemento coincidente.</span><span class="sxs-lookup"><span data-stu-id="f8244-123">Each time the user types a character, the system appends the character to the search string and then searches for a matching item.</span></span> <span data-ttu-id="f8244-124">Si el sistema encuentra una coincidencia, selecciona el elemento y, si es necesario, lo desplaza a la vista.</span><span class="sxs-lookup"><span data-stu-id="f8244-124">If the system finds a match, it selects the item and, if necessary, scrolls it into view.</span></span>

<span data-ttu-id="f8244-125">Un período de tiempo de espera está asociado a cada uno de los caracteres que el usuario escribe.</span><span class="sxs-lookup"><span data-stu-id="f8244-125">A time-out period is associated with each character that the user types.</span></span> <span data-ttu-id="f8244-126">Si el período de tiempo de espera transcurre antes de que el usuario escribe otro carácter, se restablece la cadena de búsqueda incremental.</span><span class="sxs-lookup"><span data-stu-id="f8244-126">If the time-out period elapses before the user types another character, the incremental search string is reset.</span></span>

<span data-ttu-id="f8244-127">Asegúrese de que el búfer sea lo suficientemente grande para contener la cadena y el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="f8244-127">Make sure that the buffer is large enough to hold the string and the terminating NULL character.</span></span> <span data-ttu-id="f8244-128">Si es demasiado pequeño, se producirá un error de página no válido inmediato.</span><span class="sxs-lookup"><span data-stu-id="f8244-128">If it is too small, an immediate invalid page fault will result.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8244-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8244-129">Requirements</span></span>



| <span data-ttu-id="f8244-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8244-130">Requirement</span></span> | <span data-ttu-id="f8244-131">Value</span><span class="sxs-lookup"><span data-stu-id="f8244-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8244-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8244-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f8244-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f8244-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8244-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8244-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f8244-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8244-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8244-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8244-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8244-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8244-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f8244-138">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f8244-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f8244-139">**LVM \_ GETISEARCHSTRINGW** (Unicode) y **\_ GETISEARCHSTRINGA de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f8244-139">**LVM\_GETISEARCHSTRINGW** (Unicode) and **LVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





