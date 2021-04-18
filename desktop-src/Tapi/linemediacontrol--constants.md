---
description: Las \_ constantes de marcador de bits LINEMEDIACONTROL describen un conjunto de operaciones genéricas en flujos multimedia.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: Constantes de LINEMEDIACONTROL_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3241a3b5f4f8a0363f30ce7aefaded0c63fc4189
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690698"
---
# <a name="linemediacontrol_-constants"></a><span data-ttu-id="a3db7-103">Constantes de LINEMEDIACONTROL \_</span><span class="sxs-lookup"><span data-stu-id="a3db7-103">LINEMEDIACONTROL\_ Constants</span></span>

<span data-ttu-id="a3db7-104">Las constantes de marcador de bits **LINEMEDIACONTROL \_** describen un conjunto de operaciones genéricas en flujos multimedia.</span><span class="sxs-lookup"><span data-stu-id="a3db7-104">The **LINEMEDIACONTROL\_** bit-flag constants describe a set of generic operations on media streams.</span></span> <span data-ttu-id="a3db7-105">La secuencia de medios determina las interpretaciones.</span><span class="sxs-lookup"><span data-stu-id="a3db7-105">The interpretations are determined by the media stream.</span></span> <span data-ttu-id="a3db7-106">El dispositivo de línea debe tener la capacidad de control de medios para que cualquier operación de control de medios sea efectiva.</span><span class="sxs-lookup"><span data-stu-id="a3db7-106">The line device must have the media-control capability for any media-control operation to be effective.</span></span>

<dl> <dt>

<span data-ttu-id="a3db7-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="a3db7-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3db7-108">No se realiza ningún cambio en el flujo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a3db7-108">No change is to be made to the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3db7-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**pausar LINEMEDIACONTROL \_**</span><span class="sxs-lookup"><span data-stu-id="a3db7-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL\_PAUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3db7-110">Detenga temporalmente el flujo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a3db7-110">Temporarily pause the media stream.</span></span>

<span data-ttu-id="a3db7-111">La velocidad del flujo multimedia se devuelve a la normalidad.</span><span class="sxs-lookup"><span data-stu-id="a3db7-111">The speed of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3db7-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL \_ RATEDOWN**</span><span class="sxs-lookup"><span data-stu-id="a3db7-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL\_RATEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3db7-113">La velocidad de la secuencia de medios disminuye en función de la cantidad definida por el flujo.</span><span class="sxs-lookup"><span data-stu-id="a3db7-113">The speed of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3db7-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL \_ RATENORMAL**</span><span class="sxs-lookup"><span data-stu-id="a3db7-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL\_RATENORMAL**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3db7-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL \_ RATEUP**</span><span class="sxs-lookup"><span data-stu-id="a3db7-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL\_RATEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3db7-116">La velocidad de la secuencia de medios aumenta en función de la cantidad definida por el flujo.</span><span class="sxs-lookup"><span data-stu-id="a3db7-116">The speed of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3db7-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**restablecimiento de LINEMEDIACONTROL \_**</span><span class="sxs-lookup"><span data-stu-id="a3db7-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**LINEMEDIACONTROL\_RESET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3db7-118">Restablezca el flujo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a3db7-118">Reset the media stream.</span></span> <span data-ttu-id="a3db7-119">Equivalente a un final de entrada.</span><span class="sxs-lookup"><span data-stu-id="a3db7-119">Equivalent to an end-of-input.</span></span> <span data-ttu-id="a3db7-120">Se liberan todos los búferes.</span><span class="sxs-lookup"><span data-stu-id="a3db7-120">All buffers are released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3db7-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**\_reanudación de LINEMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="a3db7-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3db7-122">Reanudar una secuencia de medios en pausa.</span><span class="sxs-lookup"><span data-stu-id="a3db7-122">Resume a paused media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3db7-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**Inicio de LINEMEDIACONTROL \_**</span><span class="sxs-lookup"><span data-stu-id="a3db7-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3db7-124">Inicie el flujo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a3db7-124">Start the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3db7-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL \_ VOLUMEDOWN**</span><span class="sxs-lookup"><span data-stu-id="a3db7-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL\_VOLUMEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3db7-126">La amplitud de la secuencia multimedia disminuye en función de la cantidad definida por el flujo.</span><span class="sxs-lookup"><span data-stu-id="a3db7-126">The amplitude of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3db7-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL \_ VOLUMENORMAL**</span><span class="sxs-lookup"><span data-stu-id="a3db7-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL\_VOLUMENORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3db7-128">La amplitud del flujo multimedia se devuelve a normal.</span><span class="sxs-lookup"><span data-stu-id="a3db7-128">The amplitude of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3db7-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL \_ VOLUMEUP**</span><span class="sxs-lookup"><span data-stu-id="a3db7-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL\_VOLUMEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3db7-130">La amplitud de la secuencia de medios aumenta en función de la cantidad definida por el flujo.</span><span class="sxs-lookup"><span data-stu-id="a3db7-130">The amplitude of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3db7-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3db7-131">Remarks</span></span>

<span data-ttu-id="a3db7-132">Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3db7-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="a3db7-133">Los 16 bits de orden inferior están reservados.</span><span class="sxs-lookup"><span data-stu-id="a3db7-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="a3db7-134">El control multimedia se proporciona para mejorar el rendimiento de las acciones en flujos multimedia en respuesta a eventos relacionados con la telefonía.</span><span class="sxs-lookup"><span data-stu-id="a3db7-134">Media control is provided to improve performance of actions on media streams in response to telephony-related events.</span></span> <span data-ttu-id="a3db7-135">Normalmente, la aplicación debe administrar un flujo de medios a través de la API específica del medio.</span><span class="sxs-lookup"><span data-stu-id="a3db7-135">The application should normally manage a media stream through the media-specific API.</span></span> <span data-ttu-id="a3db7-136">La funcionalidad de control de medios que se proporciona aquí no está pensada para reemplazar las API multimedia nativas.</span><span class="sxs-lookup"><span data-stu-id="a3db7-136">The media-control functionality provided here is not intended to replace the native media APIs.</span></span>

<span data-ttu-id="a3db7-137">Las acciones de control de medios pueden asociarse con la detección de dígitos, la detección de tonos, la transición a un estado de llamada y la detección de un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a3db7-137">Media-control actions can be associated with the detection of digits, the detection of tones, the transition into a call state, and the detection of a media type.</span></span> <span data-ttu-id="a3db7-138">Consulte las funciones de los dispositivos de una línea para determinar si el control multimedia está disponible en la línea.</span><span class="sxs-lookup"><span data-stu-id="a3db7-138">Consult a line's device capabilities to determine whether media control is available on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3db7-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3db7-139">Requirements</span></span>



| <span data-ttu-id="a3db7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3db7-140">Requirement</span></span> | <span data-ttu-id="a3db7-141">Value</span><span class="sxs-lookup"><span data-stu-id="a3db7-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a3db7-142">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a3db7-142">TAPI version</span></span><br/> | <span data-ttu-id="a3db7-143">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a3db7-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a3db7-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3db7-144">Header</span></span><br/>       | <dl> <span data-ttu-id="a3db7-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3db7-145"><dt>Tapi.h</dt></span></span> </dl> |



 

 




