---
title: Mensaje de PSM_GETTABCONTROL (Prsht. h)
description: Recupera el identificador del control de ficha de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ GetTabControl.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- PSM_GETTABCONTROL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab296159cac4dbfb4ef894d90d31bcd74d6ca2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534912"
---
# <a name="psm_gettabcontrol-message"></a><span data-ttu-id="a02a2-105">Mensaje de PSM \_ GETTABCONTROL</span><span class="sxs-lookup"><span data-stu-id="a02a2-105">PSM\_GETTABCONTROL message</span></span>

<span data-ttu-id="a02a2-106">Recupera el identificador del control de ficha de una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="a02a2-106">Retrieves the handle to the tab control of a property sheet.</span></span> <span data-ttu-id="a02a2-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) .</span><span class="sxs-lookup"><span data-stu-id="a02a2-107">You can send this message explicitly or by using the [**PropSheet\_GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a02a2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a02a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a02a2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a02a2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a02a2-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a02a2-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a02a2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a02a2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a02a2-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a02a2-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a02a2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a02a2-113">Return value</span></span>

<span data-ttu-id="a02a2-114">Devuelve el identificador del control de ficha.</span><span class="sxs-lookup"><span data-stu-id="a02a2-114">Returns the handle to the tab control.</span></span>

## <a name="remarks"></a><span data-ttu-id="a02a2-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a02a2-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a02a2-116">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="a02a2-116">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a02a2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a02a2-117">Requirements</span></span>



| <span data-ttu-id="a02a2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a02a2-118">Requirement</span></span> | <span data-ttu-id="a02a2-119">Value</span><span class="sxs-lookup"><span data-stu-id="a02a2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a02a2-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a02a2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a02a2-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a02a2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a02a2-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a02a2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a02a2-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a02a2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a02a2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a02a2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a02a2-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a02a2-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





