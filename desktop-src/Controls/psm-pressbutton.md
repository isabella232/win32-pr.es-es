---
title: Mensaje de PSM_PRESSBUTTON (Prsht. h)
description: Simula la selección de un botón de la hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ PressButton.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- PSM_PRESSBUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493301"
---
# <a name="psm_pressbutton-message"></a><span data-ttu-id="97e14-105">Mensaje de PSM \_ PRESSBUTTON</span><span class="sxs-lookup"><span data-stu-id="97e14-105">PSM\_PRESSBUTTON message</span></span>

<span data-ttu-id="97e14-106">Simula la selección de un botón de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="97e14-106">Simulates the selection of a property sheet button.</span></span> <span data-ttu-id="97e14-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) .</span><span class="sxs-lookup"><span data-stu-id="97e14-107">You can send this message explicitly or by using the [**PropSheet\_PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="97e14-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97e14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97e14-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97e14-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97e14-110">Índice del botón que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="97e14-110">Index of the button to select.</span></span> <span data-ttu-id="97e14-111">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="97e14-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="97e14-112">Valor</span><span class="sxs-lookup"><span data-stu-id="97e14-112">Value</span></span>                                                                                                                                                            | <span data-ttu-id="97e14-113">Significado</span><span class="sxs-lookup"><span data-stu-id="97e14-113">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <span data-ttu-id="97e14-114"><dt>**PSBTN \_ APPLYNOW**</dt></span><span class="sxs-lookup"><span data-stu-id="97e14-114"><dt>**PSBTN\_APPLYNOW**</dt></span></span> </dl> | <span data-ttu-id="97e14-115">Selecciona el botón **aplicar** .</span><span class="sxs-lookup"><span data-stu-id="97e14-115">Selects the **Apply** button.</span></span> <span data-ttu-id="97e14-116">Este valor no es válido cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="97e14-116">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <span data-ttu-id="97e14-117"><dt>**PSBTN \_ atrás**</dt></span><span class="sxs-lookup"><span data-stu-id="97e14-117"><dt>**PSBTN\_BACK**</dt></span></span> </dl>             | <span data-ttu-id="97e14-118">Selecciona el botón **atrás** .</span><span class="sxs-lookup"><span data-stu-id="97e14-118">Selects the **Back** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <span data-ttu-id="97e14-119"><dt>**\_Cancelar PSBTN**</dt></span><span class="sxs-lookup"><span data-stu-id="97e14-119"><dt>**PSBTN\_CANCEL**</dt></span></span> </dl>       | <span data-ttu-id="97e14-120">Selecciona el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="97e14-120">Selects the **Cancel** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <span data-ttu-id="97e14-121"><dt>**\_Finalizar PSBTN**</dt></span><span class="sxs-lookup"><span data-stu-id="97e14-121"><dt>**PSBTN\_FINISH**</dt></span></span> </dl>       | <span data-ttu-id="97e14-122">Selecciona el botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="97e14-122">Selects the **Finish** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <span data-ttu-id="97e14-123"><dt>**ayuda de PSBTN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97e14-123"><dt>**PSBTN\_HELP**</dt></span></span> </dl>             | <span data-ttu-id="97e14-124">Selecciona el botón **ayuda** .</span><span class="sxs-lookup"><span data-stu-id="97e14-124">Selects the **Help** button.</span></span> <span data-ttu-id="97e14-125">Este valor no es válido cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="97e14-125">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <span data-ttu-id="97e14-126"><dt>**PSBTN \_ siguiente**</dt></span><span class="sxs-lookup"><span data-stu-id="97e14-126"><dt>**PSBTN\_NEXT**</dt></span></span> </dl>             | <span data-ttu-id="97e14-127">Selecciona el botón **siguiente** .</span><span class="sxs-lookup"><span data-stu-id="97e14-127">Selects the **Next** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <span data-ttu-id="97e14-128"><dt>**PSBTN \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="97e14-128"><dt>**PSBTN\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="97e14-129">Selecciona el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="97e14-129">Selects the **OK** button.</span></span> <span data-ttu-id="97e14-130">Este valor no es válido cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="97e14-130">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="97e14-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97e14-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97e14-132">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="97e14-132">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97e14-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97e14-133">Return value</span></span>

<span data-ttu-id="97e14-134">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="97e14-134">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e14-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97e14-135">Requirements</span></span>



| <span data-ttu-id="97e14-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="97e14-136">Requirement</span></span> | <span data-ttu-id="97e14-137">Value</span><span class="sxs-lookup"><span data-stu-id="97e14-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97e14-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97e14-138">Minimum supported client</span></span><br/> | <span data-ttu-id="97e14-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="97e14-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="97e14-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97e14-140">Minimum supported server</span></span><br/> | <span data-ttu-id="97e14-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="97e14-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="97e14-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97e14-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="97e14-143"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="97e14-143"><dt>Prsht.h</dt></span></span> </dl> |



 

 





