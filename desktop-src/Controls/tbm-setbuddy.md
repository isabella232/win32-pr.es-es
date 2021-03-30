---
title: Mensaje de TBM_SETBUDDY (commctrl. h)
description: Asigna una ventana como la ventana relacionada para un control TrackBar. Las ventanas de amigos de la barra de desplazamiento se muestran automáticamente en una ubicación relativa a la orientación del control (horizontal o vertical).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- TBM_SETBUDDY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33e53117933390d7a34ec75a49724003255108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079072"
---
# <a name="tbm_setbuddy-message"></a><span data-ttu-id="f2c3a-105">TBM \_ SETBUDDY</span><span class="sxs-lookup"><span data-stu-id="f2c3a-105">TBM\_SETBUDDY message</span></span>

<span data-ttu-id="f2c3a-106">Asigna una ventana como la ventana relacionada para un control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-106">Assigns a window as the buddy window for a trackbar control.</span></span> <span data-ttu-id="f2c3a-107">Las ventanas de amigos de la barra de desplazamiento se muestran automáticamente en una ubicación relativa a la orientación del control (horizontal o vertical).</span><span class="sxs-lookup"><span data-stu-id="f2c3a-107">Trackbar buddy windows are automatically displayed in a location relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="f2c3a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2c3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2c3a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2c3a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c3a-110">Valor que especifica la ubicación en la que se va a mostrar la ventana relacionada.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-110">Value specifying the location at which to display the buddy window.</span></span> <span data-ttu-id="f2c3a-111">Este valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2c3a-111">This value can be one of the following:</span></span>



| <span data-ttu-id="f2c3a-112">Value</span><span class="sxs-lookup"><span data-stu-id="f2c3a-112">Value</span></span>                                                                                                                                | <span data-ttu-id="f2c3a-113">Significado</span><span class="sxs-lookup"><span data-stu-id="f2c3a-113">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="f2c3a-114"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c3a-114"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="f2c3a-115">El amigo aparecerá a la izquierda del control TrackBar si el control TrackBar usa el estilo [**TBS \_ horizontal**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f2c3a-115">The buddy will appear to the left of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="f2c3a-116">Si la barra de mandos usa el estilo [**\_ vertical de TBS**](trackbar-control-styles.md) , el amigo aparece sobre el control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-116">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears above the trackbar control.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="f2c3a-117"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c3a-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="f2c3a-118">El amigo aparecerá a la derecha del control TrackBar si el control TrackBar usa el estilo [**TBS \_ horizontal**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f2c3a-118">The buddy will appear to the right of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="f2c3a-119">Si la barra de mandos usa el estilo [**\_ vertical de TBS**](trackbar-control-styles.md) , el amigo aparece debajo del control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-119">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears below the trackbar control.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f2c3a-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2c3a-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c3a-121">Identificador de la ventana que se establecerá como el Buddy del control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-121">Handle to the window that will be set as the trackbar control's buddy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2c3a-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2c3a-122">Return value</span></span>

<span data-ttu-id="f2c3a-123">Devuelve el identificador de la ventana que se asignó previamente al control en esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-123">Returns the handle to the window that was previously assigned to the control at that location.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2c3a-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2c3a-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f2c3a-125">Los controles de barra de seguimiento admiten hasta dos ventanas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-125">Trackbar controls support up to two buddy windows.</span></span> <span data-ttu-id="f2c3a-126">Esto puede ser útil cuando se debe mostrar texto o imágenes en cada extremo del control.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-126">This can be useful when you must display text or images at each end of the control.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2c3a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2c3a-127">Requirements</span></span>



| <span data-ttu-id="f2c3a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2c3a-128">Requirement</span></span> | <span data-ttu-id="f2c3a-129">Value</span><span class="sxs-lookup"><span data-stu-id="f2c3a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c3a-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2c3a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f2c3a-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f2c3a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2c3a-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2c3a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f2c3a-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2c3a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2c3a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2c3a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2c3a-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2c3a-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





