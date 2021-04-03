---
title: Mensaje de TBM_GETBUDDY (commctrl. h)
description: Recupera el identificador de una ventana relacionada del control TrackBar en una ubicación determinada. La ubicación especificada es relativa a la orientación del control (horizontal o vertical).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- TBM_GETBUDDY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997169"
---
# <a name="tbm_getbuddy-message"></a><span data-ttu-id="91a7a-105">TBM \_ GETBUDDY</span><span class="sxs-lookup"><span data-stu-id="91a7a-105">TBM\_GETBUDDY message</span></span>

<span data-ttu-id="91a7a-106">Recupera el identificador de una ventana relacionada del control TrackBar en una ubicación determinada.</span><span class="sxs-lookup"><span data-stu-id="91a7a-106">Retrieves the handle to a trackbar control buddy window at a given location.</span></span> <span data-ttu-id="91a7a-107">La ubicación especificada es relativa a la orientación del control (horizontal o vertical).</span><span class="sxs-lookup"><span data-stu-id="91a7a-107">The specified location is relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="91a7a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91a7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91a7a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91a7a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91a7a-110">Valor que indica el identificador de ventana relacionado que se va a recuperar, por ubicación relativa.</span><span class="sxs-lookup"><span data-stu-id="91a7a-110">Value indicating which buddy window handle will be retrieved, by relative location.</span></span> <span data-ttu-id="91a7a-111">Este valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="91a7a-111">This value can be one of the following:</span></span>



| <span data-ttu-id="91a7a-112">Value</span><span class="sxs-lookup"><span data-stu-id="91a7a-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="91a7a-113">Significado</span><span class="sxs-lookup"><span data-stu-id="91a7a-113">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="91a7a-114"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="91a7a-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="91a7a-115">Recupera el identificador del Buddy situado a la izquierda de la barra de control.</span><span class="sxs-lookup"><span data-stu-id="91a7a-115">Retrieves the handle to the buddy to the left of the trackbar.</span></span> <span data-ttu-id="91a7a-116">Si el control TrackBar usa el [**estilo \_ vertical de TBS**](trackbar-control-styles.md) , el mensaje recuperará el amigo sobre la barra de control.</span><span class="sxs-lookup"><span data-stu-id="91a7a-116">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy above the trackbar.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="91a7a-117"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="91a7a-117"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="91a7a-118">Recupera el identificador del relacionado a la derecha de la barra de control.</span><span class="sxs-lookup"><span data-stu-id="91a7a-118">Retrieves the handle to the buddy to the right of the trackbar.</span></span> <span data-ttu-id="91a7a-119">Si el control TrackBar usa el [**estilo \_ vertical de TBS**](trackbar-control-styles.md) , el mensaje recuperará el amigo debajo de la barra de control.</span><span class="sxs-lookup"><span data-stu-id="91a7a-119">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy below the trackbar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="91a7a-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91a7a-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="91a7a-121">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="91a7a-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91a7a-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91a7a-122">Return value</span></span>

<span data-ttu-id="91a7a-123">Devuelve el identificador de la ventana relacionada en la ubicación especificada por *wParam*, o **null** si no existe ninguna ventana relacionada en esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="91a7a-123">Returns the handle to the buddy window at the location specified by *wParam*, or **NULL** if no buddy window exists at that location.</span></span>

## <a name="requirements"></a><span data-ttu-id="91a7a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91a7a-124">Requirements</span></span>



| <span data-ttu-id="91a7a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="91a7a-125">Requirement</span></span> | <span data-ttu-id="91a7a-126">Value</span><span class="sxs-lookup"><span data-stu-id="91a7a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91a7a-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91a7a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="91a7a-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91a7a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91a7a-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91a7a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="91a7a-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="91a7a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91a7a-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91a7a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="91a7a-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a7a-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





