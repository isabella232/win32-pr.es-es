---
title: Mensaje de CBEM_HASEDITCHANGED (commctrl. h)
description: Determina si el usuario ha cambiado el texto de un control de edición ComboBoxEx.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- CBEM_HASEDITCHANGED controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997116"
---
# <a name="cbem_haseditchanged-message"></a><span data-ttu-id="70a0f-104">CBEM \_ HASEDITCHANGED</span><span class="sxs-lookup"><span data-stu-id="70a0f-104">CBEM\_HASEDITCHANGED message</span></span>

<span data-ttu-id="70a0f-105">Determina si el usuario ha cambiado el texto de un control de edición ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="70a0f-105">Determines whether the user has changed the text of a ComboBoxEx edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="70a0f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70a0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70a0f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70a0f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="70a0f-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="70a0f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="70a0f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70a0f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="70a0f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="70a0f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70a0f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70a0f-111">Return value</span></span>

<span data-ttu-id="70a0f-112">Devuelve **true** si se ha cambiado el texto del cuadro de edición del control o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="70a0f-112">Returns **TRUE** if the text in the control's edit box has been changed, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="70a0f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70a0f-113">Remarks</span></span>

<span data-ttu-id="70a0f-114">Un control ComboBoxEx usa un control de cuadro de edición cuando se establece en el estilo de [**\_ lista desplegable CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="70a0f-114">A ComboBoxEx control uses an edit box control when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="70a0f-115">Puede recuperar el identificador de ventana del control del cuadro de edición mediante el envío de un mensaje de [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="70a0f-115">You can retrieve the edit box control's window handle by sending a [**CBEM\_GETEDITCONTROL**](cbem-geteditcontrol.md) message.</span></span>

<span data-ttu-id="70a0f-116">Cuando el usuario empiece a editar, recibirá una notificación de [CBEN \_ BEGINEDIT](cben-beginedit.md) .</span><span class="sxs-lookup"><span data-stu-id="70a0f-116">When the user begins editing, you will receive a [CBEN\_BEGINEDIT](cben-beginedit.md) notification.</span></span> <span data-ttu-id="70a0f-117">Una vez completada la edición o cambia el foco, recibirá una notificación de [CBEN \_ ENDEDIT](cben-endedit.md) .</span><span class="sxs-lookup"><span data-stu-id="70a0f-117">When editing is complete, or the focus changes, you will receive a [CBEN\_ENDEDIT](cben-endedit.md) notification.</span></span> <span data-ttu-id="70a0f-118">El mensaje **CBEM \_ HASEDITCHANGED** solo es útil para determinar si se ha cambiado el texto en caso de que se envíe antes de la \_ notificación CBEN ENDEDIT.</span><span class="sxs-lookup"><span data-stu-id="70a0f-118">The **CBEM\_HASEDITCHANGED** message is only useful for determining whether the text has been changed if it is sent before the CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="70a0f-119">Si el mensaje se envía después, devolverá **false**.</span><span class="sxs-lookup"><span data-stu-id="70a0f-119">If the message is sent afterward, it will return **FALSE**.</span></span> <span data-ttu-id="70a0f-120">Por ejemplo, supongamos que el usuario comienza a editar el texto en el cuadro de edición pero cambia el foco, generando una notificación de CBEN \_ ENDEDIT.</span><span class="sxs-lookup"><span data-stu-id="70a0f-120">For example, suppose the user starts to edit the text in the edit box but changes focus, generating a CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="70a0f-121">Si, a continuación, envía un mensaje **\_ HASEDITCHANGED de CBEM** , devolverá **false**, aunque el texto se haya cambiado.</span><span class="sxs-lookup"><span data-stu-id="70a0f-121">If you then send a **CBEM\_HASEDITCHANGED** message, it will return **FALSE**, even though the text has been changed.</span></span>

<span data-ttu-id="70a0f-122">El [**estilo \_ simple CBS**](combo-box-styles.md) no funciona correctamente con **CBEM \_ HASEDITCHANGED**.</span><span class="sxs-lookup"><span data-stu-id="70a0f-122">The [**CBS\_SIMPLE**](combo-box-styles.md) style does not work correctly with **CBEM\_HASEDITCHANGED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="70a0f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70a0f-123">Requirements</span></span>



| <span data-ttu-id="70a0f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a0f-124">Requirement</span></span> | <span data-ttu-id="70a0f-125">Value</span><span class="sxs-lookup"><span data-stu-id="70a0f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70a0f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70a0f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="70a0f-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="70a0f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70a0f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70a0f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="70a0f-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="70a0f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70a0f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70a0f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="70a0f-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="70a0f-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





