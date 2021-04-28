---
title: LM_GETIDEALSIZE mensaje (Commctrl.h)
description: 'LM_GETIDEALSIZE mensaje: recupera el alto preferido de un vínculo para el ancho actual del control.'
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE de mensajes controles de Windows
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761fb5f6e5f7a2e2e9b1b9cc862b9a8f2c0fcd1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112393"
---
# <a name="lm_getidealsize-message"></a><span data-ttu-id="f29be-104">Mensaje \_ GETIDEALSIZE de LM</span><span class="sxs-lookup"><span data-stu-id="f29be-104">LM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="f29be-105">Recupera el alto preferido de un vínculo para el ancho actual del control.</span><span class="sxs-lookup"><span data-stu-id="f29be-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="f29be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f29be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f29be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f29be-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f29be-108">Ancho máximo del vínculo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f29be-108">Maximum width of the link, in pixels.</span></span></dd> <dt>

<span data-ttu-id="f29be-109">*lParam* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f29be-109">*lParam* \[out\]</span></span>
</dt> <dd><span data-ttu-id="f29be-110">Cuando este mensaje vuelve, contiene un puntero a una <a href="/previous-versions//dd145106(v=vs.85)">**estructura SIZE.**</a></span><span class="sxs-lookup"><span data-stu-id="f29be-110">When this message returns, contains a pointer to a <a href="/previous-versions//dd145106(v=vs.85)">**SIZE**</a> structure.</span></span> <span data-ttu-id="f29be-111">El **miembro cy** de esta estructura indica el alto ideal del control para el ancho dado.</span><span class="sxs-lookup"><span data-stu-id="f29be-111">The **cy** member of this structure indicates the ideal height of the control for the given width.</span></span> <span data-ttu-id="f29be-112">Ajusta el miembro **cx a** la cantidad de espacio realmente necesario.</span><span class="sxs-lookup"><span data-stu-id="f29be-112">It adjusts the **cx** member to the amount of space actually needed.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f29be-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f29be-113">Return value</span></span>

<span data-ttu-id="f29be-114">Entero que representa el alto preferido del texto del vínculo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f29be-114">Integer that represents the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="f29be-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f29be-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f29be-116">Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0.</span><span class="sxs-lookup"><span data-stu-id="f29be-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f29be-117">Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)</span><span class="sxs-lookup"><span data-stu-id="f29be-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f29be-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f29be-118">Requirements</span></span>



| <span data-ttu-id="f29be-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f29be-119">Requirement</span></span> | <span data-ttu-id="f29be-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f29be-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f29be-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f29be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f29be-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f29be-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f29be-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f29be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f29be-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f29be-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f29be-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f29be-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f29be-126"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="f29be-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

