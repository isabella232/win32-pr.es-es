---
title: Mensaje de HDM_EDITFILTER (commctrl. h)
description: Mueve el foco de entrada al cuadro de edición cuando un botón de filtro tiene el foco.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- HDM_EDITFILTER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733c79bf747d3b55aa8dd38eb8fad8fdc83601e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802863"
---
# <a name="hdm_editfilter-message"></a><span data-ttu-id="2bce7-104">HDM \_ EDITFILTER</span><span class="sxs-lookup"><span data-stu-id="2bce7-104">HDM\_EDITFILTER message</span></span>

<span data-ttu-id="2bce7-105">Mueve el foco de entrada al cuadro de edición cuando un botón de filtro tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="2bce7-105">Moves the input focus to the edit box when a filter button has the focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="2bce7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bce7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bce7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2bce7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2bce7-108">Valor que especifica la columna que se va a editar.</span><span class="sxs-lookup"><span data-stu-id="2bce7-108">A value specifying the column to edit.</span></span>

</dd> <dt>

<span data-ttu-id="2bce7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2bce7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2bce7-110">Marca que especifica cómo controlar los cambios de edición del usuario.</span><span class="sxs-lookup"><span data-stu-id="2bce7-110">A flag that specifies how to handle the user's editing changes.</span></span> <span data-ttu-id="2bce7-111">Use esta marca para especificar qué hacer si el usuario se encuentra en el proceso de edición del filtro cuando se envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="2bce7-111">Use this flag to specify what to do if the user is in the process of editing the filter when the message is sent.</span></span>



| <span data-ttu-id="2bce7-112">Value</span><span class="sxs-lookup"><span data-stu-id="2bce7-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="2bce7-113">Significado</span><span class="sxs-lookup"><span data-stu-id="2bce7-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="2bce7-114"><dt></dt><dt> **True**</dt></span><span class="sxs-lookup"><span data-stu-id="2bce7-114"><dt></dt> <dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="2bce7-115">Descartar los cambios realizados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2bce7-115">Discard the changes made by the user.</span></span> <br/> |
| <dl> <span data-ttu-id="2bce7-116"><dt></dt><dt> **False**</dt></span><span class="sxs-lookup"><span data-stu-id="2bce7-116"><dt></dt> <dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="2bce7-117">Acepte los cambios realizados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2bce7-117">Accept the changes made by the user.</span></span> <br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bce7-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bce7-118">Return value</span></span>

<span data-ttu-id="2bce7-119">Devuelve un entero.</span><span class="sxs-lookup"><span data-stu-id="2bce7-119">Returns an integer.</span></span> <span data-ttu-id="2bce7-120">**LRESULT** se convierte en un entero que indica **true**(1) o **false**(0).</span><span class="sxs-lookup"><span data-stu-id="2bce7-120">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bce7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bce7-121">Requirements</span></span>



| <span data-ttu-id="2bce7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bce7-122">Requirement</span></span> | <span data-ttu-id="2bce7-123">Value</span><span class="sxs-lookup"><span data-stu-id="2bce7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bce7-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bce7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2bce7-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2bce7-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2bce7-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bce7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2bce7-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2bce7-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2bce7-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bce7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bce7-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bce7-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bce7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bce7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bce7-131">**HDM \_ CLEARFILTER**</span><span class="sxs-lookup"><span data-stu-id="2bce7-131">**HDM\_CLEARFILTER**</span></span>](hdm-clearfilter.md)
</dt> </dl>

 

 





