---
description: Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta un contacto de entrada.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Visualización de contactos (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361237"
---
# <a name="contact-visualization"></a><span data-ttu-id="3143f-103">Visualización de contactos</span><span class="sxs-lookup"><span data-stu-id="3143f-103">Contact Visualization</span></span>

<span data-ttu-id="3143f-104">Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta un contacto de entrada.</span><span class="sxs-lookup"><span data-stu-id="3143f-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when an input contact is detected.</span></span>

<span data-ttu-id="3143f-105">Estas constantes se utilizan con los parámetros **SPI \_ GETCONTACTVISUALIZATION** y **SPI \_ SETCONTACTVISUALIZATION** y la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="3143f-105">These constants are used with the **SPI\_GETCONTACTVISUALIZATION** and **SPI\_SETCONTACTVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="3143f-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ desactivado**</span><span class="sxs-lookup"><span data-stu-id="3143f-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3143f-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="3143f-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="3143f-108">Especifica la información de la interfaz de usuario para todos los contactos está desactivada.</span><span class="sxs-lookup"><span data-stu-id="3143f-108">Specifies UI feedback for all contacts is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3143f-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_**</span><span class="sxs-lookup"><span data-stu-id="3143f-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3143f-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="3143f-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="3143f-111">Especifica la información de la interfaz de usuario para todos los contactos está activada.</span><span class="sxs-lookup"><span data-stu-id="3143f-111">Specifies UI feedback for all contacts is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3143f-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION \_ PRESENTATIONMODE**</span><span class="sxs-lookup"><span data-stu-id="3143f-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION\_PRESENTATIONMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3143f-113">0x0002</span><span class="sxs-lookup"><span data-stu-id="3143f-113">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="3143f-114">Especifica la información de la interfaz de usuario para todos los contactos está activada con los objetos visuales de modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="3143f-114">Specifies UI feedback for all contacts is on with presentation mode visuals.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3143f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3143f-115">Requirements</span></span>



| <span data-ttu-id="3143f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3143f-116">Requirement</span></span> | <span data-ttu-id="3143f-117">Value</span><span class="sxs-lookup"><span data-stu-id="3143f-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3143f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3143f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3143f-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3143f-119">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3143f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3143f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3143f-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3143f-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3143f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3143f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3143f-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="3143f-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3143f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3143f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3143f-125">Constantes de configuración</span><span class="sxs-lookup"><span data-stu-id="3143f-125">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="3143f-126">**Visualización de gestos**</span><span class="sxs-lookup"><span data-stu-id="3143f-126">**Gesture Visualization**</span></span>](gesture-visualization.md)
</dt> <dt>

[<span data-ttu-id="3143f-127">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="3143f-127">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="3143f-128">Configuración de comentarios de entrada</span><span class="sxs-lookup"><span data-stu-id="3143f-128">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

