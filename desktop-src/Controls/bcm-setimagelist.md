---
title: Mensaje de BCM_SETIMAGELIST (commctrl. h)
description: Asigna una lista de imágenes a un control de botón. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button SetImageList.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- BCM_SETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079274"
---
# <a name="bcm_setimagelist-message"></a><span data-ttu-id="5df2f-105">\_Mensaje SETIMAGELIST de BCM</span><span class="sxs-lookup"><span data-stu-id="5df2f-105">BCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="5df2f-106">Asigna una lista de imágenes a un control de botón.</span><span class="sxs-lookup"><span data-stu-id="5df2f-106">Assigns an image list to a button control.</span></span> <span data-ttu-id="5df2f-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="5df2f-107">You can send this message explicitly or use the [**Button\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5df2f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5df2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5df2f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5df2f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5df2f-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5df2f-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5df2f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5df2f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5df2f-112">Puntero a una estructura [**de \_ ImageList de botón**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que contiene información de la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="5df2f-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5df2f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5df2f-113">Return value</span></span>

<span data-ttu-id="5df2f-114">Si el mensaje se realiza correctamente, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="5df2f-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="5df2f-115">En caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="5df2f-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5df2f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5df2f-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5df2f-117">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="5df2f-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5df2f-118">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5df2f-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="5df2f-119">La lista de imágenes a la que se hace referencia en el miembro **himl** de la estructura [**\_ ImageList del botón**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) debe contener una sola imagen que se usará para todos los Estados o imágenes individuales para cada Estado.</span><span class="sxs-lookup"><span data-stu-id="5df2f-119">The image list referred to in the **himl** member of the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure should contain either a single image to be used for all states or individual images for each state.</span></span> <span data-ttu-id="5df2f-120">Los siguientes Estados se definen en vssym32. h.</span><span class="sxs-lookup"><span data-stu-id="5df2f-120">The following states are defined in vssym32.h.</span></span>

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

<span data-ttu-id="5df2f-121">Tenga en cuenta que PBS \_ STYLUSHOT se usa solo en Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="5df2f-121">Note that PBS\_STYLUSHOT is used only on tablet computers.</span></span>

<span data-ttu-id="5df2f-122">Cada valor es un índice de la imagen correspondiente en la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="5df2f-122">Each value is an index to the appropriate image in the image list.</span></span> <span data-ttu-id="5df2f-123">Si solo hay una imagen, se utiliza para todos los Estados.</span><span class="sxs-lookup"><span data-stu-id="5df2f-123">If only one image is present, it is used for all states.</span></span> <span data-ttu-id="5df2f-124">Si la lista de imágenes contiene más de una imagen, cada índice corresponde a un estado del botón.</span><span class="sxs-lookup"><span data-stu-id="5df2f-124">If the image list contains more than one image, each index corresponds to one state of the button.</span></span> <span data-ttu-id="5df2f-125">Si no se proporciona una imagen para cada Estado, no se dibuja nada para esos Estados sin imágenes.</span><span class="sxs-lookup"><span data-stu-id="5df2f-125">If an image is not provided for each state, nothing is drawn for those states without images.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df2f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5df2f-126">Requirements</span></span>



| <span data-ttu-id="5df2f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5df2f-127">Requirement</span></span> | <span data-ttu-id="5df2f-128">Value</span><span class="sxs-lookup"><span data-stu-id="5df2f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5df2f-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5df2f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5df2f-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5df2f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5df2f-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5df2f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5df2f-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5df2f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5df2f-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5df2f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5df2f-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5df2f-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





