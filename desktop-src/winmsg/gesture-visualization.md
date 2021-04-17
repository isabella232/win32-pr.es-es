---
description: Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos de la lista.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Visualización de gestos (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697601"
---
# <a name="gesture-visualization"></a><span data-ttu-id="2eec6-103">Visualización de gestos</span><span class="sxs-lookup"><span data-stu-id="2eec6-103">Gesture Visualization</span></span>

<span data-ttu-id="2eec6-104">Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos de la lista.</span><span class="sxs-lookup"><span data-stu-id="2eec6-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed gestures is detected.</span></span>

<span data-ttu-id="2eec6-105">Estas constantes se utilizan con los parámetros **SPI \_ GETGESTUREVISUALIZATION** y **SPI \_ SETGESTUREVISUALIZATION** y la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="2eec6-105">These constants are used with the **SPI\_GETGESTUREVISUALIZATION** and **SPI\_SETGESTUREVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="2eec6-106">**Note**</span><span class="sxs-lookup"><span data-stu-id="2eec6-106">**Note**</span></span>  

<span data-ttu-id="2eec6-107">Para recuperar o establecer la información de visualización del lápiz, se recomienda usar los parámetros **SPI \_ GETPENVISUALIZATION** y **SPI \_ SETPENVISUALIZATION** y las constantes enumeradas en la [**visualización del lápiz**](pen-visualization.md).</span><span class="sxs-lookup"><span data-stu-id="2eec6-107">For retrieving or setting pen visualization info, we recommend that you use the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the constants listed in [**Pen Visualization**](pen-visualization.md).</span></span>

<dl> <dt>

<span data-ttu-id="2eec6-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ desactivado**</span><span class="sxs-lookup"><span data-stu-id="2eec6-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eec6-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="2eec6-109">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="2eec6-110">Especifica que los comentarios de la interfaz de usuario para todos los gestos están desactivados.</span><span class="sxs-lookup"><span data-stu-id="2eec6-110">Specifies that UI feedback for all gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2eec6-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_**</span><span class="sxs-lookup"><span data-stu-id="2eec6-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eec6-112">0x001F</span><span class="sxs-lookup"><span data-stu-id="2eec6-112">0x001F</span></span>
</dt> <dt>



<span data-ttu-id="2eec6-113">Especifica que la información de la interfaz de usuario para todos los gestos está activada.</span><span class="sxs-lookup"><span data-stu-id="2eec6-113">Specifies that UI feedback for all gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2eec6-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION \_ TAP**</span><span class="sxs-lookup"><span data-stu-id="2eec6-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eec6-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="2eec6-115">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="2eec6-116">Especifica la información de la interfaz de usuario para una derivación.</span><span class="sxs-lookup"><span data-stu-id="2eec6-116">Specifies UI feedback for a tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2eec6-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION \_ DOUBLETAP**</span><span class="sxs-lookup"><span data-stu-id="2eec6-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eec6-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="2eec6-118">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="2eec6-119">Especifica la información de la interfaz de usuario para una doble punteo.</span><span class="sxs-lookup"><span data-stu-id="2eec6-119">Specifies UI feedback for a double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2eec6-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="2eec6-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION\_PRESSANDTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eec6-121">0x0004</span><span class="sxs-lookup"><span data-stu-id="2eec6-121">0x0004</span></span>
</dt> <dt>



<span data-ttu-id="2eec6-122">Especifica la información de la interfaz de usuario para presionar y pulsar.</span><span class="sxs-lookup"><span data-stu-id="2eec6-122">Specifies UI feedback for a press and tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2eec6-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION \_ PRESSANDHOLD**</span><span class="sxs-lookup"><span data-stu-id="2eec6-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION\_PRESSANDHOLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eec6-124">0x0008</span><span class="sxs-lookup"><span data-stu-id="2eec6-124">0x0008</span></span>
</dt> <dt>



<span data-ttu-id="2eec6-125">Especifica la información de la interfaz de usuario para mantener presionado.</span><span class="sxs-lookup"><span data-stu-id="2eec6-125">Specifies UI feedback for a press and hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2eec6-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION \_ RIGHTTAP**</span><span class="sxs-lookup"><span data-stu-id="2eec6-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION\_RIGHTTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eec6-127">0x0010</span><span class="sxs-lookup"><span data-stu-id="2eec6-127">0x0010</span></span>
</dt> <dt>



<span data-ttu-id="2eec6-128">Especifica la información de la interfaz de usuario para una derivación derecha.</span><span class="sxs-lookup"><span data-stu-id="2eec6-128">Specifies UI feedback for a right tap.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2eec6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eec6-129">Requirements</span></span>



| <span data-ttu-id="2eec6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eec6-130">Requirement</span></span> | <span data-ttu-id="2eec6-131">Value</span><span class="sxs-lookup"><span data-stu-id="2eec6-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2eec6-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eec6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2eec6-133">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2eec6-133">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2eec6-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eec6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2eec6-135">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2eec6-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2eec6-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2eec6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eec6-137"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eec6-137"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eec6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2eec6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eec6-139">Constantes de configuración</span><span class="sxs-lookup"><span data-stu-id="2eec6-139">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="2eec6-140">**Visualización de contactos**</span><span class="sxs-lookup"><span data-stu-id="2eec6-140">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="2eec6-141">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="2eec6-141">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="2eec6-142">Configuración de comentarios de entrada</span><span class="sxs-lookup"><span data-stu-id="2eec6-142">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

