---
title: Mensaje de TCM_REMOVEIMAGE (commctrl. h)
description: Quita una imagen de una lista de imágenes de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ RemoveImage.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- TCM_REMOVEIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbc51aa0efed847e39e735443c0d42e288bbaab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658370"
---
# <a name="tcm_removeimage-message"></a><span data-ttu-id="ec219-105">\_Mensaje REMOVEIMAGE de TCM</span><span class="sxs-lookup"><span data-stu-id="ec219-105">TCM\_REMOVEIMAGE message</span></span>

<span data-ttu-id="ec219-106">Quita una imagen de una lista de imágenes de un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="ec219-106">Removes an image from a tab control's image list.</span></span> <span data-ttu-id="ec219-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) .</span><span class="sxs-lookup"><span data-stu-id="ec219-107">You can send this message explicitly or by using the [**TabCtrl\_RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec219-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec219-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec219-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec219-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec219-110">Índice de la imagen que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="ec219-110">Index of the image to remove.</span></span>

</dd> <dt>

<span data-ttu-id="ec219-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec219-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ec219-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ec219-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec219-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec219-113">Return value</span></span>

<span data-ttu-id="ec219-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ec219-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec219-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec219-115">Remarks</span></span>

<span data-ttu-id="ec219-116">El control de pestaña actualiza el índice de la imagen de cada pestaña, por lo que cada pestaña permanece asociada a la misma imagen que antes.</span><span class="sxs-lookup"><span data-stu-id="ec219-116">The tab control updates each tab's image index, so each tab remains associated with the same image as before.</span></span> <span data-ttu-id="ec219-117">Si una pestaña usa la imagen que se va a quitar, la pestaña se establecerá en no tener ninguna imagen.</span><span class="sxs-lookup"><span data-stu-id="ec219-117">If a tab is using the image being removed, the tab will be set to have no image.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec219-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec219-118">Requirements</span></span>



| <span data-ttu-id="ec219-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec219-119">Requirement</span></span> | <span data-ttu-id="ec219-120">Value</span><span class="sxs-lookup"><span data-stu-id="ec219-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec219-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec219-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ec219-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ec219-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec219-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec219-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ec219-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec219-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec219-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec219-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec219-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec219-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





