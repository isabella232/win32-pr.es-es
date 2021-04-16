---
title: Mensaje de PSM_CHANGED (Prsht. h)
description: Informa a una hoja de propiedades de que la información de una página ha cambiado. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ Changed.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- PSM_CHANGED controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f931db5e25f816f7ea164ca5871a4e3e7757a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658318"
---
# <a name="psm_changed-message"></a><span data-ttu-id="defd1-105">Mensaje de PSM \_ cambiado</span><span class="sxs-lookup"><span data-stu-id="defd1-105">PSM\_CHANGED message</span></span>

<span data-ttu-id="defd1-106">Informa a una hoja de propiedades de que la información de una página ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="defd1-106">Informs a property sheet that information in a page has changed.</span></span> <span data-ttu-id="defd1-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) .</span><span class="sxs-lookup"><span data-stu-id="defd1-107">You can send this message explicitly or by using the [**PropSheet\_Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="defd1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="defd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="defd1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="defd1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="defd1-110">Identificador de la página que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="defd1-110">Handle to the page that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="defd1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="defd1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="defd1-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="defd1-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="defd1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="defd1-113">Return value</span></span>

<span data-ttu-id="defd1-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="defd1-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="defd1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="defd1-115">Remarks</span></span>

<span data-ttu-id="defd1-116">La hoja de propiedades habilitará el botón **aplicar** .</span><span class="sxs-lookup"><span data-stu-id="defd1-116">The property sheet will enable the **Apply** button.</span></span>

> [!Note]  
> <span data-ttu-id="defd1-117">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="defd1-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="defd1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="defd1-118">Requirements</span></span>



| <span data-ttu-id="defd1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="defd1-119">Requirement</span></span> | <span data-ttu-id="defd1-120">Value</span><span class="sxs-lookup"><span data-stu-id="defd1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="defd1-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="defd1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="defd1-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="defd1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="defd1-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="defd1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="defd1-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="defd1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="defd1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="defd1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="defd1-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="defd1-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





