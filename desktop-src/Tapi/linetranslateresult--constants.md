---
description: Las \_ constantes de marcador de bits LINETRANSLATERESULT describen varios resultados de una traducción de direcciones.
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: Constantes de LINETRANSLATERESULT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad10c3da2b4250ded5706e4aaa10b9b61f8739b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681214"
---
# <a name="linetranslateresult_-constants"></a><span data-ttu-id="8632d-103">Constantes de LINETRANSLATERESULT \_</span><span class="sxs-lookup"><span data-stu-id="8632d-103">LINETRANSLATERESULT\_ Constants</span></span>

<span data-ttu-id="8632d-104">Las constantes de marcador de bits **LINETRANSLATERESULT \_** describen varios resultados de una traducción de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8632d-104">The **LINETRANSLATERESULT\_** bit-flag constants describe various results of an address translation.</span></span>

<dl> <dt>

<span data-ttu-id="8632d-105"><span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**\_canónico LINETRANSLATERESULT**</span><span class="sxs-lookup"><span data-stu-id="8632d-105"><span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT\_CANONICAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-106">Indica que la cadena de entrada tiene un formato canónico válido.</span><span class="sxs-lookup"><span data-stu-id="8632d-106">Indicates that the input string was in valid canonical format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8632d-107"><span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT \_ DIALBILLING**</span><span class="sxs-lookup"><span data-stu-id="8632d-107"><span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-108">Indica que la dirección devuelta contiene un "$".</span><span class="sxs-lookup"><span data-stu-id="8632d-108">Indicates that the returned address contains a "$".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8632d-109"><span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT \_ DIALDIALTONE**</span><span class="sxs-lookup"><span data-stu-id="8632d-109"><span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-110">Indica que la dirección devuelta contiene una "W".</span><span class="sxs-lookup"><span data-stu-id="8632d-110">Indicates that the returned address contains a "W".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8632d-111"><span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT \_ DIALPROMPT**</span><span class="sxs-lookup"><span data-stu-id="8632d-111"><span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-112">Indica que la dirección devuelta contiene un "?".</span><span class="sxs-lookup"><span data-stu-id="8632d-112">Indicates that the returned address contains a "?".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8632d-113"><span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT \_ DIALQUIET**</span><span class="sxs-lookup"><span data-stu-id="8632d-113"><span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-114">Indica que la dirección devuelta contiene un "@".</span><span class="sxs-lookup"><span data-stu-id="8632d-114">Indicates that the returned address contain a "@".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8632d-115"><span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT \_ International**</span><span class="sxs-lookup"><span data-stu-id="8632d-115"><span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT\_INTERNATIONAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-116">Indica que la llamada se está tratando como una llamada internacional (el código de país o región especificado en la dirección de destino es diferente del código de país o región especificado para el **CurrentLocation**).</span><span class="sxs-lookup"><span data-stu-id="8632d-116">Indicates that the call is being treated as an international call (country or region code specified in the destination address is different from the country or region code specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8632d-117"><span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT \_ INTOLLLIST**</span><span class="sxs-lookup"><span data-stu-id="8632d-117"><span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT\_INTOLLLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-118">Indica que la llamada local se está marcando como larga distancia porque el país o la región tiene llamada de peaje y el prefijo aparece en el **TollPrefixList** de **CurrentLocation**.</span><span class="sxs-lookup"><span data-stu-id="8632d-118">Indicates that the local call is being dialed as long distance because the country or region has toll calling and the prefix appears in the **TollPrefixList** of the **CurrentLocation**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8632d-119"><span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT \_ local**</span><span class="sxs-lookup"><span data-stu-id="8632d-119"><span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-120">Indica que la llamada se está tratando como una llamada local (el código de país o región y el código de área especificados en la dirección de destino son los mismos que los especificados para el **CurrentLocation**).</span><span class="sxs-lookup"><span data-stu-id="8632d-120">Indicates that the call is being treated as a local call (country or region code and area code specified in the destination address are the same as those specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8632d-121"><span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT \_ LONGDISTANCE**</span><span class="sxs-lookup"><span data-stu-id="8632d-121"><span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT\_LONGDISTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-122">Indica que la llamada se está tratando como una llamada de larga distancia (el código de país o región especificado en la dirección de destino es el mismo, pero el código de área es diferente de los especificados para el **CurrentLocation**).</span><span class="sxs-lookup"><span data-stu-id="8632d-122">Indicates that the call is being treated as a long distance call (country or region code specified in the destination address is the same but area code is different from those specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8632d-123"><span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT \_ NOTINTOLLLIST**</span><span class="sxs-lookup"><span data-stu-id="8632d-123"><span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT\_NOTINTOLLLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-124">Indica que el país o la región admite llamadas de peaje, pero el prefijo no aparece en **TollPrefixList**, por lo que la llamada se marca como una llamada local.</span><span class="sxs-lookup"><span data-stu-id="8632d-124">Indicates that the country or region supports toll calling but the prefix does not appear in the **TollPrefixList**, so the call is dialed as a local call.</span></span> <span data-ttu-id="8632d-125">Tenga en cuenta que, si tanto como inNOTINTOLLIST están desactivados, el país o la región actual no admiten prefijos de peaje y los elementos de la interfaz de usuario relacionados con prefijos de peaje no se deben presentar al usuario; Si este bit está activado, el país o la región admiten listas de peajes, y los elementos de la interfaz de usuario relacionados deben estar habilitados.</span><span class="sxs-lookup"><span data-stu-id="8632d-125">Note that if both INTOLLIST and NOTINTOLLIST are off, the current country or region does not support toll prefixes, and user-interface elements related to toll prefixes should not be presented to the user; if either such bit is on, the country or region does support toll lists, and the related user-interface elements should be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8632d-126"><span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT \_ NOtranslation**</span><span class="sxs-lookup"><span data-stu-id="8632d-126"><span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT\_NOTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-127">Indica que la traducción de direcciones no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8632d-127">Indicates that address translation is not available.</span></span> <span data-ttu-id="8632d-128">Este elemento solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="8632d-128">This element is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8632d-129"><span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT \_ VOICEDETECT**</span><span class="sxs-lookup"><span data-stu-id="8632d-129"><span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT\_VOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8632d-130">Indica que la dirección de marcado devuelta contiene un ":".</span><span class="sxs-lookup"><span data-stu-id="8632d-130">Indicates that the returned dialable address contains a ":".</span></span> <span data-ttu-id="8632d-131">Este elemento solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="8632d-131">This element is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>

