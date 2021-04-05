---
title: Mensaje de TB_SETTOOLTIPS (commctrl. h)
description: Asocia un control ToolTip a una barra de herramientas.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- TB_SETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079126"
---
# <a name="tb_settooltips-message"></a><span data-ttu-id="1ccf6-104">\_Mensaje SETTOOLTIPS TB</span><span class="sxs-lookup"><span data-stu-id="1ccf6-104">TB\_SETTOOLTIPS message</span></span>

<span data-ttu-id="1ccf6-105">Asocia un control ToolTip a una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="1ccf6-105">Associates a tooltip control with a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ccf6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ccf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ccf6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ccf6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ccf6-108">Identificador del control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="1ccf6-108">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="1ccf6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ccf6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1ccf6-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1ccf6-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ccf6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ccf6-111">Return value</span></span>

<span data-ttu-id="1ccf6-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1ccf6-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ccf6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ccf6-113">Remarks</span></span>

<span data-ttu-id="1ccf6-114">Cualquier botón que se agregue a una barra de herramientas antes de enviar el mensaje de **TB \_ SETTOOLTIPS** no se registrará con el control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="1ccf6-114">Any buttons added to a toolbar before sending the **TB\_SETTOOLTIPS** message will not be registered with the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ccf6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ccf6-115">Requirements</span></span>



| <span data-ttu-id="1ccf6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ccf6-116">Requirement</span></span> | <span data-ttu-id="1ccf6-117">Value</span><span class="sxs-lookup"><span data-stu-id="1ccf6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccf6-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ccf6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1ccf6-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ccf6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ccf6-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ccf6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1ccf6-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ccf6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ccf6-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ccf6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ccf6-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ccf6-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





