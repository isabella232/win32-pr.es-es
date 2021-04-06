---
title: Mensaje de TB_GETMETRICS (commctrl. h)
description: Recupera las métricas de un control de barra de herramientas.
ms.assetid: 19c735cf-09f8-443e-8a73-dd64af0193a1
keywords:
- TB_GETMETRICS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1ee299f56b367eef649a05657d713e22206a7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905452"
---
# <a name="tb_getmetrics-message"></a><span data-ttu-id="8b0c9-104">\_Mensaje GETMETRICS TB</span><span class="sxs-lookup"><span data-stu-id="8b0c9-104">TB\_GETMETRICS message</span></span>

<span data-ttu-id="8b0c9-105">Recupera las métricas de un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-105">Retrieves the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b0c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b0c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b0c9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b0c9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8b0c9-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8b0c9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b0c9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b0c9-110">Puntero a una estructura [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) que recibe las métricas de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-110">Pointer to a [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that receives the toolbar metrics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b0c9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b0c9-111">Return value</span></span>

<span data-ttu-id="8b0c9-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b0c9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b0c9-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8b0c9-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="8b0c9-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8b0c9-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b0c9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b0c9-116">Requirements</span></span>



| <span data-ttu-id="8b0c9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b0c9-117">Requirement</span></span> | <span data-ttu-id="8b0c9-118">Value</span><span class="sxs-lookup"><span data-stu-id="8b0c9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0c9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b0c9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8b0c9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8b0c9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b0c9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b0c9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8b0c9-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b0c9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b0c9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b0c9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b0c9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b0c9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





