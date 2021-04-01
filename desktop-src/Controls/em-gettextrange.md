---
title: Mensaje EM_GETTEXTRANGE (RichEdit. h)
description: Recupera un intervalo especificado de caracteres de un control Rich Edit.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- EM_GETTEXTRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68c4089bbe2cc09daa39d69e9094a4abaead787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996825"
---
# <a name="em_gettextrange-message"></a><span data-ttu-id="8a37d-104">\_Mensaje GETTEXTRANGE em</span><span class="sxs-lookup"><span data-stu-id="8a37d-104">EM\_GETTEXTRANGE message</span></span>

<span data-ttu-id="8a37d-105">Recupera un intervalo especificado de caracteres de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8a37d-105">Retrieves a specified range of characters from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a37d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a37d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a37d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a37d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a37d-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8a37d-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8a37d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a37d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a37d-110">Puntero a una estructura [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) que especifica el intervalo de caracteres que se va a recuperar y un búfer en el que se van a copiar los caracteres.</span><span class="sxs-lookup"><span data-stu-id="8a37d-110">Pointer to a [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure that specifies the range of characters to retrieve and a buffer to copy the characters to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a37d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a37d-111">Return value</span></span>

<span data-ttu-id="8a37d-112">El mensaje devuelve el número de caracteres copiados, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="8a37d-112">The message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a37d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a37d-113">Requirements</span></span>



| <span data-ttu-id="8a37d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a37d-114">Requirement</span></span> | <span data-ttu-id="8a37d-115">Value</span><span class="sxs-lookup"><span data-stu-id="8a37d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a37d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a37d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8a37d-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8a37d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a37d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a37d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8a37d-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a37d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a37d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a37d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a37d-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a37d-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a37d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a37d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a37d-123">**TEXTRANGE**</span><span class="sxs-lookup"><span data-stu-id="8a37d-123">**TEXTRANGE**</span></span>](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





