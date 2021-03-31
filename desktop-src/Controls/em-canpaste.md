---
title: Mensaje EM_CANPASTE (RichEdit. h)
description: Determina si un control Rich Edit puede pegar un formato de Portapapeles especificado.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- EM_CANPASTE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079533"
---
# <a name="em_canpaste-message"></a><span data-ttu-id="af67d-104">Mensaje de la \_ descanpaste em</span><span class="sxs-lookup"><span data-stu-id="af67d-104">EM\_CANPASTE message</span></span>

<span data-ttu-id="af67d-105">Determina si un control Rich Edit puede pegar un formato de Portapapeles especificado.</span><span class="sxs-lookup"><span data-stu-id="af67d-105">Determines whether a rich edit control can paste a specified clipboard format.</span></span>

## <a name="parameters"></a><span data-ttu-id="af67d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af67d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af67d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af67d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af67d-108">Especifica los [formatos del portapapeles](/windows/desktop/dataxchg/clipboard-formats) que se van a probar.</span><span class="sxs-lookup"><span data-stu-id="af67d-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats) to try.</span></span> <span data-ttu-id="af67d-109">Para probar cualquier formato que esté actualmente en el portapapeles, establezca este parámetro en cero.</span><span class="sxs-lookup"><span data-stu-id="af67d-109">To try any format currently on the clipboard, set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="af67d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af67d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af67d-111">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="af67d-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af67d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af67d-112">Return value</span></span>

<span data-ttu-id="af67d-113">Si el formato del portapapeles se puede pegar, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="af67d-113">If the clipboard format can be pasted, the return value is a nonzero value.</span></span>

<span data-ttu-id="af67d-114">Si no se puede pegar el formato del portapapeles, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="af67d-114">If the clipboard format cannot be pasted, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="af67d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af67d-115">Requirements</span></span>



| <span data-ttu-id="af67d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af67d-116">Requirement</span></span> | <span data-ttu-id="af67d-117">Value</span><span class="sxs-lookup"><span data-stu-id="af67d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af67d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af67d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af67d-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="af67d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af67d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af67d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af67d-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="af67d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af67d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af67d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af67d-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="af67d-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af67d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="af67d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af67d-125">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="af67d-125">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