> [!Note]  
> <span data-ttu-id="8632d-132">El carácter ":" (dos puntos) se agregará a la lista de caracteres que se puede incrustar en una cadena de marcado y pasarse a las direcciones de destino.</span><span class="sxs-lookup"><span data-stu-id="8632d-132">The ":" (colon) character will be added to the list of characters that can be embedded in a dialable string and passed into destination addresses.</span></span> <span data-ttu-id="8632d-133">Si intenta pasarlo desde una aplicación a un dispositivo de línea que admita una versión de API anterior a 2,0, lo más probable es que LINEERR \_ INVALADDRESS, o que en el carácter se omita por completo.</span><span class="sxs-lookup"><span data-stu-id="8632d-133">Attempting to pass it from an application to a line device that supports an API version earlier than 2.0 will most likely result in LINEERR\_INVALADDRESS, or possibly in the character being ignored entirely.</span></span> <span data-ttu-id="8632d-134">El significado de este carácter es "PAUSE hasta que se detecte un mensaje de voz y continúe marcando"; está pensada para su uso cuando se marca automáticamente en sistemas que proporcionan mensajes de voz, como procesadores de tarjetas de llamada a larga distancia.</span><span class="sxs-lookup"><span data-stu-id="8632d-134">The meaning of this character is "Pause until a voice prompt is detected, then continue dialing"; it is intended for use when automatically dialing into systems that give voice prompts, such as long distance calling card processors.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8632d-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8632d-135">Remarks</span></span>

<span data-ttu-id="8632d-136">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="8632d-136">No extensibility.</span></span> <span data-ttu-id="8632d-137">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="8632d-137">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="8632d-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8632d-138">Requirements</span></span>



| <span data-ttu-id="8632d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8632d-139">Requirement</span></span> | <span data-ttu-id="8632d-140">Value</span><span class="sxs-lookup"><span data-stu-id="8632d-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8632d-141">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8632d-141">TAPI version</span></span><br/> | <span data-ttu-id="8632d-142">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8632d-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8632d-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8632d-143">Header</span></span><br/>       | <dl> <span data-ttu-id="8632d-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8632d-144"><dt>Tapi.h</dt></span></span> </dl> |



 

 




