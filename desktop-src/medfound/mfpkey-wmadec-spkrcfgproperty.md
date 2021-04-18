---
description: Especifica la configuración de los altavoces en el equipo cliente.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: Propiedad MFPKEY_WMADEC_SPKRCFG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544782"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a><span data-ttu-id="92f71-103">\_ \_ Propiedad SPKRCFG de MFPKEY WMADEC</span><span class="sxs-lookup"><span data-stu-id="92f71-103">MFPKEY\_WMADEC\_SPKRCFG Property</span></span>

<span data-ttu-id="92f71-104">Especifica la configuración de los altavoces en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="92f71-104">Specifies the speaker configuration on the client computer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="92f71-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="92f71-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="92f71-106">g \_ wszWMACSpeakerConfig</span><span class="sxs-lookup"><span data-stu-id="92f71-106">g\_wszWMACSpeakerConfig</span></span>

## <a name="data-type"></a><span data-ttu-id="92f71-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="92f71-107">Data Type</span></span>

<span data-ttu-id="92f71-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="92f71-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="92f71-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="92f71-109">Default Value</span></span>

<span data-ttu-id="92f71-110">No se presupone ninguna configuración específica del orador.</span><span class="sxs-lookup"><span data-stu-id="92f71-110">No specific speaker configuration is assumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="92f71-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92f71-111">Remarks</span></span>

<span data-ttu-id="92f71-112">Debe establecer este valor en una de las constantes o valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="92f71-112">You should set this value to one of the constants or values in the following table.</span></span> <span data-ttu-id="92f71-113">Las constantes se definen en Microsoft DirectSound y se enumeran aquí para mayor comodidad.</span><span class="sxs-lookup"><span data-stu-id="92f71-113">The constants are defined in Microsoft DirectSound, and are listed here for convenience.</span></span> <span data-ttu-id="92f71-114">Para resolver estos nombres de constantes para el compilador, debe incluir dsound. h.</span><span class="sxs-lookup"><span data-stu-id="92f71-114">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="92f71-115">Constante</span><span class="sxs-lookup"><span data-stu-id="92f71-115">Constant</span></span>             | <span data-ttu-id="92f71-116">Value</span><span class="sxs-lookup"><span data-stu-id="92f71-116">Value</span></span>      | <span data-ttu-id="92f71-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="92f71-117">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="92f71-118">DSSPEAKER \_ DIRECTOUT</span><span class="sxs-lookup"><span data-stu-id="92f71-118">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="92f71-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92f71-119">0x00000000</span></span> | <span data-ttu-id="92f71-120">El audio se pasa directamente, sin tener que configurarse para los altavoces.</span><span class="sxs-lookup"><span data-stu-id="92f71-120">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="92f71-121">\_auriculares DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="92f71-121">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="92f71-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="92f71-122">0x00000001</span></span> | <span data-ttu-id="92f71-123">El equipo cliente está equipado con auriculares.</span><span class="sxs-lookup"><span data-stu-id="92f71-123">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="92f71-124">\_mono DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="92f71-124">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="92f71-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="92f71-125">0x00000002</span></span> | <span data-ttu-id="92f71-126">El equipo cliente está equipado con un orador monoaural.</span><span class="sxs-lookup"><span data-stu-id="92f71-126">The client computer is equipped with a monoaural speaker.</span></span>                    |
| <span data-ttu-id="92f71-127">DSSPEAKER \_ cuádruple</span><span class="sxs-lookup"><span data-stu-id="92f71-127">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="92f71-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="92f71-128">0x00000003</span></span> | <span data-ttu-id="92f71-129">El equipo cliente está equipado con altavoces quadraphonic.</span><span class="sxs-lookup"><span data-stu-id="92f71-129">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="92f71-130">\_estéreo DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="92f71-130">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="92f71-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="92f71-131">0x00000004</span></span> | <span data-ttu-id="92f71-132">El equipo cliente está equipado con altavoces estéreo.</span><span class="sxs-lookup"><span data-stu-id="92f71-132">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="92f71-133">\_envolvente DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="92f71-133">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="92f71-134">0x00000005</span><span class="sxs-lookup"><span data-stu-id="92f71-134">0x00000005</span></span> | <span data-ttu-id="92f71-135">El equipo cliente está equipado con altavoces con sonido envolvente de cuatro canales.</span><span class="sxs-lookup"><span data-stu-id="92f71-135">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="92f71-136">DSSPEAKER \_ 5POINT1</span><span class="sxs-lookup"><span data-stu-id="92f71-136">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="92f71-137">0x00000006</span><span class="sxs-lookup"><span data-stu-id="92f71-137">0x00000006</span></span> | <span data-ttu-id="92f71-138">El equipo cliente está equipado con cinco altavoces y un subwoofer.</span><span class="sxs-lookup"><span data-stu-id="92f71-138">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="92f71-139">DSSPEAKER \_ 7POINT1</span><span class="sxs-lookup"><span data-stu-id="92f71-139">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="92f71-140">0x00000007</span><span class="sxs-lookup"><span data-stu-id="92f71-140">0x00000007</span></span> | <span data-ttu-id="92f71-141">El equipo cliente está equipado con siete altavoces y un subwoofer.</span><span class="sxs-lookup"><span data-stu-id="92f71-141">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="92f71-142">El valor establecido para esta propiedad determina los formatos de salida enumerados por el códec para el audio multicanal.</span><span class="sxs-lookup"><span data-stu-id="92f71-142">The value set for this property determines the output formats enumerated by the codec for multichannel audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="92f71-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92f71-143">Requirements</span></span>



| <span data-ttu-id="92f71-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="92f71-144">Requirement</span></span> | <span data-ttu-id="92f71-145">Value</span><span class="sxs-lookup"><span data-stu-id="92f71-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92f71-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92f71-146">Minimum supported client</span></span><br/> | <span data-ttu-id="92f71-147">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="92f71-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="92f71-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92f71-148">Minimum supported server</span></span><br/> | <span data-ttu-id="92f71-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="92f71-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="92f71-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92f71-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="92f71-151"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="92f71-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92f71-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="92f71-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92f71-153">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92f71-153">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




