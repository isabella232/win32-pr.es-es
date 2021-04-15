---
description: Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos del lápiz enumerados.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Visualización del lápiz (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545574"
---
# <a name="pen-visualization"></a><span data-ttu-id="38852-103">Visualización del lápiz</span><span class="sxs-lookup"><span data-stu-id="38852-103">Pen Visualization</span></span>

<span data-ttu-id="38852-104">Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos del lápiz enumerados.</span><span class="sxs-lookup"><span data-stu-id="38852-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed pen gestures is detected.</span></span>

<span data-ttu-id="38852-105">Estas constantes se utilizan con los parámetros **SPI \_ GETPENVISUALIZATION** y **SPI \_ SETPENVISUALIZATION** y la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="38852-105">These constants are used with the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="38852-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION \_ desactivado**</span><span class="sxs-lookup"><span data-stu-id="38852-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38852-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="38852-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="38852-108">Especifica que la información de la interfaz de usuario para todos los gestos de lápiz está desactivada.</span><span class="sxs-lookup"><span data-stu-id="38852-108">Specifies that UI feedback for all pen gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38852-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_**</span><span class="sxs-lookup"><span data-stu-id="38852-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38852-110">0x0023</span><span class="sxs-lookup"><span data-stu-id="38852-110">0x0023</span></span>
</dt> <dt>



<span data-ttu-id="38852-111">Especifica que la información de la interfaz de usuario para todos los gestos de lápiz está activada.</span><span class="sxs-lookup"><span data-stu-id="38852-111">Specifies that UI feedback for all pen gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38852-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION \_ TAP**</span><span class="sxs-lookup"><span data-stu-id="38852-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38852-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="38852-113">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="38852-114">Especifica la información de la interfaz de usuario para una TAP del lápiz.</span><span class="sxs-lookup"><span data-stu-id="38852-114">Specifies UI feedback for a pen tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38852-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION \_ DOUBLETAP**</span><span class="sxs-lookup"><span data-stu-id="38852-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38852-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="38852-116">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="38852-117">Especifica la información de la interfaz de usuario para una doble Punte de lápiz.</span><span class="sxs-lookup"><span data-stu-id="38852-117">Specifies UI feedback for a pen double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38852-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**\_cursor PENVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="38852-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**PENVISUALIZATION\_CURSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38852-119">0x0020</span><span class="sxs-lookup"><span data-stu-id="38852-119">0x0020</span></span>
</dt> <dt>



<span data-ttu-id="38852-120">Especifica la información de la interfaz de usuario para el cursor del lápiz.</span><span class="sxs-lookup"><span data-stu-id="38852-120">Specifies UI feedback for the pen cursor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38852-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38852-121">Requirements</span></span>



| <span data-ttu-id="38852-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="38852-122">Requirement</span></span> | <span data-ttu-id="38852-123">Value</span><span class="sxs-lookup"><span data-stu-id="38852-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="38852-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38852-124">Minimum supported client</span></span><br/> | <span data-ttu-id="38852-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="38852-125">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="38852-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38852-126">Minimum supported server</span></span><br/> | <span data-ttu-id="38852-127">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="38852-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="38852-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38852-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="38852-129"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="38852-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38852-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="38852-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38852-131">Constantes de configuración</span><span class="sxs-lookup"><span data-stu-id="38852-131">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="38852-132">**Visualización de contactos**</span><span class="sxs-lookup"><span data-stu-id="38852-132">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="38852-133">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="38852-133">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="38852-134">Configuración de comentarios de entrada</span><span class="sxs-lookup"><span data-stu-id="38852-134">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

