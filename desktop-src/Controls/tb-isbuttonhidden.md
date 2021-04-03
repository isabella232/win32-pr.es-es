---
title: Mensaje de TB_ISBUTTONHIDDEN (commctrl. h)
description: Determina si el botón especificado de una barra de herramientas está oculto.
ms.assetid: 3372a64f-8209-4e3f-a6a9-8fe2e7e87ff2
keywords:
- TB_ISBUTTONHIDDEN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIDDEN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db36f289a05fecfb2a0795965820324a9ce68057
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997172"
---
# <a name="tb_isbuttonhidden-message"></a><span data-ttu-id="9b04c-104">\_Mensaje ISBUTTONHIDDEN TB</span><span class="sxs-lookup"><span data-stu-id="9b04c-104">TB\_ISBUTTONHIDDEN message</span></span>

<span data-ttu-id="9b04c-105">Determina si el botón especificado de una barra de herramientas está oculto.</span><span class="sxs-lookup"><span data-stu-id="9b04c-105">Determines whether the specified button in a toolbar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b04c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b04c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b04c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b04c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b04c-108">Identificador de comando del botón.</span><span class="sxs-lookup"><span data-stu-id="9b04c-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="9b04c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b04c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9b04c-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9b04c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b04c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b04c-111">Return value</span></span>

<span data-ttu-id="9b04c-112">Devuelve un valor distinto de cero si el botón está oculto o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9b04c-112">Returns nonzero if the button is hidden, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b04c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b04c-113">Requirements</span></span>



| <span data-ttu-id="9b04c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b04c-114">Requirement</span></span> | <span data-ttu-id="9b04c-115">Value</span><span class="sxs-lookup"><span data-stu-id="9b04c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b04c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b04c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9b04c-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9b04c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b04c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b04c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9b04c-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b04c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b04c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b04c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b04c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b04c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





