---
title: Mensaje EM_GETSELTEXT (RichEdit. h)
description: Recupera el texto seleccionado actualmente en un control Rich Edit.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- EM_GETSELTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde2c0677fa04ff6d7991bca56bad0c08a6f5ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905201"
---
# <a name="em_getseltext-message"></a><span data-ttu-id="1654f-104">\_Mensaje GETSELTEXT em</span><span class="sxs-lookup"><span data-stu-id="1654f-104">EM\_GETSELTEXT message</span></span>

<span data-ttu-id="1654f-105">Recupera el texto seleccionado actualmente en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1654f-105">Retrieves the currently selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1654f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1654f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1654f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1654f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1654f-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1654f-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1654f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1654f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1654f-110">Puntero a un búfer que recibe el texto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="1654f-110">Pointer to a buffer that receives the selected text.</span></span> <span data-ttu-id="1654f-111">La aplicación que realiza la llamada debe asegurarse de que el búfer sea lo suficientemente grande como para contener el texto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="1654f-111">The calling application must ensure that the buffer is large enough to hold the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1654f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1654f-112">Return value</span></span>

<span data-ttu-id="1654f-113">Este mensaje devuelve el número de caracteres copiados, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="1654f-113">This message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="1654f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1654f-114">Requirements</span></span>



| <span data-ttu-id="1654f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1654f-115">Requirement</span></span> | <span data-ttu-id="1654f-116">Value</span><span class="sxs-lookup"><span data-stu-id="1654f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1654f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1654f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1654f-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1654f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1654f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1654f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1654f-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1654f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1654f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1654f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1654f-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1654f-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





