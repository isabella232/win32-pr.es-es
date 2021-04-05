---
title: Mensaje de TB_ISBUTTONINDETERMINATE (commctrl. h)
description: Determina si el botón especificado de una barra de herramientas es indeterminado.
ms.assetid: b4d759b3-cdbc-417b-9da4-4ed9edc38c0e
keywords:
- TB_ISBUTTONINDETERMINATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONINDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc024efcad9f0f48ae4882b019269903c249bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079127"
---
# <a name="tb_isbuttonindeterminate-message"></a><span data-ttu-id="d1c82-104">\_Mensaje ISBUTTONINDETERMINATE TB</span><span class="sxs-lookup"><span data-stu-id="d1c82-104">TB\_ISBUTTONINDETERMINATE message</span></span>

<span data-ttu-id="d1c82-105">Determina si el botón especificado de una barra de herramientas es indeterminado.</span><span class="sxs-lookup"><span data-stu-id="d1c82-105">Determines whether the specified button in a toolbar is indeterminate.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1c82-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1c82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c82-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1c82-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c82-108">Identificador de comando del botón.</span><span class="sxs-lookup"><span data-stu-id="d1c82-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="d1c82-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1c82-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d1c82-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d1c82-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c82-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1c82-111">Return value</span></span>

<span data-ttu-id="d1c82-112">Devuelve un valor distinto de cero si el botón es indeterminado o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="d1c82-112">Returns nonzero if the button is indeterminate, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1c82-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1c82-113">Requirements</span></span>



| <span data-ttu-id="d1c82-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1c82-114">Requirement</span></span> | <span data-ttu-id="d1c82-115">Value</span><span class="sxs-lookup"><span data-stu-id="d1c82-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c82-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1c82-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c82-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d1c82-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1c82-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1c82-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c82-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1c82-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1c82-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1c82-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1c82-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1c82-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





