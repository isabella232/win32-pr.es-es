---
title: Mensaje de BCM_GETTEXTMARGIN (commctrl. h)
description: Obtiene los márgenes utilizados para dibujar texto en un control de botón. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button GetTextMargin.
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- BCM_GETTEXTMARGIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a7d809207c21c74a36c796a9035ed0e3772481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996293"
---
# <a name="bcm_gettextmargin-message"></a><span data-ttu-id="7ab0f-105">\_Mensaje GETTEXTMARGIN de BCM</span><span class="sxs-lookup"><span data-stu-id="7ab0f-105">BCM\_GETTEXTMARGIN message</span></span>

<span data-ttu-id="7ab0f-106">Obtiene los márgenes utilizados para dibujar texto en un control de botón.</span><span class="sxs-lookup"><span data-stu-id="7ab0f-106">Gets the margins used to draw text in a button control.</span></span> <span data-ttu-id="7ab0f-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) .</span><span class="sxs-lookup"><span data-stu-id="7ab0f-107">You can send this message explicitly or use the [**Button\_GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ab0f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ab0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ab0f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ab0f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ab0f-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7ab0f-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7ab0f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ab0f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ab0f-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene los márgenes que se van a usar para dibujar el texto.</span><span class="sxs-lookup"><span data-stu-id="7ab0f-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ab0f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ab0f-113">Return value</span></span>

<span data-ttu-id="7ab0f-114">Si el mensaje se realiza correctamente, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="7ab0f-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="7ab0f-115">En caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="7ab0f-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ab0f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ab0f-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ab0f-117">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="7ab0f-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="7ab0f-118">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7ab0f-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ab0f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ab0f-119">Requirements</span></span>



| <span data-ttu-id="7ab0f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ab0f-120">Requirement</span></span> | <span data-ttu-id="7ab0f-121">Value</span><span class="sxs-lookup"><span data-stu-id="7ab0f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab0f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ab0f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7ab0f-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7ab0f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ab0f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ab0f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7ab0f-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ab0f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ab0f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ab0f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ab0f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ab0f-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

