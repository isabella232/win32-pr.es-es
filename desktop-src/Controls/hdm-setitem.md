---
title: Mensaje de HDM_SETITEM (commctrl. h)
description: Establece los atributos del elemento especificado en un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header setItem.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- HDM_SETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492160"
---
# <a name="hdm_setitem-message"></a><span data-ttu-id="bb842-105">HDM \_ SETITEM</span><span class="sxs-lookup"><span data-stu-id="bb842-105">HDM\_SETITEM message</span></span>

<span data-ttu-id="bb842-106">Establece los atributos del elemento especificado en un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="bb842-106">Sets the attributes of the specified item in a header control.</span></span> <span data-ttu-id="bb842-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) .</span><span class="sxs-lookup"><span data-stu-id="bb842-107">You can send this message explicitly or use the [**Header\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb842-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb842-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb842-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb842-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb842-110">Índice actual del elemento cuyos atributos se van a cambiar.</span><span class="sxs-lookup"><span data-stu-id="bb842-110">The current index of the item whose attributes are to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="bb842-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb842-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb842-112">Puntero a una estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que contiene información del elemento.</span><span class="sxs-lookup"><span data-stu-id="bb842-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains item information.</span></span> <span data-ttu-id="bb842-113">Cuando se envía este mensaje, se debe establecer el miembro de **máscara** de la estructura para indicar los atributos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="bb842-113">When this message is sent, the **mask** member of the structure must be set to indicate which attributes are being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb842-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb842-114">Return value</span></span>

<span data-ttu-id="bb842-115">Devuelve un valor distinto de cero si se ejecuta correctamente o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bb842-115">Returns nonzero upon success, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb842-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb842-116">Remarks</span></span>

<span data-ttu-id="bb842-117">La estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que admite este mensaje es compatible con la información de la lista de imágenes y el orden de los elementos.</span><span class="sxs-lookup"><span data-stu-id="bb842-117">The [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that supports this message supports item order and image list information.</span></span> <span data-ttu-id="bb842-118">Mediante el uso de estos miembros, puede controlar el orden en que se muestran los elementos y especificar las imágenes que aparecerán con los elementos.</span><span class="sxs-lookup"><span data-stu-id="bb842-118">By using these members, you can control the order in which items are displayed and specify images to appear with items.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb842-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb842-119">Requirements</span></span>



| <span data-ttu-id="bb842-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb842-120">Requirement</span></span> | <span data-ttu-id="bb842-121">Value</span><span class="sxs-lookup"><span data-stu-id="bb842-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb842-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb842-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bb842-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bb842-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb842-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb842-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bb842-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb842-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb842-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb842-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb842-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb842-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bb842-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="bb842-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bb842-129">**HDM \_ SETITEMW** (Unicode) y **HDM \_ SETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bb842-129">**HDM\_SETITEMW** (Unicode) and **HDM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





