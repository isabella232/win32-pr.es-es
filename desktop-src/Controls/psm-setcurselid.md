---
title: Mensaje de PSM_SETCURSELID (Prsht. h)
description: Activa la página especificada en una hoja de propiedades basándose en el identificador de recursos de la página. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetCurSelByID.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- PSM_SETCURSELID controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150754"
---
# <a name="psm_setcurselid-message"></a><span data-ttu-id="109b6-105">Mensaje de PSM \_ SETCURSELID</span><span class="sxs-lookup"><span data-stu-id="109b6-105">PSM\_SETCURSELID message</span></span>

<span data-ttu-id="109b6-106">Activa la página especificada en una hoja de propiedades basándose en el identificador de recursos de la página.</span><span class="sxs-lookup"><span data-stu-id="109b6-106">Activates the given page in a property sheet based on the resource identifier of the page.</span></span> <span data-ttu-id="109b6-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .</span><span class="sxs-lookup"><span data-stu-id="109b6-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="109b6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="109b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="109b6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="109b6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="109b6-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="109b6-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="109b6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="109b6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="109b6-112">Identificador de recurso de la página que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="109b6-112">Resource identifier of the page to activate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="109b6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="109b6-113">Return value</span></span>

<span data-ttu-id="109b6-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="109b6-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="109b6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="109b6-115">Remarks</span></span>

<span data-ttu-id="109b6-116">La ventana que está perdiendo la activación recibe el código de notificación [PSN \_ KILLACTIVE](psn-killactive.md) y la ventana que obtiene la activación recibe el código de notificación [PSN \_ SETACTIVE](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="109b6-116">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="109b6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="109b6-117">Requirements</span></span>



| <span data-ttu-id="109b6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="109b6-118">Requirement</span></span> | <span data-ttu-id="109b6-119">Value</span><span class="sxs-lookup"><span data-stu-id="109b6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="109b6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="109b6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="109b6-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="109b6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="109b6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="109b6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="109b6-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="109b6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="109b6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="109b6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="109b6-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="109b6-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





