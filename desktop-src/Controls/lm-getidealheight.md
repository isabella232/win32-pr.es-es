---
title: LM_GETIDEALHEIGHT mensaje (Commctrl.h)
description: 'LM_GETIDEALHEIGHT mensaje: recupera el alto preferido de un vínculo para el ancho actual del control.'
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- LM_GETIDEALHEIGHT de mensajes controles de Windows
topic_type:
- apiref
api_name:
- LM_GETIDEALHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6e82f259124e6da285ed2357d48ca07d5f8c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112403"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="bd4e9-104">Mensaje \_ GETIDEALHEIGHT de LM</span><span class="sxs-lookup"><span data-stu-id="bd4e9-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="bd4e9-105">Recupera el alto preferido de un vínculo para el ancho actual del control.</span><span class="sxs-lookup"><span data-stu-id="bd4e9-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd4e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd4e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd4e9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd4e9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bd4e9-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bd4e9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bd4e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd4e9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bd4e9-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bd4e9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd4e9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd4e9-111">Return value</span></span>

<span data-ttu-id="bd4e9-112">Entero que representa el alto preferido del texto del vínculo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="bd4e9-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd4e9-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bd4e9-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bd4e9-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0.</span><span class="sxs-lookup"><span data-stu-id="bd4e9-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="bd4e9-115">Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)</span><span class="sxs-lookup"><span data-stu-id="bd4e9-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd4e9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd4e9-116">Requirements</span></span>



| <span data-ttu-id="bd4e9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd4e9-117">Requirement</span></span> | <span data-ttu-id="bd4e9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bd4e9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd4e9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd4e9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bd4e9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bd4e9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd4e9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd4e9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bd4e9-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd4e9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd4e9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd4e9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd4e9-124"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="bd4e9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





