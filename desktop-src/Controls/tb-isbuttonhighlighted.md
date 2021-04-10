---
title: Mensaje de TB_ISBUTTONHIGHLIGHTED (commctrl. h)
description: Comprueba el estado de resaltado de un botón de la barra de herramientas.
ms.assetid: d5aab670-a989-46f2-b4f8-d8a8968cbe07
keywords:
- TB_ISBUTTONHIGHLIGHTED controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIGHLIGHTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53e25058fee8fa5dcac218a641277ac46aed4e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079128"
---
# <a name="tb_isbuttonhighlighted-message"></a><span data-ttu-id="323c6-104">\_Mensaje ISBUTTONHIGHLIGHTED TB</span><span class="sxs-lookup"><span data-stu-id="323c6-104">TB\_ISBUTTONHIGHLIGHTED message</span></span>

<span data-ttu-id="323c6-105">Comprueba el estado de resaltado de un botón de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="323c6-105">Checks the highlight state of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="323c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="323c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="323c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="323c6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="323c6-108">Identificador de comando para un botón de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="323c6-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="323c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="323c6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="323c6-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="323c6-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="323c6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="323c6-111">Return value</span></span>

<span data-ttu-id="323c6-112">Devuelve un valor distinto de cero si el botón está resaltado o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="323c6-112">Returns nonzero if the button is highlighted, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="323c6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="323c6-113">Requirements</span></span>



| <span data-ttu-id="323c6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="323c6-114">Requirement</span></span> | <span data-ttu-id="323c6-115">Value</span><span class="sxs-lookup"><span data-stu-id="323c6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="323c6-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="323c6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="323c6-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="323c6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="323c6-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="323c6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="323c6-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="323c6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="323c6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="323c6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="323c6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="323c6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





