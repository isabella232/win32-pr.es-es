---
description: Las \_ constantes de marcador de bits LINEBEARERMODE describen diferentes modos de portador de una llamada.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: Constantes de LINEBEARERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690968"
---
# <a name="linebearermode_-constants"></a><span data-ttu-id="f8e57-103">Constantes de LINEBEARERMODE \_</span><span class="sxs-lookup"><span data-stu-id="f8e57-103">LINEBEARERMODE\_ Constants</span></span>

<span data-ttu-id="f8e57-104">Las constantes de marcador de bits **LINEBEARERMODE \_** describen diferentes modos de portador de una llamada.</span><span class="sxs-lookup"><span data-stu-id="f8e57-104">The **LINEBEARERMODE\_** bit-flag constants describe different bearer modes of a call.</span></span> <span data-ttu-id="f8e57-105">Cuando una aplicación realiza una llamada, puede solicitar un modo de portador específico.</span><span class="sxs-lookup"><span data-stu-id="f8e57-105">When an application makes a call, it can request a specific bearer mode.</span></span> <span data-ttu-id="f8e57-106">Estos modos se usan para seleccionar una calidad de servicio determinada para la conexión solicitada desde la red telefónica subyacente.</span><span class="sxs-lookup"><span data-stu-id="f8e57-106">These modes are used to select a certain quality of service for the requested connection from the underlying telephone network.</span></span> <span data-ttu-id="f8e57-107">Los modos de portador disponibles en una línea determinada son la capacidad del dispositivo de la línea.</span><span class="sxs-lookup"><span data-stu-id="f8e57-107">Bearer modes available on a given line are a device capability of the line.</span></span>

<dl> <dt>

