---
title: Mensaje de PSM_SETFINISHTEXT (Prsht. h)
description: Establece el texto del botón Finalizar en un asistente, muestra y habilita el botón, y oculta los botones siguiente y atrás. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetFinishText.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- PSM_SETFINISHTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801225"
---
# <a name="psm_setfinishtext-message"></a><span data-ttu-id="1cbc0-105">Mensaje de PSM \_ SETFINISHTEXT</span><span class="sxs-lookup"><span data-stu-id="1cbc0-105">PSM\_SETFINISHTEXT message</span></span>

<span data-ttu-id="1cbc0-106">Establece el texto del botón **Finalizar** en un asistente, muestra y habilita el botón, y oculta los botones **siguiente** y **atrás** .</span><span class="sxs-lookup"><span data-stu-id="1cbc0-106">Sets the text of the **Finish** button in a wizard, shows and enables the button, and hides the **Next** and **Back** buttons.</span></span> <span data-ttu-id="1cbc0-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .</span><span class="sxs-lookup"><span data-stu-id="1cbc0-107">You can send this message explicitly or by using the [**PropSheet\_SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1cbc0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cbc0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cbc0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1cbc0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cbc0-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1cbc0-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1cbc0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1cbc0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cbc0-112">Puntero al nuevo texto para el botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="1cbc0-112">Pointer to the new text for the **Finish** button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cbc0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cbc0-113">Return value</span></span>

<span data-ttu-id="1cbc0-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1cbc0-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cbc0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cbc0-115">Remarks</span></span>

<span data-ttu-id="1cbc0-116">De forma predeterminada, el botón **Finalizar** no tiene una tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="1cbc0-116">By default, the **Finish** button does not have a keyboard accelerator.</span></span> <span data-ttu-id="1cbc0-117">Puede crear una tecla de aceleración con este mensaje incluyendo una y comercial (&) en la cadena de texto que asigna a *lParam*.</span><span class="sxs-lookup"><span data-stu-id="1cbc0-117">You can create a keyboard accelerator with this message by including an ampersand (&) in the text string that you assign to *lParam*.</span></span> <span data-ttu-id="1cbc0-118">Por ejemplo, "&Finish" define F como la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="1cbc0-118">For example, "&Finish" defines F as the accelerator key.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cbc0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cbc0-119">Requirements</span></span>



| <span data-ttu-id="1cbc0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cbc0-120">Requirement</span></span> | <span data-ttu-id="1cbc0-121">Value</span><span class="sxs-lookup"><span data-stu-id="1cbc0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbc0-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cbc0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1cbc0-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1cbc0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1cbc0-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cbc0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1cbc0-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1cbc0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1cbc0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cbc0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cbc0-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cbc0-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="1cbc0-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1cbc0-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1cbc0-129">**PSM \_ SETFINISHTEXTW** (Unicode) y **PSM \_ SETFINISHTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1cbc0-129">**PSM\_SETFINISHTEXTW** (Unicode) and **PSM\_SETFINISHTEXTA** (ANSI)</span></span><br/>    |



 

 





