---
title: Mensaje de PSM_APPLY (Prsht. h)
description: Simula la selección del botón aplicar, que indica que una o más páginas han cambiado y los cambios deben validarse y registrarse.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- PSM_APPLY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905472"
---
# <a name="psm_apply-message"></a><span data-ttu-id="5d895-104">Mensaje de aplicación de PSM \_</span><span class="sxs-lookup"><span data-stu-id="5d895-104">PSM\_APPLY message</span></span>

<span data-ttu-id="5d895-105">Simula la selección del botón **aplicar** , que indica que una o más páginas han cambiado y los cambios deben validarse y registrarse.</span><span class="sxs-lookup"><span data-stu-id="5d895-105">Simulates the selection of the **Apply** button, indicating that one or more pages have changed and the changes need to be validated and recorded.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d895-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d895-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d895-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d895-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d895-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5d895-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5d895-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d895-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d895-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5d895-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d895-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d895-111">Return value</span></span>

<span data-ttu-id="5d895-112">Devuelve **true** si todas las páginas aplicaron correctamente los cambios o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5d895-112">Returns **TRUE** if all pages successfully applied the changes, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d895-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d895-113">Remarks</span></span>

<span data-ttu-id="5d895-114">La hoja de propiedades envía el código de notificación [PSN \_ KILLACTIVE](psn-killactive.md) a la página actual.</span><span class="sxs-lookup"><span data-stu-id="5d895-114">The property sheet sends the [PSN\_KILLACTIVE](psn-killactive.md) notification code to the current page.</span></span> <span data-ttu-id="5d895-115">Si la página actual devuelve **false**, la hoja de propiedades envía [PSN \_ aplicar](psn-apply.md) código de notificación a todas las páginas activas.</span><span class="sxs-lookup"><span data-stu-id="5d895-115">If the current page returns **FALSE**, the property sheet sends the [PSN\_APPLY](psn-apply.md) notification code to all active pages.</span></span> <span data-ttu-id="5d895-116">Puede enviar el mensaje de \_ aplicación PSM explícitamente o mediante la macro [**PropSheet \_ Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) .</span><span class="sxs-lookup"><span data-stu-id="5d895-116">You can send the PSM\_APPLY message explicitly or by using the [**PropSheet\_Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) macro.</span></span>

> [!Note]  
> <span data-ttu-id="5d895-117">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="5d895-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d895-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d895-118">Requirements</span></span>



| <span data-ttu-id="5d895-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d895-119">Requirement</span></span> | <span data-ttu-id="5d895-120">Value</span><span class="sxs-lookup"><span data-stu-id="5d895-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d895-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d895-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5d895-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5d895-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5d895-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d895-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5d895-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d895-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5d895-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d895-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d895-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d895-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





