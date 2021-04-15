---
title: Mensaje de LM_GETIDEALSIZE (commctrl. h)
description: Recupera el alto preferido de un vínculo para el ancho actual del control.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE controles de mensajes de Windows
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
ms.openlocfilehash: c138e22982116a3b7173f586d96c70cfc91194c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489100"
---
# <a name="lm_getidealsize-message"></a><span data-ttu-id="5989a-104">\_Mensaje GETIDEALSIZE de LM</span><span class="sxs-lookup"><span data-stu-id="5989a-104">LM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="5989a-105">Recupera el alto preferido de un vínculo para el ancho actual del control.</span><span class="sxs-lookup"><span data-stu-id="5989a-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="5989a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5989a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5989a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5989a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5989a-108">Ancho máximo del vínculo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="5989a-108">Maximum width of the link, in pixels.</span></span></dd> <dt>

<span data-ttu-id="5989a-109">*lParam* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5989a-109">*lParam* \[out\]</span></span>
</dt> <dd><span data-ttu-id="5989a-110">Cuando este mensaje vuelve, contiene un puntero a una estructura de <a href="/previous-versions//dd145106(v=vs.85)">**tamaño**</a> .</span><span class="sxs-lookup"><span data-stu-id="5989a-110">When this message returns, contains a pointer to a <a href="/previous-versions//dd145106(v=vs.85)">**SIZE**</a> structure.</span></span> <span data-ttu-id="5989a-111">El miembro **CY** de esta estructura indica el alto ideal del control para el ancho especificado.</span><span class="sxs-lookup"><span data-stu-id="5989a-111">The **cy** member of this structure indicates the ideal height of the control for the given width.</span></span> <span data-ttu-id="5989a-112">Ajusta el miembro de **CX** a la cantidad de espacio realmente necesaria.</span><span class="sxs-lookup"><span data-stu-id="5989a-112">It adjusts the **cx** member to the amount of space actually needed.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5989a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5989a-113">Return value</span></span>

<span data-ttu-id="5989a-114">Entero que representa el alto preferido del texto del vínculo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="5989a-114">Integer that represents the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="5989a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5989a-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5989a-116">Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="5989a-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5989a-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5989a-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5989a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5989a-118">Requirements</span></span>



| <span data-ttu-id="5989a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5989a-119">Requirement</span></span> | <span data-ttu-id="5989a-120">Value</span><span class="sxs-lookup"><span data-stu-id="5989a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5989a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5989a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5989a-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5989a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5989a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5989a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5989a-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5989a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5989a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5989a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5989a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5989a-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

