---
title: Mensaje de TB_SETMETRICS (commctrl. h)
description: Establece las métricas de un control de barra de herramientas.
ms.assetid: 60e35d65-6291-4a55-a4cf-19b5b1db8a65
keywords:
- TB_SETMETRICS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5320ecc85f0a44c4c80868ae5699b051e1ac1781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996108"
---
# <a name="tb_setmetrics-message"></a><span data-ttu-id="6e38e-104">\_Mensaje SETMETRICS TB</span><span class="sxs-lookup"><span data-stu-id="6e38e-104">TB\_SETMETRICS message</span></span>

<span data-ttu-id="6e38e-105">Establece las métricas de un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="6e38e-105">Sets the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e38e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e38e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e38e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e38e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6e38e-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6e38e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6e38e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e38e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e38e-110">Estructura [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) que contiene las métricas de la barra de herramientas que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="6e38e-110">[**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that contains the toolbar metrics to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e38e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e38e-111">Return value</span></span>

<span data-ttu-id="6e38e-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="6e38e-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e38e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e38e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6e38e-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="6e38e-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6e38e-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6e38e-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6e38e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e38e-116">Requirements</span></span>



| <span data-ttu-id="6e38e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e38e-117">Requirement</span></span> | <span data-ttu-id="6e38e-118">Value</span><span class="sxs-lookup"><span data-stu-id="6e38e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e38e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e38e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6e38e-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6e38e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e38e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e38e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6e38e-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e38e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e38e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e38e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e38e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e38e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





