---
title: Mensaje de PSM_QUERYSIBLINGS (Prsht. h)
description: Se envía a una hoja de propiedades, que, a continuación, reenvía el mensaje a cada una de sus páginas. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- PSM_QUERYSIBLINGS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534353"
---
# <a name="psm_querysiblings-message"></a><span data-ttu-id="7852b-105">Mensaje de PSM \_ QUERYSIBLINGS</span><span class="sxs-lookup"><span data-stu-id="7852b-105">PSM\_QUERYSIBLINGS message</span></span>

<span data-ttu-id="7852b-106">Se envía a una hoja de propiedades, que, a continuación, reenvía el mensaje a cada una de sus páginas.</span><span class="sxs-lookup"><span data-stu-id="7852b-106">Sent to a property sheet, which then forwards the message to each of its pages.</span></span> <span data-ttu-id="7852b-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .</span><span class="sxs-lookup"><span data-stu-id="7852b-107">You can send this message explicitly or by using the [**PropSheet\_QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7852b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7852b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7852b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7852b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7852b-110">Primer parámetro definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7852b-110">First application-defined parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7852b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7852b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7852b-112">Segundo parámetro definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7852b-112">Second application-defined parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7852b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7852b-113">Return value</span></span>

<span data-ttu-id="7852b-114">Devuelve el valor distinto de cero de una página de la hoja de propiedades, o bien, cero si no hay ninguna página que devuelva un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="7852b-114">Returns the nonzero value from a page in the property sheet, or zero if no page returns a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7852b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7852b-115">Remarks</span></span>

<span data-ttu-id="7852b-116">Si una página devuelve un valor distinto de cero, la hoja de propiedades no envía el mensaje a las páginas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7852b-116">If a page returns a nonzero value, the property sheet does not send the message to subsequent pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="7852b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7852b-117">Requirements</span></span>



| <span data-ttu-id="7852b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7852b-118">Requirement</span></span> | <span data-ttu-id="7852b-119">Value</span><span class="sxs-lookup"><span data-stu-id="7852b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7852b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7852b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7852b-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7852b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7852b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7852b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7852b-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7852b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7852b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7852b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7852b-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="7852b-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





