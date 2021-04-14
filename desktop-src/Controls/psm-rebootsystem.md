---
title: Mensaje de PSM_REBOOTSYSTEM (Prsht. h)
description: Indica que el sistema debe reiniciarse para que los cambios surtan efecto. Puede enviar el mensaje de PSM \_ REBOOTSYSTEM explícitamente o mediante la \_ macro REBOOTSYSTEM de PropSheet.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- PSM_REBOOTSYSTEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489952"
---
# <a name="psm_rebootsystem-message"></a><span data-ttu-id="c09e6-105">Mensaje de PSM \_ REBOOTSYSTEM</span><span class="sxs-lookup"><span data-stu-id="c09e6-105">PSM\_REBOOTSYSTEM message</span></span>

<span data-ttu-id="c09e6-106">Indica que el sistema debe reiniciarse para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="c09e6-106">Indicates the system needs to be restarted for the changes to take effect.</span></span> <span data-ttu-id="c09e6-107">Puede enviar el mensaje de **PSM \_ REBOOTSYSTEM** explícitamente o mediante la [**macro \_ REBOOTSYSTEM de PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .</span><span class="sxs-lookup"><span data-stu-id="c09e6-107">You can send the **PSM\_REBOOTSYSTEM** message explicitly or by using the [**PropSheet\_RebootSystem**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c09e6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c09e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c09e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c09e6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c09e6-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c09e6-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c09e6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c09e6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c09e6-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c09e6-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c09e6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c09e6-113">Return value</span></span>

<span data-ttu-id="c09e6-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c09e6-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c09e6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c09e6-115">Remarks</span></span>

<span data-ttu-id="c09e6-116">Una aplicación debe enviar este mensaje solo en respuesta al mensaje de notificación [PSN \_ Apply](psn-apply.md) o [PSN \_ KILLACTIVE](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="c09e6-116">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification message.</span></span>

<span data-ttu-id="c09e6-117">Este mensaje hace que la función [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelva el \_ valor de identificador PSREBOOTSYSTEM, pero solo si el usuario hace clic en el botón **Aceptar** para cerrar la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c09e6-117">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSREBOOTSYSTEM value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="c09e6-118">Es responsabilidad de la aplicación reiniciar el sistema, lo que se puede hacer mediante la función [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="c09e6-118">It is the application's responsibility to reboot the system, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

<span data-ttu-id="c09e6-119">Este mensaje sustituye a todos los mensajes de [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) que preceden o siguen.</span><span class="sxs-lookup"><span data-stu-id="c09e6-119">This message supersedes all [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) messages that precede or follow it.</span></span>

> [!Note]  
> <span data-ttu-id="c09e6-120">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="c09e6-120">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c09e6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c09e6-121">Requirements</span></span>



| <span data-ttu-id="c09e6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c09e6-122">Requirement</span></span> | <span data-ttu-id="c09e6-123">Value</span><span class="sxs-lookup"><span data-stu-id="c09e6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c09e6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c09e6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c09e6-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c09e6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c09e6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c09e6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c09e6-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c09e6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c09e6-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c09e6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c09e6-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="c09e6-129"><dt>Prsht.h</dt></span></span> </dl> |



 