<span data-ttu-id="f8e57-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**</span><span class="sxs-lookup"><span data-stu-id="f8e57-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE\_ALTSPEECHDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e57-109">La transferencia alternativa de voz o datos sin restricciones en la misma llamada (ISDN).</span><span class="sxs-lookup"><span data-stu-id="f8e57-109">The alternate transfer of speech or unrestricted data on the same call (ISDN).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e57-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**datos de LINEBEARERMODE \_**</span><span class="sxs-lookup"><span data-stu-id="f8e57-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**LINEBEARERMODE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e57-111">La transferencia de datos sin restricciones en la llamada.</span><span class="sxs-lookup"><span data-stu-id="f8e57-111">The unrestricted data transfer on the call.</span></span> <span data-ttu-id="f8e57-112">La velocidad de datos se especifica por separado.</span><span class="sxs-lookup"><span data-stu-id="f8e57-112">The data rate is specified separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e57-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ multiuso**</span><span class="sxs-lookup"><span data-stu-id="f8e57-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE\_MULTIUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e57-114">Modo multiuso definido por ISDN.</span><span class="sxs-lookup"><span data-stu-id="f8e57-114">The multiuse mode defined by ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e57-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**</span><span class="sxs-lookup"><span data-stu-id="f8e57-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE\_NONCALLSIGNALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e57-116">Esto corresponde a una conexión de señalización no asociada a la llamada desde la aplicación al proveedor o el conmutador de servicio (tratado como una secuencia de medios por TAPI).</span><span class="sxs-lookup"><span data-stu-id="f8e57-116">This corresponds to a non-call-associated signaling connection from the application to the service provider or switch (treated as a media stream by TAPI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e57-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**acceso \_ directo de LINEBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="f8e57-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE\_PASSTHROUGH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e57-118">Cuando una llamada está activa en LINEBEARERMODE \_ PASSTHROUGH, el proveedor de servicios proporciona acceso directo al hardware asociado para que la aplicación lo controle.</span><span class="sxs-lookup"><span data-stu-id="f8e57-118">When a call is active in LINEBEARERMODE\_PASSTHROUGH, the service provider gives direct access to the attached hardware for control by the application.</span></span> <span data-ttu-id="f8e57-119">Este modo lo usan principalmente las aplicaciones que quieren un control directo temporal sobre los módems asincrónicos, a los que se accede a través de las [funciones de comunicaciones](/windows/desktop/DevIO/communications-functions)con el fin de configurar o usar características especiales que no admite el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="f8e57-119">This mode is used primarily by applications desiring temporary direct control over asynchronous modems, accessed through the [communications functions](/windows/desktop/DevIO/communications-functions), for the purpose of configuring or using special features not otherwise supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e57-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**</span><span class="sxs-lookup"><span data-stu-id="f8e57-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE\_RESTRICTEDDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e57-121">Servicio de portador para datos digitales en los que solo los siete bits de orden inferior de cada octeto pueden contener datos de usuario (por ejemplo, para el servicio 56Kbit/s conmutado).</span><span class="sxs-lookup"><span data-stu-id="f8e57-121">Bearer service for digital data in which only the low-order seven bits of each octet may contain user data (for example, for Switched 56kbit/s service).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e57-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE \_ Speech**</span><span class="sxs-lookup"><span data-stu-id="f8e57-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE\_SPEECH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e57-123">Esto corresponde a la transmisión de voz G. 711 en la llamada.</span><span class="sxs-lookup"><span data-stu-id="f8e57-123">This corresponds to G.711 speech transmission on the call.</span></span> <span data-ttu-id="f8e57-124">La red puede usar técnicas de procesamiento como la transmisión analógica, la cancelación de eco y la compresión/descompresión.</span><span class="sxs-lookup"><span data-stu-id="f8e57-124">The network can use processing techniques such as analog transmission, echo cancellation, and compression/decompression.</span></span> <span data-ttu-id="f8e57-125">No se garantiza la integridad de bits.</span><span class="sxs-lookup"><span data-stu-id="f8e57-125">Bit integrity is not assured.</span></span> <span data-ttu-id="f8e57-126">La voz no está diseñada para admitir los tipos de medios de fax y módem.</span><span class="sxs-lookup"><span data-stu-id="f8e57-126">Speech is not intended to support fax and modem media types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e57-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ Voice**</span><span class="sxs-lookup"><span data-stu-id="f8e57-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e57-128">Se trata de un servicio de portador de nivel sonoro analógico de 3,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="f8e57-128">This is a regular 3.1 kHz analog voice-grade bearer service.</span></span> <span data-ttu-id="f8e57-129">No se garantiza la integridad de bits.</span><span class="sxs-lookup"><span data-stu-id="f8e57-129">Bit integrity is not assured.</span></span> <span data-ttu-id="f8e57-130">La voz puede admitir tipos de medios de fax y módem.</span><span class="sxs-lookup"><span data-stu-id="f8e57-130">Voice can support fax and modem media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8e57-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8e57-131">Remarks</span></span>

<span data-ttu-id="f8e57-132">Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8e57-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="f8e57-133">Los 16 bits de orden inferior están reservados.</span><span class="sxs-lookup"><span data-stu-id="f8e57-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="f8e57-134">Tenga en cuenta que el modo de portador y el tipo de medio son nociones diferentes.</span><span class="sxs-lookup"><span data-stu-id="f8e57-134">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="f8e57-135">El modo de portador de una llamada es una indicación de la calidad de la conexión telefónica tal como la proporciona principalmente la red.</span><span class="sxs-lookup"><span data-stu-id="f8e57-135">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="f8e57-136">El tipo de medio de una llamada es una indicación del tipo de flujo de información que se intercambia en esa llamada.</span><span class="sxs-lookup"><span data-stu-id="f8e57-136">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="f8e57-137">El módem de fax o de datos del grupo 3 son tipos de medios que usan una llamada con un modo de portador de voz 3,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="f8e57-137">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8e57-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8e57-138">Requirements</span></span>



| <span data-ttu-id="f8e57-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8e57-139">Requirement</span></span> | <span data-ttu-id="f8e57-140">Value</span><span class="sxs-lookup"><span data-stu-id="f8e57-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f8e57-141">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f8e57-141">TAPI version</span></span><br/> | <span data-ttu-id="f8e57-142">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f8e57-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f8e57-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8e57-143">Header</span></span><br/>       | <dl> <span data-ttu-id="f8e57-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8e57-144"><dt>Tapi.h</dt></span></span> </dl> |



 

