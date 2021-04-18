---
title: Mensaje de TTM_ENUMTOOLS (commctrl. h)
description: Recupera la información que mantiene un control ToolTip sobre la herramienta actual \ 8212; es decir, la herramienta para la que la información sobre herramientas está mostrando texto actualmente.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- TTM_ENUMTOOLS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad1679f9740539507a57c4cba93319569add0af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490684"
---
# <a name="ttm_enumtools-message"></a><span data-ttu-id="25a2f-104">TTM \_ ENUMTOOLS</span><span class="sxs-lookup"><span data-stu-id="25a2f-104">TTM\_ENUMTOOLS message</span></span>

<span data-ttu-id="25a2f-105">Recupera la información que mantiene un control ToolTip sobre la herramienta actual, es decir, la herramienta para la que la información sobre herramientas está mostrando texto actualmente.</span><span class="sxs-lookup"><span data-stu-id="25a2f-105">Retrieves the information that a tooltip control maintains about the current tool that is, the tool for which the tooltip is currently displaying text.</span></span>

## <a name="parameters"></a><span data-ttu-id="25a2f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25a2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25a2f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25a2f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25a2f-108">Índice de base cero de la herramienta para la que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="25a2f-108">Zero-based index of the tool for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="25a2f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25a2f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25a2f-110">Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que recibe información sobre la herramienta.</span><span class="sxs-lookup"><span data-stu-id="25a2f-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the tool.</span></span> <span data-ttu-id="25a2f-111">Establezca el miembro **cbSize** de esta estructura en SIZEOF (TOOLINFO) antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="25a2f-111">Set the **cbSize** member of this structure to sizeof(TOOLINFO) before sending this message.</span></span> <span data-ttu-id="25a2f-112">Asigne un búfer.</span><span class="sxs-lookup"><span data-stu-id="25a2f-112">Allocate a buffer.</span></span> <span data-ttu-id="25a2f-113">Establezca el miembro **lpszText** para que apunte al búfer para recibir el texto de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="25a2f-113">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span> <span data-ttu-id="25a2f-114">No hay ninguna manera de determinar el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="25a2f-114">There is no way to determine the required buffer size.</span></span> <span data-ttu-id="25a2f-115">Sin embargo, el texto de la herramienta, tal como se devuelve en el miembro **lpszText** de la estructura **TOOLINFO** , tiene una longitud máxima de 80 **TCHARs**, incluido el carácter **nulo** final.</span><span class="sxs-lookup"><span data-stu-id="25a2f-115">However, tool text, as returned at the **lpszText** member of the **TOOLINFO** structure, has a maximum length of 80 **TCHARs**, including the terminating **NULL**.</span></span> <span data-ttu-id="25a2f-116">Si el texto supera esta longitud, se trunca.</span><span class="sxs-lookup"><span data-stu-id="25a2f-116">If the text exceeds this length, it is truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25a2f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25a2f-117">Return value</span></span>

<span data-ttu-id="25a2f-118">Devuelve **true** si se enumera cualquier herramienta o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="25a2f-118">Returns **TRUE** if any tools are enumerated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="25a2f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25a2f-119">Remarks</span></span>

<span data-ttu-id="25a2f-120">**Advertencia de seguridad:** El uso de este mensaje podría poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="25a2f-120">**Security Warning:** Using this message might compromise the security of your program.</span></span> <span data-ttu-id="25a2f-121">Este mensaje no proporciona una manera para que el receptor del mensaje conozca el tamaño del búfer o para especificar el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="25a2f-121">This message does not provide a way for the message receiver to know the size of the buffer or to specify the size of the buffer.</span></span> <span data-ttu-id="25a2f-122">Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="25a2f-122">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="25a2f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25a2f-123">Requirements</span></span>



| <span data-ttu-id="25a2f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="25a2f-124">Requirement</span></span> | <span data-ttu-id="25a2f-125">Value</span><span class="sxs-lookup"><span data-stu-id="25a2f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25a2f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25a2f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="25a2f-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="25a2f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25a2f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25a2f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="25a2f-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="25a2f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25a2f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25a2f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="25a2f-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="25a2f-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="25a2f-132">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="25a2f-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="25a2f-133">**TTM \_ ENUMTOOLSW** (Unicode) y **TTM \_ ENUMTOOLSA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="25a2f-133">**TTM\_ENUMTOOLSW** (Unicode) and **TTM\_ENUMTOOLSA** (ANSI)</span></span><br/>               |



 

 





