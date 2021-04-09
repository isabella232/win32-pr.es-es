---
title: Mensaje de PSM_SETBUTTONTEXT (Prsht. h)
description: Establece el texto de un botón en un asistente de Aero. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetButtonText.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- PSM_SETBUTTONTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079264"
---
# <a name="psm_setbuttontext-message"></a><span data-ttu-id="67ea7-105">Mensaje de PSM \_ SETBUTTONTEXT</span><span class="sxs-lookup"><span data-stu-id="67ea7-105">PSM\_SETBUTTONTEXT message</span></span>

<span data-ttu-id="67ea7-106">Establece el texto de un botón en un asistente de Aero.</span><span class="sxs-lookup"><span data-stu-id="67ea7-106">Sets the text on a button in an Aero wizard.</span></span> <span data-ttu-id="67ea7-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .</span><span class="sxs-lookup"><span data-stu-id="67ea7-107">You can send this message explicitly or by using the [**PropSheet\_SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="67ea7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67ea7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67ea7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67ea7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67ea7-110">Uno de los siguientes valores que especifican el botón cuyo texto se establece.</span><span class="sxs-lookup"><span data-stu-id="67ea7-110">One of the following values specifying the button whose text is set.</span></span>



| <span data-ttu-id="67ea7-111">Value</span><span class="sxs-lookup"><span data-stu-id="67ea7-111">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="67ea7-112">Significado</span><span class="sxs-lookup"><span data-stu-id="67ea7-112">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="67ea7-113"><dt>**PSWIZB \_ atrás**</dt></span><span class="sxs-lookup"><span data-stu-id="67ea7-113"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="67ea7-114">Botón **atrás** .</span><span class="sxs-lookup"><span data-stu-id="67ea7-114">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="67ea7-115"><dt>**\_Cancelar PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="67ea7-115"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="67ea7-116">Botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="67ea7-116">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="67ea7-117"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="67ea7-117"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="67ea7-118">El botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="67ea7-118">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="67ea7-119"><dt>**\_Finalizar PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="67ea7-119"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="67ea7-120">El botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="67ea7-120">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="67ea7-121"><dt>**PSWIZB \_ siguiente**</dt></span><span class="sxs-lookup"><span data-stu-id="67ea7-121"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="67ea7-122">Botón **siguiente** .</span><span class="sxs-lookup"><span data-stu-id="67ea7-122">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="67ea7-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67ea7-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67ea7-124">Texto que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="67ea7-124">The text to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67ea7-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67ea7-125">Return value</span></span>

<span data-ttu-id="67ea7-126">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="67ea7-126">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="67ea7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67ea7-127">Requirements</span></span>



| <span data-ttu-id="67ea7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="67ea7-128">Requirement</span></span> | <span data-ttu-id="67ea7-129">Value</span><span class="sxs-lookup"><span data-stu-id="67ea7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67ea7-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67ea7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="67ea7-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="67ea7-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="67ea7-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67ea7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="67ea7-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="67ea7-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="67ea7-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67ea7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="67ea7-135"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="67ea7-135"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="67ea7-136">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="67ea7-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="67ea7-137">**PSM \_ SETBUTTONTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="67ea7-137">**PSM\_SETBUTTONTEXTW** (Unicode)</span></span><br/>                                       |



 

 





