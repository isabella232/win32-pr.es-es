---
title: Mensaje de PSM_SETCURSEL (Prsht. h)
description: Activa la página especificada en una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetCurSel.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- PSM_SETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150188"
---
# <a name="psm_setcursel-message"></a><span data-ttu-id="964f9-105">Mensaje de PSM \_ SETCURSEL</span><span class="sxs-lookup"><span data-stu-id="964f9-105">PSM\_SETCURSEL message</span></span>

<span data-ttu-id="964f9-106">Activa la página especificada en una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="964f9-106">Activates the specified page in a property sheet.</span></span> <span data-ttu-id="964f9-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="964f9-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="964f9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="964f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="964f9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="964f9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="964f9-110">Índice de base cero de la página.</span><span class="sxs-lookup"><span data-stu-id="964f9-110">The zero-based index of the page.</span></span> <span data-ttu-id="964f9-111">Una aplicación puede especificar el índice o el identificador o ambos.</span><span class="sxs-lookup"><span data-stu-id="964f9-111">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="964f9-112">Si se especifican ambos, *lParam* tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="964f9-112">If both are specified, *lParam* takes precedence.</span></span>

</dd> <dt>

<span data-ttu-id="964f9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="964f9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="964f9-114">Identificador de la página que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="964f9-114">The handle to the page to activate.</span></span> <span data-ttu-id="964f9-115">Una aplicación puede especificar el índice o el identificador o ambos.</span><span class="sxs-lookup"><span data-stu-id="964f9-115">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="964f9-116">Si se especifican ambos, *lParam* tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="964f9-116">If both are specified, *lParam* takes precedence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="964f9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="964f9-117">Return value</span></span>

<span data-ttu-id="964f9-118">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="964f9-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="964f9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="964f9-119">Remarks</span></span>

<span data-ttu-id="964f9-120">La ventana que está perdiendo la activación recibe el código de notificación [PSN \_ KILLACTIVE](psn-killactive.md) y la ventana que obtiene la activación recibe el código de notificación [PSN \_ SETACTIVE](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="964f9-120">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="964f9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="964f9-121">Requirements</span></span>



| <span data-ttu-id="964f9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="964f9-122">Requirement</span></span> | <span data-ttu-id="964f9-123">Value</span><span class="sxs-lookup"><span data-stu-id="964f9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="964f9-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="964f9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="964f9-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="964f9-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="964f9-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="964f9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="964f9-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="964f9-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="964f9-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="964f9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="964f9-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="964f9-129"><dt>Prsht.h</dt></span></span> </dl> |



 

 





