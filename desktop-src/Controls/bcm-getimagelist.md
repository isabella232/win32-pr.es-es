---
title: Mensaje de BCM_GETIMAGELIST (commctrl. h)
description: Obtiene la estructura del botón \_ ImageList que describe la lista de imágenes asignada a un control de botón. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button GetImageList.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- BCM_GETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490888"
---
# <a name="bcm_getimagelist-message"></a><span data-ttu-id="5f21f-105">\_Mensaje GETIMAGELIST de BCM</span><span class="sxs-lookup"><span data-stu-id="5f21f-105">BCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="5f21f-106">Obtiene la estructura del [**botón \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que describe la lista de imágenes asignada a un control de botón.</span><span class="sxs-lookup"><span data-stu-id="5f21f-106">Gets the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that describes the image list assigned to a button control.</span></span> <span data-ttu-id="5f21f-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="5f21f-107">You can send this message explicitly or use the [**Button\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f21f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f21f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f21f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f21f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f21f-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f21f-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5f21f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f21f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f21f-112">Puntero a una estructura [**de \_ ImageList de botón**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que contiene información de la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="5f21f-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f21f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f21f-113">Return value</span></span>

<span data-ttu-id="5f21f-114">Si el mensaje se realiza correctamente, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="5f21f-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="5f21f-115">En caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="5f21f-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f21f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f21f-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5f21f-117">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="5f21f-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5f21f-118">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5f21f-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f21f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f21f-119">Requirements</span></span>



| <span data-ttu-id="5f21f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f21f-120">Requirement</span></span> | <span data-ttu-id="5f21f-121">Value</span><span class="sxs-lookup"><span data-stu-id="5f21f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f21f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f21f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5f21f-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5f21f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f21f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f21f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5f21f-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f21f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f21f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f21f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f21f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f21f-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





