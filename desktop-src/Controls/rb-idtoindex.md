---
title: Mensaje de RB_IDTOINDEX (commctrl. h)
description: Convierte un identificador de banda en un índice de banda en un control rebar.
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- RB_IDTOINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_IDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7acd85862bc4787a6b32d2fdd3c897a52913b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489238"
---
# <a name="rb_idtoindex-message"></a><span data-ttu-id="a2e3b-104">Mensaje de IDTOINDEX de RB \_</span><span class="sxs-lookup"><span data-stu-id="a2e3b-104">RB\_IDTOINDEX message</span></span>

<span data-ttu-id="a2e3b-105">Convierte un identificador de banda en un índice de banda en un control rebar.</span><span class="sxs-lookup"><span data-stu-id="a2e3b-105">Converts a band identifier to a band index in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2e3b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2e3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2e3b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2e3b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2e3b-108">Identificador definido por la aplicación de la banda en cuestión.</span><span class="sxs-lookup"><span data-stu-id="a2e3b-108">The application-defined identifier of the band in question.</span></span> <span data-ttu-id="a2e3b-109">Este es el valor que se pasó en el miembro **wID** de la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) cuando se insertó la banda.</span><span class="sxs-lookup"><span data-stu-id="a2e3b-109">This is the value that was passed in the **wID** member of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure when the band was inserted.</span></span>

</dd> <dt>

<span data-ttu-id="a2e3b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2e3b-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a2e3b-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a2e3b-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2e3b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2e3b-112">Return value</span></span>

<span data-ttu-id="a2e3b-113">Devuelve el índice de banda de base cero si es correcto, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a2e3b-113">Returns the zero-based band index if successful, or -1 otherwise.</span></span> <span data-ttu-id="a2e3b-114">Si existen identificadores de banda duplicados, se devuelve el primero.</span><span class="sxs-lookup"><span data-stu-id="a2e3b-114">If duplicate band identifiers exist, the first one is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2e3b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2e3b-115">Requirements</span></span>



| <span data-ttu-id="a2e3b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2e3b-116">Requirement</span></span> | <span data-ttu-id="a2e3b-117">Value</span><span class="sxs-lookup"><span data-stu-id="a2e3b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e3b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2e3b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a2e3b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a2e3b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a2e3b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2e3b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a2e3b-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2e3b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2e3b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2e3b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2e3b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2e3b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





