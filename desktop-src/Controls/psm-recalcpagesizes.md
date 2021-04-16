---
title: Mensaje de PSM_RECALCPAGESIZES (Prsht. h)
description: Vuelve a calcular el tamaño de página de una hoja de propiedades estándar o del asistente después de que se hayan agregado o quitado páginas. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet RecalcPageSizes.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- PSM_RECALCPAGESIZES controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658315"
---
# <a name="psm_recalcpagesizes-message"></a><span data-ttu-id="fba30-105">Mensaje de PSM \_ RECALCPAGESIZES</span><span class="sxs-lookup"><span data-stu-id="fba30-105">PSM\_RECALCPAGESIZES message</span></span>

<span data-ttu-id="fba30-106">Vuelve a calcular el tamaño de página de una hoja de propiedades estándar o del asistente después de que se hayan agregado o quitado páginas.</span><span class="sxs-lookup"><span data-stu-id="fba30-106">Recalculates the page size of a standard or wizard property sheet after pages have been added or removed.</span></span> <span data-ttu-id="fba30-107">Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .</span><span class="sxs-lookup"><span data-stu-id="fba30-107">You can send this message explicitly or use the [**PropSheet\_RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fba30-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fba30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba30-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fba30-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fba30-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fba30-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fba30-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fba30-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fba30-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fba30-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba30-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fba30-113">Return value</span></span>

<span data-ttu-id="fba30-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fba30-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fba30-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fba30-115">Remarks</span></span>

<span data-ttu-id="fba30-116">Cuando se crea una hoja de propiedades, se ajusta para ajustarse a su colección inicial de páginas.</span><span class="sxs-lookup"><span data-stu-id="fba30-116">When a property sheet is created, it is sized to fit its initial collection of pages.</span></span> <span data-ttu-id="fba30-117">Con el fin de mantener la compatibilidad con versiones anteriores de los controles comunes, las hojas de propiedades y los asistentes no cambian de tamaño automáticamente cuando se agregan o quitan páginas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="fba30-117">In order to maintain compatibility with previous versions of the common controls, property sheets and wizards do not automatically resize themselves when pages are subsequently added or removed.</span></span> <span data-ttu-id="fba30-118">Con los controles comunes [versión 5,80](common-control-versions.md), las aplicaciones deben enviar un mensaje de **PSM \_ RECALCPAGESIZES** después de agregar o quitar páginas con [**PSM \_ ADDPAGE**](psm-addpage.md), [**PSM \_ INSERTPAGE**](psm-insertpage.md), [**PSM \_ REMOVEPAGE**](psm-removepage.md)o sus macros equivalentes.</span><span class="sxs-lookup"><span data-stu-id="fba30-118">With common controls [version 5.80](common-control-versions.md), applications should send a **PSM\_RECALCPAGESIZES** message after adding or removing pages with [**PSM\_ADDPAGE**](psm-addpage.md), [**PSM\_INSERTPAGE**](psm-insertpage.md), [**PSM\_REMOVEPAGE**](psm-removepage.md), or their equivalent macros.</span></span> <span data-ttu-id="fba30-119">Garantiza que la hoja de propiedades tenga el tamaño adecuado para su colección actual de páginas.</span><span class="sxs-lookup"><span data-stu-id="fba30-119">It ensures that the property sheet is properly sized for its current collection of pages.</span></span> <span data-ttu-id="fba30-120">Si no se envía este mensaje, es posible que algunas páginas de hojas de propiedades estén truncadas o sean demasiado grandes.</span><span class="sxs-lookup"><span data-stu-id="fba30-120">If this message is not sent, some property sheet pages may be truncated or too large.</span></span>

> [!Note]  
> <span data-ttu-id="fba30-121">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="fba30-121">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fba30-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fba30-122">Requirements</span></span>



| <span data-ttu-id="fba30-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fba30-123">Requirement</span></span> | <span data-ttu-id="fba30-124">Value</span><span class="sxs-lookup"><span data-stu-id="fba30-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fba30-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fba30-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fba30-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fba30-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fba30-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fba30-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fba30-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fba30-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fba30-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fba30-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fba30-130"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="fba30-130"><dt>Prsht.h</dt></span></span> </dl> |



 

 





