---
title: Mensaje de BCM_GETIDEALSIZE (commctrl. h)
description: Obtiene el tamaño del botón que mejor se adapta a su texto e imagen, si hay una lista de imágenes. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button GetIdealSize.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- BCM_GETIDEALSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656535"
---
# <a name="bcm_getidealsize-message"></a><span data-ttu-id="2ec5e-105">\_Mensaje GETIDEALSIZE de BCM</span><span class="sxs-lookup"><span data-stu-id="2ec5e-105">BCM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="2ec5e-106">Obtiene el tamaño del botón que mejor se adapta a su texto e imagen, si hay una lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-106">Gets the size of the button that best fits its text and image, if an image list is present.</span></span> <span data-ttu-id="2ec5e-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) .</span><span class="sxs-lookup"><span data-stu-id="2ec5e-107">You can send this message explicitly or use the [**Button\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ec5e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ec5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ec5e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ec5e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ec5e-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2ec5e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ec5e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ec5e-112">Puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) que recibe el tamaño deseado del botón, incluida la lista de texto e imagen, si está presente.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-112">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the desired size of the button, including text and image list, if present.</span></span> <span data-ttu-id="2ec5e-113">La aplicación que realiza la llamada es responsable de la asignación de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="2ec5e-114">Establezca los miembros **CX** y **CY** en cero para que el alto y el ancho idóneos se devuelvan en la estructura de **tamaño** .</span><span class="sxs-lookup"><span data-stu-id="2ec5e-114">Set the **cx** and **cy** members to zero to have the ideal height and width returned in the **SIZE** structure.</span></span> <span data-ttu-id="2ec5e-115">Para especificar un ancho de botón, establezca el miembro de **CX** en el ancho del botón deseado.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-115">To specify a button width, set the **cx** member to the desired button width.</span></span> <span data-ttu-id="2ec5e-116">El sistema calculará el alto ideal para este ancho y lo devolverá en el miembro **CY** .</span><span class="sxs-lookup"><span data-stu-id="2ec5e-116">The system will calculate the ideal height for this width and return it in the **cy** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ec5e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ec5e-117">Return value</span></span>

<span data-ttu-id="2ec5e-118">Si el mensaje se realiza correctamente, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-118">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="2ec5e-119">En caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-119">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ec5e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ec5e-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2ec5e-121">Si no se desea ningún ancho de botón especial, debe establecer ambos miembros de [**tamaño**](/previous-versions//dd145106(v=vs.85)) en cero para calcular y devolver el alto y ancho ideales.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-121">If no special button width is desired, then you must set both members of [**SIZE**](/previous-versions//dd145106(v=vs.85)) to zero to calculate and return the ideal height and width.</span></span> <span data-ttu-id="2ec5e-122">Si el valor del miembro **CX** es mayor que cero, este valor se considera el ancho del botón deseado y se calcula el alto ideal para este ancho y se devuelve en el miembro **CY** .</span><span class="sxs-lookup"><span data-stu-id="2ec5e-122">If the value of the **cx** member is greater than zero, then this value is considered the desired button width, and the ideal height for this width is calculated and returned in the **cy** member.</span></span>

 

<span data-ttu-id="2ec5e-123">Este mensaje es más aplicable a los pulsadores.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-123">This message is most applicable to PushButtons.</span></span> <span data-ttu-id="2ec5e-124">Cuando se envía a un botón de pulsación, el mensaje recupera el rectángulo delimitador necesario para mostrar el texto del botón.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-124">When sent to a PushButton, the message retrieves the bounding rectangle required to display the button's text.</span></span> <span data-ttu-id="2ec5e-125">Además, si el botón de botón tiene una lista de imágenes, también se ajusta el tamaño del rectángulo delimitador para incluir la imagen del botón.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-125">Additionally, if the PushButton has an image list, the bounding rectangle is also sized to include the button's image.</span></span>

<span data-ttu-id="2ec5e-126">Cuando se envía a un botón de cualquier otro tipo, se recupera el tamaño del rectángulo de ventana del control.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-126">When sent to a button of any other type, the size of the control's window rectangle is retrieved.</span></span>

> [!Note]  
> <span data-ttu-id="2ec5e-127">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-127">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2ec5e-128">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2ec5e-128">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2ec5e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ec5e-129">Requirements</span></span>



| <span data-ttu-id="2ec5e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ec5e-130">Requirement</span></span> | <span data-ttu-id="2ec5e-131">Value</span><span class="sxs-lookup"><span data-stu-id="2ec5e-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ec5e-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ec5e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2ec5e-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2ec5e-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ec5e-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ec5e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2ec5e-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ec5e-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ec5e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ec5e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ec5e-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ec5e-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

