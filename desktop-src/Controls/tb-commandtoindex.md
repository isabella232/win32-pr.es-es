---
title: Mensaje de TB_COMMANDTOINDEX (commctrl. h)
description: Recupera el índice de base cero para el botón asociado al identificador de comando especificado.
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- TB_COMMANDTOINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_COMMANDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0257f55e01db59f1d23d59583f1ef78f44b1dac1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151261"
---
# <a name="tb_commandtoindex-message"></a><span data-ttu-id="df0ce-104">\_Mensaje COMMANDTOINDEX TB</span><span class="sxs-lookup"><span data-stu-id="df0ce-104">TB\_COMMANDTOINDEX message</span></span>

<span data-ttu-id="df0ce-105">Recupera el índice de base cero para el botón asociado al identificador de comando especificado.</span><span class="sxs-lookup"><span data-stu-id="df0ce-105">Retrieves the zero-based index for the button associated with the specified command identifier.</span></span>

## <a name="parameters"></a><span data-ttu-id="df0ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df0ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df0ce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df0ce-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df0ce-108">Identificador de comando asociado al botón.</span><span class="sxs-lookup"><span data-stu-id="df0ce-108">Command identifier associated with the button.</span></span>

</dd> <dt>

<span data-ttu-id="df0ce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df0ce-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="df0ce-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="df0ce-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df0ce-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df0ce-111">Return value</span></span>

<span data-ttu-id="df0ce-112">Devuelve el índice de base cero para el botón o-1 si el identificador de comando especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="df0ce-112">Returns the zero-based index for the button or -1 if the specified command identifier is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="df0ce-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df0ce-113">Requirements</span></span>



| <span data-ttu-id="df0ce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="df0ce-114">Requirement</span></span> | <span data-ttu-id="df0ce-115">Value</span><span class="sxs-lookup"><span data-stu-id="df0ce-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df0ce-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df0ce-116">Minimum supported client</span></span><br/> | <span data-ttu-id="df0ce-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="df0ce-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df0ce-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df0ce-118">Minimum supported server</span></span><br/> | <span data-ttu-id="df0ce-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="df0ce-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df0ce-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df0ce-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="df0ce-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="df0ce-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





