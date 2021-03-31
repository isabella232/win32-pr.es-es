---
title: Mensaje de PSM_CANCELTOCLOSE (Prsht. h)
description: Enviado por una aplicación cuando se han realizado cambios desde la notificación de aplicación de PSN más reciente \_ que no se puede cancelar. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ CancelToClose.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- PSM_CANCELTOCLOSE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150818"
---
# <a name="psm_canceltoclose-message"></a><span data-ttu-id="02491-105">Mensaje de PSM \_ CANCELTOCLOSE</span><span class="sxs-lookup"><span data-stu-id="02491-105">PSM\_CANCELTOCLOSE message</span></span>

<span data-ttu-id="02491-106">Enviado por una aplicación cuando se han realizado cambios desde la notificación de [ \_ aplicación de PSN](psn-apply.md) más reciente que no se puede cancelar.</span><span class="sxs-lookup"><span data-stu-id="02491-106">Sent by an application when it has performed changes since the most recent [PSN\_APPLY](psn-apply.md) notification that cannot be canceled.</span></span> <span data-ttu-id="02491-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .</span><span class="sxs-lookup"><span data-stu-id="02491-107">You can send this message explicitly or by using the [**PropSheet\_CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="02491-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02491-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02491-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02491-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02491-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="02491-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="02491-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02491-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02491-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="02491-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02491-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02491-113">Return value</span></span>

<span data-ttu-id="02491-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="02491-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02491-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02491-115">Remarks</span></span>

<span data-ttu-id="02491-116">**PSM \_ CANCELTOCLOSE** deshabilita el botón **Cancelar** y cambia el texto del botón **Aceptar** a "cerrar".</span><span class="sxs-lookup"><span data-stu-id="02491-116">**PSM\_CANCELTOCLOSE** disables the **Cancel** button and changes the text of the **OK** button to "Close".</span></span>

<span data-ttu-id="02491-117">La mayoría de las hojas de propiedades esperan a realizar cambios irreversibles hasta que \_ se recibe una notificación de aplicación de PSN.</span><span class="sxs-lookup"><span data-stu-id="02491-117">Most property sheets wait to perform irreversible changes until a PSN\_APPLY notification is received.</span></span> <span data-ttu-id="02491-118">Sin embargo, en algunas circunstancias, una hoja de propiedades puede realizar cambios irreversibles fuera de la secuencia de restablecimiento de PSN estándar \_ Apply/PSN \_ .</span><span class="sxs-lookup"><span data-stu-id="02491-118">However, in some circumstances, a property sheet may make irreversible changes outside the standard PSN\_APPLY/PSN\_RESET sequence.</span></span> <span data-ttu-id="02491-119">Un ejemplo es una hoja de propiedades que contiene un botón **Editar** que se utiliza para mostrar un cuadro de diálogo para editar una propiedad.</span><span class="sxs-lookup"><span data-stu-id="02491-119">One example is a property sheet that contains an **Edit** button that is used to display a subdialog box for editing a property.</span></span> <span data-ttu-id="02491-120">Cuando el usuario hace clic en **Aceptar** para enviar el cambio, la página de la hoja de propiedades tiene varias opciones.</span><span class="sxs-lookup"><span data-stu-id="02491-120">When the user clicks **OK** to submit the change, the property sheet page has several options.</span></span>

-   <span data-ttu-id="02491-121">Puede registrar los cambios, pero espere hasta que reciba una notificación de \_ aplicación de PSN para aplicarlos.</span><span class="sxs-lookup"><span data-stu-id="02491-121">It can record the changes, but wait until it receives a PSN\_APPLY notification to apply them.</span></span> <span data-ttu-id="02491-122">Este es el método preferido.</span><span class="sxs-lookup"><span data-stu-id="02491-122">This is the preferred approach.</span></span>
-   <span data-ttu-id="02491-123">Puede aplicar los cambios inmediatamente después de salir del cuadro de diálogo, pero recuerde la configuración original.</span><span class="sxs-lookup"><span data-stu-id="02491-123">It can apply the changes immediately after exiting the subdialog box, but remember the original settings.</span></span> <span data-ttu-id="02491-124">Esta configuración se puede usar para restaurar el estado original si \_ se recibe una notificación de restablecimiento de PSN.</span><span class="sxs-lookup"><span data-stu-id="02491-124">Those settings can be used to restore the original state if a PSN\_RESET notification is received.</span></span>
-   <span data-ttu-id="02491-125">Puede aplicar los cambios inmediatamente y no intentar restaurar la configuración original cuando recibe una notificación de [ \_ restablecimiento de PSN](psn-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="02491-125">It can apply the changes immediately and not attempt to restore the original settings when it receives a [PSN\_RESET](psn-reset.md) notification.</span></span> <span data-ttu-id="02491-126">Este enfoque no se recomienda, pero puede ser necesario si los cambios son demasiado expuestos para que las otras dos opciones resulten prácticas.</span><span class="sxs-lookup"><span data-stu-id="02491-126">This approach is not recommended, but may be necessary if the changes are too far-reaching for the other two options to be practical.</span></span>

<span data-ttu-id="02491-127">En la tercera opción, las aplicaciones deben enviar un mensaje de **PSM \_ CANCELTOCLOSE** a la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="02491-127">For the third option, applications should send a **PSM\_CANCELTOCLOSE** message to the property sheet.</span></span> <span data-ttu-id="02491-128">Indica al usuario que no se pueden revertir los cambios realizados con el cuadro de diálogo haciendo clic en el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="02491-128">It indicates to the user that the changes made with the subdialog box cannot be reversed by clicking the **Cancel** button.</span></span>

> [!Note]  
> <span data-ttu-id="02491-129">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="02491-129">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02491-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02491-130">Requirements</span></span>



| <span data-ttu-id="02491-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="02491-131">Requirement</span></span> | <span data-ttu-id="02491-132">Value</span><span class="sxs-lookup"><span data-stu-id="02491-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02491-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02491-133">Minimum supported client</span></span><br/> | <span data-ttu-id="02491-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="02491-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="02491-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02491-135">Minimum supported server</span></span><br/> | <span data-ttu-id="02491-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="02491-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="02491-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02491-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="02491-138"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="02491-138"><dt>Prsht.h</dt></span></span> </dl> |



 

 





