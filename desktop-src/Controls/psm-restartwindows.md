---
title: Mensaje de PSM_RESTARTWINDOWS (Prsht. h)
description: Indica que es necesario reiniciar Windows para que los cambios surtan efecto.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- PSM_RESTARTWINDOWS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905170"
---
# <a name="psm_restartwindows-message"></a><span data-ttu-id="e03fe-104">Mensaje de PSM \_ RESTARTWINDOWS</span><span class="sxs-lookup"><span data-stu-id="e03fe-104">PSM\_RESTARTWINDOWS message</span></span>

<span data-ttu-id="e03fe-105">Indica que es necesario reiniciar Windows para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="e03fe-105">Indicates that Windows needs to be restarted for the changes to take effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="e03fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e03fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e03fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e03fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e03fe-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e03fe-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e03fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e03fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e03fe-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e03fe-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e03fe-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e03fe-111">Return value</span></span>

<span data-ttu-id="e03fe-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e03fe-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e03fe-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e03fe-113">Remarks</span></span>

<span data-ttu-id="e03fe-114">Una aplicación debe enviar este mensaje solo en respuesta al código de notificación [PSN \_ Apply](psn-apply.md) o [PSN \_ KILLACTIVE](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="e03fe-114">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span> <span data-ttu-id="e03fe-115">Puede enviar el mensaje de **PSM \_ RESTARTWINDOWS** explícitamente o mediante la [**macro \_ RESTARTWINDOWS de PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) .</span><span class="sxs-lookup"><span data-stu-id="e03fe-115">You can send the **PSM\_RESTARTWINDOWS** message explicitly or by using the [**PropSheet\_RestartWindows**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) macro.</span></span>

<span data-ttu-id="e03fe-116">Este mensaje hace que la función [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelva el \_ valor de identificador PSRESTARTWINDOWS, pero solo si el usuario hace clic en el botón **Aceptar** para cerrar la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e03fe-116">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSRESTARTWINDOWS value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="e03fe-117">Es responsabilidad de la aplicación reiniciar Windows, lo que se puede hacer mediante la función [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="e03fe-117">It is the application's responsibility to restart Windows, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

> [!Note]  
> <span data-ttu-id="e03fe-118">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="e03fe-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e03fe-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e03fe-119">Requirements</span></span>



| <span data-ttu-id="e03fe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e03fe-120">Requirement</span></span> | <span data-ttu-id="e03fe-121">Value</span><span class="sxs-lookup"><span data-stu-id="e03fe-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e03fe-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e03fe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e03fe-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e03fe-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e03fe-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e03fe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e03fe-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e03fe-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e03fe-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e03fe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e03fe-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="e03fe-127"><dt>Prsht.h</dt></span></span> </dl> |



 

