---
title: Mensaje de HDM_SETHOTDIVIDER (commctrl. h)
description: Cambia el color de un divisor entre los elementos de encabezado para indicar el destino de una operación externa de arrastrar y colocar. Puede enviar este mensaje explícitamente o utilizar la \_ macro header SetHotDivider.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- HDM_SETHOTDIVIDER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb894100878e9b3ee85e8e8367a4b81a022a0a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150229"
---
# <a name="hdm_sethotdivider-message"></a><span data-ttu-id="e9cbe-105">HDM \_ SETHOTDIVIDER</span><span class="sxs-lookup"><span data-stu-id="e9cbe-105">HDM\_SETHOTDIVIDER message</span></span>

<span data-ttu-id="e9cbe-106">Cambia el color de un divisor entre los elementos de encabezado para indicar el destino de una operación externa de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="e9cbe-106">Changes the color of a divider between header items to indicate the destination of an external drag-and-drop operation.</span></span> <span data-ttu-id="e9cbe-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) .</span><span class="sxs-lookup"><span data-stu-id="e9cbe-107">You can send this message explicitly or use the [**Header\_SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9cbe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9cbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9cbe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9cbe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9cbe-110">Tipo de valor representado por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="e9cbe-110">The type of value represented by *lParam*.</span></span> <span data-ttu-id="e9cbe-111">Este valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e9cbe-111">This value can be one of the following:</span></span>



| <span data-ttu-id="e9cbe-112">Value</span><span class="sxs-lookup"><span data-stu-id="e9cbe-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="e9cbe-113">Significado</span><span class="sxs-lookup"><span data-stu-id="e9cbe-113">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="e9cbe-114"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e9cbe-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="e9cbe-115">Indica que *lParam* contiene las coordenadas de cliente del puntero.</span><span class="sxs-lookup"><span data-stu-id="e9cbe-115">Indicates that *lParam* holds the client coordinates of the pointer.</span></span><br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="e9cbe-116"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e9cbe-116"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="e9cbe-117">Indica que *lParam* contiene un valor de índice de división.</span><span class="sxs-lookup"><span data-stu-id="e9cbe-117">Indicates that *lParam* holds a divider index value.</span></span><br/>                 |



 

</dd> <dt>

<span data-ttu-id="e9cbe-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9cbe-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9cbe-119">Un valor contenido en *lParam* se interpreta en función del valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="e9cbe-119">A value held in *lParam* is interpreted depending on the value of *wParam*.</span></span>

<span data-ttu-id="e9cbe-120">Si *wParam* es **true**, *lParam* representa las coordenadas x e y del puntero.</span><span class="sxs-lookup"><span data-stu-id="e9cbe-120">If *wParam* is **TRUE**, *lParam* represents the x- and y-coordinates of the pointer.</span></span> <span data-ttu-id="e9cbe-121">La coordenada x está en la palabra baja y la coordenada y está en la palabra alta.</span><span class="sxs-lookup"><span data-stu-id="e9cbe-121">The x-coordinate is in the low word, and the y-coordinate is in the high word.</span></span> <span data-ttu-id="e9cbe-122">Cuando el control de encabezado recibe el mensaje, resalta el divisor adecuado en función de las coordenadas *lParam* .</span><span class="sxs-lookup"><span data-stu-id="e9cbe-122">When the header control receives the message, it highlights the appropriate divider based on the *lParam* coordinates.</span></span>

<span data-ttu-id="e9cbe-123">Si *wParam* es **false**, *lParam* representa el índice entero del divisor que se va a resaltar.</span><span class="sxs-lookup"><span data-stu-id="e9cbe-123">If *wParam* is **FALSE**, *lParam* represents the integer index of the divider to be highlighted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9cbe-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9cbe-124">Return value</span></span>

<span data-ttu-id="e9cbe-125">Devuelve un valor igual al índice del divisor que resaltó el control.</span><span class="sxs-lookup"><span data-stu-id="e9cbe-125">Returns a value equal to the index of the divider that the control highlighted.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9cbe-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9cbe-126">Remarks</span></span>

<span data-ttu-id="e9cbe-127">Este mensaje crea un efecto de que un control de encabezado produce automáticamente cuando tiene el estilo de controlador de [**HDS \_**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e9cbe-127">This message creates an effect that a header control automatically produces when it has the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="e9cbe-128">El **mensaje \_ SETHOTDIVIDER de HDM** está diseñado para usarse cuando el propietario del control administra las operaciones de arrastrar y colocar manualmente.</span><span class="sxs-lookup"><span data-stu-id="e9cbe-128">The **HDM\_SETHOTDIVIDER** message is intended to be used when the owner of the control handles drag-and-drop operations manually.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9cbe-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9cbe-129">Requirements</span></span>



| <span data-ttu-id="e9cbe-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9cbe-130">Requirement</span></span> | <span data-ttu-id="e9cbe-131">Value</span><span class="sxs-lookup"><span data-stu-id="e9cbe-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9cbe-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9cbe-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e9cbe-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e9cbe-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9cbe-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9cbe-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e9cbe-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9cbe-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9cbe-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9cbe-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9cbe-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9cbe-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





