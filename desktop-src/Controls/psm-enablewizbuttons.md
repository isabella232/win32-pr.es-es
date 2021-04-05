---
title: Mensaje de PSM_ENABLEWIZBUTTONS (Prsht. h)
description: Habilita o deshabilita cualquiera de los botones estándar en un asistente de Aero. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet EnableWizButtons.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- PSM_ENABLEWIZBUTTONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996642"
---
# <a name="psm_enablewizbuttons-message"></a><span data-ttu-id="25c1c-105">Mensaje de PSM \_ ENABLEWIZBUTTONS</span><span class="sxs-lookup"><span data-stu-id="25c1c-105">PSM\_ENABLEWIZBUTTONS message</span></span>

<span data-ttu-id="25c1c-106">Habilita o deshabilita cualquiera de los botones estándar en un asistente de Aero.</span><span class="sxs-lookup"><span data-stu-id="25c1c-106">Enables or disables any of the standard buttons in an Aero wizard.</span></span> <span data-ttu-id="25c1c-107">Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .</span><span class="sxs-lookup"><span data-stu-id="25c1c-107">You can send this message explicitly or use the [**PropSheet\_EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="25c1c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25c1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25c1c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25c1c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25c1c-110">Uno o varios de los siguientes valores que especifican qué botones de la hoja de propiedades se van a habilitar.</span><span class="sxs-lookup"><span data-stu-id="25c1c-110">One or more of the following values that specify which property sheet buttons are to be enabled.</span></span> <span data-ttu-id="25c1c-111">Si un valor de botón está incluido en este parámetro y *lParam*, se habilita.</span><span class="sxs-lookup"><span data-stu-id="25c1c-111">If a button value is included in both this parameter and *lParam*, it is enabled.</span></span>



| <span data-ttu-id="25c1c-112">Value</span><span class="sxs-lookup"><span data-stu-id="25c1c-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="25c1c-113">Significado</span><span class="sxs-lookup"><span data-stu-id="25c1c-113">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="25c1c-114"><dt>**PSWIZB \_ atrás**</dt></span><span class="sxs-lookup"><span data-stu-id="25c1c-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="25c1c-115">Botón **atrás** .</span><span class="sxs-lookup"><span data-stu-id="25c1c-115">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="25c1c-116"><dt>**\_Cancelar PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="25c1c-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="25c1c-117">Botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="25c1c-117">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="25c1c-118"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="25c1c-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="25c1c-119">El botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="25c1c-119">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="25c1c-120"><dt>**\_Finalizar PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="25c1c-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="25c1c-121">El botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="25c1c-121">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="25c1c-122"><dt>**PSWIZB \_ siguiente**</dt></span><span class="sxs-lookup"><span data-stu-id="25c1c-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="25c1c-123">Botón **siguiente** .</span><span class="sxs-lookup"><span data-stu-id="25c1c-123">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="25c1c-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25c1c-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25c1c-125">Uno o varios de los mismos valores utilizados en *wParam*, que especifican qué botones se ven afectados por esta llamada.</span><span class="sxs-lookup"><span data-stu-id="25c1c-125">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="25c1c-126">Si aparece un valor de botón en este parámetro pero no en *wParam*, indica que se debe deshabilitar el botón.</span><span class="sxs-lookup"><span data-stu-id="25c1c-126">If a button value appears in this parameter but not in *wParam*, it indicates that the button should be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25c1c-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25c1c-127">Return value</span></span>

<span data-ttu-id="25c1c-128">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="25c1c-128">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="25c1c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25c1c-129">Requirements</span></span>



| <span data-ttu-id="25c1c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="25c1c-130">Requirement</span></span> | <span data-ttu-id="25c1c-131">Value</span><span class="sxs-lookup"><span data-stu-id="25c1c-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25c1c-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25c1c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="25c1c-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="25c1c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="25c1c-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25c1c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="25c1c-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="25c1c-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="25c1c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25c1c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="25c1c-137"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="25c1c-137"><dt>Prsht.h</dt></span></span> </dl> |



 

 





